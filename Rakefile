##
# Rakefile
# -----
# Modified by: Kevin Chan
#
# Description:
#   Rake task to generate the Jekyll site locally and deploy the contents of the
#   compiled site into a seperate branch, rather than the entire source of the
#   site. This prevents GitHub from building the site from source itself, making
#   this process ideal for adding Jekyll plugins.
#
# Requirements:
#   gem install jekyll              # Install Jekyll
#   git checkout -b source          # Create new branch "source"
#   git push -u origin source       # Push the (empty) "source" branch so that GitHub registers it.
#
# Usage:
#   Navigate to the root of your Git repository via terminal.
#   In terminal, run "rake publish" (without quotes)
#   Follow the prompt for username and password (needed to push to GitHub)
#
# Sources:
#   http://ixti.net/software/2013/01/28/using-jekyll-plugins-on-github-pages.html
#   http://blog.sorryapp.com/blogging-with-jekyll/2014/01/31/using-jekyll-plugins-on-github-pages.html

require "tmpdir"
require "jekyll"

# Get origin to which the site will be pushed to
ORIGIN = `git config --get remote.origin.url`

desc "Generate site files."
task :generate do
    # Compile the Jekyll site
    Jekyll::Site.new(Jekyll.configuration({
        "source"      => ".",
        "destination" => "_site"
    })).process
end

desc "Generate and publish site to gh-pages."
task :publish => [:generate] do
    # Make a temporary directory to build before deployment. This directory
    # will be torn down once task is complete.
    Dir.mktmpdir do |tmp|
        # Copy compiled site files to tmp directory
        cp_r "_site/.", tmp

        # Switch to tmp directory
        pwd = Dir.pwd
        Dir.chdir tmp

        # Prepare all compiled content for deployment
        system "git init"
        system "git add . && git commit -m 'Site updated at #{Time.now.utc}'"

        # Add origin remote for parent repo to tmp directory
        system "git remote add origin #{ORIGIN}"

        # Push files to gh-pages branch and force overwrite
        system "git push origin master --force"

        # Switch back to current directory
        Dir.chdir pwd
    end
end
