---
layout: project_details
categories: ["projects"]
title: "ImpactJS Enemy Editor"
url_demo: ""
url_source: "http://bitbucket.org/chessmasterhong/smw-koopa-krisis_enemy-editor"
thumbnail_style: "background: url(/img/editor0.png) no-repeat -5px -15px content-box; background-size: 280%;"
slides:
    - image: "/img/editor0.png"
      caption: "View all enemies' data in a project through an organized table. Efficiently batch edit multiple enemy data."
    - image: "/img/editor1.png"
      caption: "View enemy's data in a simple, easy to understand layout."
    - image: "/img/editor2.png"
      caption: "Quickly edit enemy's data using dynamic forms parsed from the enemy's source code."
---


The ImpactJS Enemy Editor originally started out as a specialized tool designed for the [Super Mario World: Koopa Krisis](/projects/super_mario_world_koopa_krisis) to assist us in quickly creating enemies. I later realized that this tool can be further extended to ImpactJS games in general. The aim is to provide a generic tool for ImpactJS developers to easily view and edit enemy files (either in bulk or as an individual file), quickly create new enemies, and to provide consistent code layout throughout files. This tool was heavily built on PHP, while utilizing some HTML5, CSS3, and JavaScript.


Background Information
---
While refactoring and fixing the code for all our existing enemies, I found it boring and tedious to have to manually edit each file. It is inefficient, time consuming, and very error-prone. There needed to be a way to edit large amounts of [ImpactJS] files if necessary. To my knowledge, no tool currently exists publicly that does this.


Features
---
This tool is, in a nutshell, boilerplate code generator. It abstracts the enemy's source code into a HTML form. The programmer would then just have to fill out the form with the appropriate enemy details and presto! An enemy is created. Likewise, it can parse and edit existing enemies.

The major time-saving feature of this tool is the ability to parse all of the project's enemies' data into an organized table view. This allows the developer to quickly view or edit all enemies at once, which is invaluable for refactoring and tweaking large amounts of files.

* View and all enemies in project directory via a table layout
* Edit the properties of multiple enemies at a given time
* View detailed report of enemy's properties without browsing through its source code
* Edit enemy's properties using source code with inline fields
* Create basic enemies using skeleton/template code


My Roles, Experiences, and Challenges
---
I wrote a custom JavaScript/ImpactJS code parser from scratch.
