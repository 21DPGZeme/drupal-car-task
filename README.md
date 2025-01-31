# Drupal "Car" task

1.	Create new Drupal project using Composer.
2.	Add drush module to project using Composer
3.	Create content type "Car" with these fields:
    * Mark (type: text)
    * Color (type: text list; values: red, yellow, green)
    * Image (type: media image)
4.	Create new reference field for user. Field should have a reference to a car content type. User can have unlimited referenced cars.
5.	Create custom view block that outputs all content from content type "Car".
    * Block must output 3 items per page, with fields title, mark, color, image and user name.
    * It must have a pager.
    * List should start with latest added content to first (DESC)
    * Add color exposed filter.
    * Put block in front page
    * Add link in bottom of block to custom created route from next task.
6.	Create custom module named "Alter Car".
    * Create custom route
    * Route must return current user car count
    * Add permission to route that anonymous users cant view
7.	Alter color field output in block so that it outputs real color instead of text.
8.	Export all your site configs outside web folder using drush and push it on to your GIT repository. Send repository link to us for evaluation.
