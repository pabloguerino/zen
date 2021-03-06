TEMPLATES
---------

I couldn't figure out which template controlled which bit of markup, but then I
read https://www.drupal.org/node/223440#theme-debug and my mind is blown!

Okay, maybe that last sentence is a bit link-baity. But it's probably the most
useful tip you are going to get about the Drupal theme system. Using a browser's
DOM inspector is a natural way to investigate something on a page generated by
Drupal. The Zen theme automatically tells Drupal to output HTML comments
detailing all the templates used to build the current page. You should disable
this setting before moving your sub-theme to a production website; go to the
sub-theme's settings page (available from admin/appearance).


TEMPLATE LOCATIONS
------------------

Drupal 7 contains the following template files which you can override and modify
by copying them to your sub-theme.

Your Zen sub-theme overrides a handful of Drupal's templates. Those are the
*.html.twig files you see in this directory. All other templates come from the
classy theme. In order to override those templates, you should copy them from
the core/classy/templates folder to your sub-theme's templates folder.

As always, when adding a new template file to your sub-theme, you will need to
rebuild the "theme registry" in order for Drupal to see it. For more info, see:
  https://drupal.org/node/173880#theme-registry
