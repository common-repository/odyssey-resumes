=== Odyssey Resumes ===
Contributors: (wordpressnoob777)
Donate link: http://odysseycreativedesign.com/
Tags: resumes, resume, profile
Requires at least: 4.6
Tested up to: 5.3.2
Stable tag: 1.0.0
Requires PHP: 5.3
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html


An easy to use Resume plugin that allows custom templates and themes for your resume.  This plugin requires ACF as of now but we will add universal support soon.

== Description ==

Build beautiful resumes with this easy to use plugin which allows custom templates and child themes. Swatches allow the user to instantly switch between multiple color schemes for the same resume.

* Supports Contact Info, About Me, Pictures, Work Experience, Skill Sliders, Education, Links and References
* Create multiple versions of the same resume
* Create your own Custom templates and themes
* Integrates with ACF and comes with ACF JSON (acf.json)
* Animations and SVG Pre Loaders
* Customizable print stylesheet
* Comes with SASS!
* Social Media Section



== Coming Soon ==

* TODO: Awards Section
* TODO: add share button to send pdf
* TODO: show dark screen at night, light at day be default
* TODO: PDF Download Button (jspdf seems buggy)
* TODO: composer plugin
* TODO: add twig support


==  Prerequisites ==

You must have the following plugins or files available.  We will add gravity forms support, as well as a verion which will not depend on either plugin.  But we strongly recommend using ACF if you want to customize your resume.

* ACF with Google Maps
https://www.advancedcustomfields.com/

You will need to enter your own google maps api key in this file.
`am-resume/functions.php`

* Font Awesome
This plugin assumes you have font awesome. The icons will not show up without Font Awesome but you can easily create your own template and use your own icons.

* Animate.css
Animations are optional but if you would like to use them.

[Animate.css](https://daneden.github.io/animate.css/)

==  Installation  ==

1. First make sure that the ACF plugin is installed and activated already.  We will be adding support for Gravity Forms as well as a standalone version.  There is settings page as of now and all the options are configured on a per resume basis via ACF.

2. Go to your site's ACF Tools and use the import button to import the JSON in the file `acf.json`.

3. If your site doesn't already use Font Awesome then you can add the cdn files in your template file.

`
wp_enqueue_style('print-resume', plugin_dir_url(__FILE__) . 'default/default.css');
wp_enqueue_script('page-resume', plugin_dir_url(__FILE__) . 'default/default.js', array('jquery'), false, true);
`


4. Activate this plugin and look for `Resume` in the left hand column


==  Themes and Templates: ==

* Themes

A theme is a small css file that is used in addition to your main css file.  A theme can be changed from the swatches on the top right that allow you to switch from light to dark theme.

There is a basic line of jquery in the default.js file that switches stylesheets.

* Templates

And templates are css, js and php file used to render the resume.

There is a default template included in the plugin at `templates/default/`

* Creating a New Template

To create a new template, you only have to add the files you want to change.

There is an included template called `default-theme` that serves as an example of how you can override whatever file you want in the `default` template.

Then  you just enter your new theme name in the ACF field for your Resume Post.


== npm Deploy Styles to Assets Folder ==

I have used simple NPM scripts to compile css. There is no need to install gulp since there are not a lot of tasks.  To deploy stylesheets to the assets folder, you can just type the command below.  You will need to install sass globally for this command to work, which you should already have!

`npm deploy;`

== Frequently Asked Questions ==

=== How do I create a new template or theme?  ===

You can copy files one by one from the `templates/default` folder and place them in a new directory in `templates`.


=== How do I add a child theme?  ===

You can also add a child theme so you don't have to copy the entire template.  To add a child theme, create a new folder for your theme in the templates directory.  Then copy only the files you want to customize into the folder.  Set your template to use the child theme and that's it!

=== Will this plugin work without ACF? ===

As of now, this plugin requires ACF but this will change in the future.

== Changelog ==

Version 1.0 is the first release

== Upgrade Notice ==

### 1.0 ###
First release

== Screenshots ==

[screenshot1.png  Skills Matrix in Light Theme]
[screenshot2.png  Skills Matrix in Dark Theme]
[screenshot3.png  ACF Fields]
[screenshot4.png  Resume Header]
