# nyu-lab-bdd-tdd

[![Build Status](https://travis-ci.org/rofrano/nyu-lab-bdd-tdd.svg?branch=master)](https://travis-ci.org/rofrano/nyu-lab-bdd-tdd)
[![Codecov](https://img.shields.io/codecov/c/github/rofrano/nyu-lab-bdd-tdd.svg)]()

NYU DevOps lab on Behavior Driven Development and Test Driven Development

## Introduction

One of my favorite quotes is:

_“If it's worth building, it's worth testing.
If it's not worth testing, why are you wasting your time working on it?”_

As Software Engineers we need to have the discipline to ensure that our code works as expected and continues to do so regardless of any changes, refactoring, or the introduction of new functionality.

This lab introduces Test Driven Development using `PyUnit` and `nose`. It also explores the use of using RSpec syntax with Python through the introduction of `noseOfYeti` and `expects` as plug-ins that make test cases more readable.

It also introduces Behavior Driven Development using `Behave` as a way to define Acceptance Tests that customer can understand and developers can execute!

## Setup

For easy setup, you need to have Vagrant and VirtualBox installed. Then all you have to do is clone this repo and invoke vagrant:

    git clone git@github.com:rofrano/nyu-lab-bdd-tdd.git
    cd nyu-lab-bdd-tdd
    vagrant up && vagrant ssh
    cd /vagrant

You can now run `behave` and `nosetests` to run the BDD and TDD tests respectively.

## Manually running the Tests

Run the tests using `unittest`

    $ python -m unittest discover

Run the tests using `nose`

    $ nosetests

Nose is configured to automatically include the flags `--with-spec --spec-color` so that red-green-refactor is meaningful. If you are in a command shell that supports colors, passing tests will be green while failing tests will be red.

Run Code Coverage to see how well your test cases exercise your code:

    $ coverage run test_server.py
    $ coverage report -m --include= server.py

This is particularly useful because it reports the line numbers for the code that is not covered so that you can write more test cases.

You can even run `nosetests` with `coverage`

    $ nosetests --with-coverage --cover-package=server

Try and get as close to 100% coverage as you can.

## What's featured in the project?

    * server.py -- the main Service using Python Flask
    * test_server.py -- test cases using unittest
    * test_server_spec.py -- test specs using noseOfYeti
    * ./features/pets.feature -- Behave feature file
    * ./features/steps/steps.py -- Behave step definitions

This repo is part of the DevOps course at NYU