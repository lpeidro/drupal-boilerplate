# Metadrop's Drupal Boilerplate

## Introduction

This repository is a boilerplate to create Drupal 8/9/10 projects with many tools already preconfigured with minimal effort. You can have a Drupal site running in your local in less than 3 minutes.

Tools included out-of-the-box:

  - A Docker infrastructure.
  - A boilerplate folder structure that fits all project needs.
  - A working and preconfigured Drush, the Drupal shell.
  - MkDocs to document your project using Markdown files.
  - Grumphp to enforce [Drupal coding standards](https://www.drupal.org/docs/develop/standards/coding-standards). It is configured to use [phplint](https://github.com/overtrue/phplint), yamlint,  [jsonlint](https://github.com/Seldaek/jsonlint), [drupalcheck](https://github.com/mglaman/drupal-check), [phpcpd](https://github.com/sebastianbergmann/phpcpd) and [phpcs](https://github.com/squizlabs/PHP_CodeSniffer).
  - Phpqa for static analysis.
  - Behat BDD testing configured and working.
  - PHPUnit for unit testing configured and working.
  - [BackstopJS](https://github.com/garris/BackstopJS) for visual regression testing.
  - [Stylelint](https://stylelint.io/) for checking style files.
  - [Scripthor](https://github.com/Metadrop/scripthor) toolset with some helper scripts for development.
  - Optionally, a Solr container ready to be used by Drupal.

It is based on [Docker4Drupal](https://wodby.com/docs/1.0/stacks/drupal/local/), which uses Docker and Docker Compose. To get all the information about available webservers, databases, PHP versions and other containers check their [wodby/docker4drupa repository](https://github.com/wodby/docker4drupal).

Because it uses Docker under the hood, you can customize whatever you want, add new containers or use any standard Docker funcionality to accomodate your project needs.

## Quickview
![Create project](./create-project.gif)


## Requisites

 - [Docker](https://docs.docker.com/get-docker/)
 - [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

To create a new project based on this boilerplate, the recommended method is using Composer's create-project command:

```
composer create-project  --ignore-platform-reqs metadrop/drupal-boilerplate my-project
```


Once Composer finalizes the project creation an assistant will be autmatically run. It will ask you a few questions:

 - The project name: this a machine name for the project. It will be used for Docker container names, project URL and some other places. Please, use only letters, numbers and underscores.

 - Setup a git repository? If yes, the assistant will initialize a git repository and make the initial commit.

 - Install Drupal? If thes, the assistan will configure and install a Drupal site.

 - Radix sub-theme: the asistant can create a [Radix](https://www.drupal.org/project/radix) subtheme for you. We quite often use Radix as the base theme of our projects. You can skip this and use your own theme, of course.


After the assistant finished, if you have selected to install Drupal your project will be running and the assitant will print the URL to access it.















## FAQ


### Is this for me?

This boilerplate is a good choice for medium to advanced users that want to have a full local environment with a complete set of tools ready to use for their Drupal projects in matter of minutes. However, you should be comfortable using Docker, Drush and another tools without a managing layer like DDEV provides.


### Why not Lando/DDEV/whatever?

We love them! However, we have had some issues trying to adapt them to a certain edge case projects. Those tools allows to handle complex topics like docker thanks to a managing layer. However, that layer imposes some limits. It is not easy to hit them, but when you do it is a hard limit. That's when this boilerplate can be helpful.


