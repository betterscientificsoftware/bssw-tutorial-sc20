---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# Hands-On: Module 8: Continuous Integration
## Goals
You'll establish a simple continuous integration workflow and then refine it, adding code coverage assessment

## Prerequisites
* A [GitHub](https://github.com) account
* A [Travis-CI](https://travis-ci.com) account linked to your GitHub account
* A [Codecov](https://codecov.io) account linked to your GitHub account

## Instructions
1. Fork the [hello-numerical-world-sc20](https://github.com/betterscientificsoftware/hello-numerical-world-sc20) repository
2. Add a .travis.yml file to run ‘make check’
3. Submit a PR to us
4. Add code coverage verification using codecov.io
    1. You need to tell the compiler and linker to generate the code coverage report
    2. Once the tests are finished executing, you need to upload the coverage files to codecov.io
5. Observe code coverage results when updated PR is tested
6. Increase test coverage by changing ‘make check’ to ‘make check_all’
7. Observe changes in code coverage results when updated PR is tested
    - Also observe the changes in the time required to execute the more extensive tests
8. Extra credit: Make the CI test fail if code coverage drops
    - Hint: read codecov.io documentation

A video walk-through of (most of) this exercise is available at: <https://youtu.be/QE4RFp8lGiQ>
* This video was created by Mark Miller (LLNL) for tutorial at ATPESC earlier this year.  Where he refers to the repository as `hello-numerical-world-atpesc-2020`, substitute `hello-numerical-world-sc20`.