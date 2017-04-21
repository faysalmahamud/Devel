=== DEVEL ===
Contributors: faysal.turjo
Tags: generator, dummy content, dummy data, lorem ipsun, admin, exemples, testing, images, attachments, featured image, taxonomies, users, post type, faker, fake data, random, developer, dev, development, test, tests, demo, data, example, dummy, users, blogs, sample,developer, development, local,deprecated, logging, admin, WP_DEBUG, E_NOTICE, developer,menu, duplicate, copy, clone, reset, admin,users, profiles, user switching, fast user switching, multisite, become, user management, developer
Donate link: https://github.com/faysalmahamud
Requires at least: 3.4
Tested up to: 4.7
Stable tag: 1.2.6
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

A plugin, which helps WordPress developers develop.

== Description ==
  A suite of plugin containing fun for plugin developers and themers.

  If you'd like to check out the code and contribute, [join with me on GitHub](https://github.com/faysalmahamud/Devel). Pull requests, issues, and plugin recommendations are more than welcome!

  Devel
  Helper functions for Wordpress developers and inquisitive admins.

  The plugin basically covered drupal devel with extentive features.

  Key Features
    -- Generate content
    -- Generate User
    -- Generate Terms
    -- Generate Taxonomy
    -- Generate Menus

    Generate function is currently support for acf, pods fields and posttypes & fields(ongoing) plugins.

    For custom field of any post types using functions.php Be sure you use given functions or update field using

  Additional Features
    -- PHP info
    -- function reference
    -- filter and action reference
    -- Status report
    -- Query Analizer
    -- Widget Testing
    -- User Switching
    -- Wordpress Reset
    -- Git branch
    -- RTL Tester
    -- Execute PHP Code
    -- Deprecated Notices
    and so on....

  To see documetation goto plugins documentation section or http://faysalmahamud.com/wordpress/

  = DEBUG USAGE =
    Enable the included Kint as for pretty print of variables. kint($array) function is provided, which pretty prints arrays. Useful during development.

    * `d( $var )`
    * `print_log( $vars, $name = '', $inline = false )`
    * `dsm($input, $name = NULL)`
    * `dpm($input, $name = NULL)`
    * `print_wp_query($inline = false)`
    * `print_wp($inline = false)`
    * `print_post($inline = false)`

   - explained below

    = kint Way =
      `<?php d( $var ); ?>`

      Examples:

      <?php global $post; d( $post ); ?>

      `<?php
          global $post;
          $term_list = wp_get_post_terms( $post->ID, 'my_taxonomy', array( 'fields' => 'all' ) );
          d( $term_list );
      ?>`
    = Devel Basic Way =
      Examples:
      print_log( $vars, $name = '', $inline = false )
      `<?php
          global $post;
          $term_list = wp_get_post_terms( $post->ID, 'category', array( 'fields' => 'all' ) );
          print_log( $term_list);
      ?>`

      Examples:
      some helper functions that are frequently needed
      `<?php print_wp_query();?>`
      `<?php print_wp();?>`
      `<?php print_post();?>` gives The post object for the current post
    = Drupal Way =
      Drupal Lovers can use this function
      * `dsm($input_name)`
      * `dpm($input_name)`

      `<?php dsm( array('test1,test2') ); ?>`
      `<?php dpm( array('test1,test2') ); ?>`
      `<?php
          global $post;
          $term_list = wp_get_post_terms( $post->ID, 'my_taxonomy', array( 'fields' => 'all' ) );
          dsm( $term_list , true );
          //OR
          dpm( $term_list , true );
      ?>`
    = Your Own Functions =
      `<?php
      function your_own_function() {
           global $post;
           $term_list = wp_get_post_terms( $post->ID, 'my_taxonomy', array( 'fields' => 'all' ) );
           d( $term_list  );
      }
      ?>`

      Then at strategic points in your theme or plugin:

      `<?php your_own_function(); ?>`

    Obviously, if this plugin is not active, calls to the helper functions will cause errors.
  = GENERATE USAGE =
    Generate posts, users,menus,taxonomy,terms used for created dummy contents.

    However wordpress has not any fixed post type or field types. There are several plugins for that. It is not possible to give support for all post types of custom fields plugin.

    Currently Support
    1. [acf](https://wordpress.org/plugins/advanced-custom-fields/)
    2. [pods](https://wordpress.org/plugins/pods/)
    3. [post-types&fields](https://github.com/faysalmahamud/post-types-fields)

    If you use fields using functions.php. You can use devel generated functions or add update option using the following.
      -- coming soon

== Installation ==

  1. Upload the `devel` folder to your plugins directory (e.g. `/wp-content/plugins/`)
  2. Activate the plugin through the 'Plugins' menu in WordPress
== Frequently Asked Questions ==

= Why are there no FAQs besides this one? =

Because you haven't asked one yet.

== Screenshots ==

1. On activation, the plugin prompts you to specify what type of developer you are. This is used to configure the plugins checks.
2. On activation, the plugin does a quick check to see if you have essential developer plugins installed.
3. With one click you can install and activate the plugin.
4. The plugin's settings page (Tools > Developer) will check to make sure your environment is correctly configured, including plugins, constants, and other settings.

== Changelog ==
= 1.0 =
* Initial Release

== Upgrade Notice ==
= 1.0 =
This release contains a few bug fixed and many enhancements and new features, and is a recommended update.
