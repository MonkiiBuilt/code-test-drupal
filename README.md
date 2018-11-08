# Hello!

Welcome to the [Monkii](https://www.monkii.com.au) Code Test.

If you're reading this message, you have probably been in
touch with Monkii about a role as a [Drupal Developer](https://www.monkii.com.au/careers/drupal).

This repo contains a set of exercises for Drupal developers
which will give you an opportunity to demonstrate your
level of skill and problem solving capabilities.

You should plan to spend **3 - 4 hours** completing the
exercises in this test. You may not finish everything, so
prioritise the tasks which you feel most comfortable
completing.

## How to complete the test

This repo contains a pre-configured vm and a bare Drupal 8
installation. To complete the test, you should:

* clone the repo
* install the pre-requisites ([VirtualBox](https://www.virtualbox.org/wiki/Downloads) and [Vagrant](https://www.vagrantup.com/downloads.html))
* initialise the vm (this takes a while!)
* complete the exercises in this README
* zip up the entire `code-test-drupal` folder and email it
to [careers@monkii.com](mailto:careers@monkii.com)

**Important:** please **do not** fork the repo or push your
completed test to a public repo.

## Getting started

Install the latest versions of the pre-requisites:
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)

Navigate to the repo in a terminal and start the vm:

`vagrant up`

Vagrant will ask you to enter your password at some points
in order to create NFS shares. Once you've reached this
point, go make a coffee/tea as it may take 10-20 minutes to
complete.

When the vm is ready, you should be able to navigate to
your new Drupal site at [http://monkiicode.test](http://monkiicode.test).

## Completing the exercises

Each exercise is worded as a feature request, so pretend
we are an important client who you want to keep very happy.

Tasks should be completed using a combination of the
techniques at your disposal as a seasoned Drupal developer,
such as:
* contributed modules and base themes
* custom module(s)
* custom theme
* Drupal config
* other libraries

When deciding how to complete each exercise, here are a few 
things to keep in mind:
* the feature should be easy to use for "the client"
* code should be easy to understand and maintainable
* git commits should be organised with good commit messages
(yes we will be checking!)
* there should be no manual steps to "deploy" your feature.
For example, if a taxonomy needs to be created, it should
be done with code or config that's committed to the repo.

## Once you've finished

When you're all finished with the test, make sure you've
committed your features to your local repo and then zip up
or archive the entire `code-test-drupal` folder. This should
be sent in an email to [careers@monkii.com](mailto:careers@monkii.com)
with any notes you'd like to include about your submission.

You might also want to clean up your vm by navigating to the
project folder in a terminal and typing:

`vagrant destroy`

## A note on tools

### Vagrant

The Ubuntu-based vm in this project is based on the
excellent DrupalVM project by geerlingguy: https://github.com/geerlingguy/drupal-vm

Once provisioned, you can access the vm via the command:

`vagrant ssh`

Inside the VM, this project folder will be mounted at:

`/var/www/drupalvm`

The Drupal install will be in:

`/var/www/drupalvm/drupal`

### Composer

The Drupal installation has been created using composer. This
means Drupal core and contributed modules should not be
checked into the repo (these folders have been added to
.gitignore).

If you want to use a contributed module from drupal.org, it
can be added to the repo using composer, ie:

`composer require drupal/MODULE_NAME`

Composer can also be used to add non-Drupal libraries to
the project. All dependencies added this way will end up in
`composer.json` and `composer.lock`, which should be
committed to the repo.

### Drush

If you're familiar with drush, you can use it to speed up
a lot of your tasks. Here are a few useful commands, but
there are many more that can be discovered just by running
`drush` in the Drupal folder inside the vm.

#### Enabling modules

`drush pm:enable MODULE_NAME`

**Note:** contributed modules should be downloaded first
via composer.

#### Clearing caches

`drush cache:rebuild`

#### Export Drupal config to the project

`drush config:export`

**Note:** this is a great way to build things like content
types and taxonomies, and configure modules. Running this
command will write your Drupal config to yaml files in the
folder:

`drupal/config/sync`

which
can be committed to the repo.

# Exercises

# Thank you!

We're so excited to see how you solve these problems, and
look forward to working with you in the near future. :)