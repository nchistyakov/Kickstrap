The Gist
========

Kickstrap uses the latest version of Twitter's bootstrap (http://twitter.github.com/bootstrap) and adds a layer of extras to create slick web applications with themes, modern html/css standards, an icon font, and progressive enhancement through javascript.

Last updated with Bootstrap v. 2.02

The Extras
==========

**Font Awesome**

Turns glyphicons into an icon font to use a variety of sizes and colors. Also adds a bunch of new icons.

+ http://fortawesome.github.com/Font-Awesome/#

**HTML5 Boilerplate Goodies**

Uses sample files and resources gathered and created from HTML5 Boilerplate for making great HTML5 pages. Bootstrap Extra includes a sample file ready to go for a new Bootstrap HTML5 Page.

+ http://html5boilerplate.com/

**Themes**

+ Easily switch to different color schemes.
+ Support for Bootswatch themes. Easily switch between predefined theme packages.
+ http://bootswatch.com/

Change Themes
-------------

1. Open /extras/less/overrides.less
2. Uncomment the @import lines of the theme you want to use.
3. Compile.

Upgrade bootstrap core (if you don't want to wait for me to do it)
-------------------------------------------------------------------------

Using bootstrap extras requires using the LESS framework in your development environment. 
At this time, you can avoid having to do this by simply downloading the latest releases of Bootstrap extras from GitHub.

1. Download complete bootstrap files from http://twitter.github.com/bootstrap
2. Simply paste everything into the root of this directory (at the same level as index.html and 404.html)
3. Edit /less/bootstrap.less
4. After this line:<pre>
@import "variables.less"; // Modify this for custom colors, font-sizes, etc</pre>
Add this line: <pre>
@import "../extras/less/overrides.less"; // Use our own variables if we want.</pre>
So it should look like this:<pre>
// Core variables and mixins
@import "variables.less"; // Modify this for custom colors, font-sizes, etc
@import "../extras/less/themes.less"; // Use our own variables if we want.
@import "mixins.less";</pre>
5. Comment out the sprites line like this<pre>
//@import "sprites.less";</pre>
6. In the same file add this to the very end:<pre>
//Overrides
@import "../extras/less/overrides.less";</pre>
7. Compile and you're set.

Authors
-------

**Mark Otto** (Bootstrap)

+ http://twitter.com/mdo
+ http://github.com/markdotto

**Jacob Thornton** (Bootstrap)

+ http://twitter.com/fat
+ http://github.com/fat

**Adam Kochanowicz** (Kickstrap)

+ http://twitter.com/yourwebsitesUX

Copyright and license
---------------------

Bootstrap: Copyright 2012 Twitter, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
