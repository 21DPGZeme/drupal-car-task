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

# Installation instructions

1. Install WSL and Docker
2. Run this command in your Linux terminal to install DDEV:
`curl -fsSL https://raw.githubusercontent.com/ddev/ddev/master/scripts/install_ddev.sh | bash`
3. Run these commands to create and start a new drupal project:
`mkdir my-drupal-site && cd my-drupal-site`
`ddev config --project-type=drupal10 --docroot=web`
`ddev start`
`ddev composer create drupal/recommended-project:^10`
`ddev composer require drush/drush`
`ddev drush site:install --account-name=admin --account-pass=admin -y`
`ddev launch`
`# or automatically log in with`
`ddev launch $(ddev drush uli)`
4. If your terminal can't find a browser you can set it by adding this line to ~/.bashrc (may require restart):
`export BROWSER="powershell.exe /C start"`
5. Import the config files using Drush
