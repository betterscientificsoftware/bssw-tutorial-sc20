---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# Welcome to Better Scientific Software

The [Better Scientific Software tutorial](https://sc20.supercomputing.org/presentation/?id=tut146&sess=sess275) will be presented on Tuesday 10 November 2020 as part of the [Supercomputing 2020](https://sc20.supercomputing.org) (SC20) conference.  [Registration](https://sc20.supercomputing.org/attend/register/) for the tutorial program ("TUT") will be required to participate.

This site will provide late-breaking updates and additional information and resources for participants in the tutorial.  Expect updates to this site up to, and perhaps shortly after, the date of the tutorial.

*Last update: {{ "now" | date: "%F" }}*

## Final Version of Slides

The final slides will be available at <https://doi.org/10.6084/m9.figshare.12994376> when they are ready.

## Agenda

| Time (EST) | Module | Topic | Speaker | Time (UTC) |
|-----------:|-------:|-------|---------|-----------:|
| 2:30pm-2:35pm | 00 | Introduction | David E. Bernholdt, ORNL | 19:30-19:35 |
| 2:35pm-2:45pm | 01 | Motivation and Overview of Best Practices in HPC Software Development | David E. Bernholdt, ORNL | 19:35-19:45 |
| 2:45pm-3:15pm | 02 | Agile Methodologies | Rinku Gupta, ANL | 19:45-20:15 |
| 3:15pm-3:30pm | 03 | Git Workflows | Patricia Grubel, LANL | 20:15-20:30 |
| 3:30pm-4:00pm | 04 | Software Design | Anshu Dubey, ANL | 20:30-21:00 |
| 4:00pm-4:15pm | 05 | Software Testing 1 | Rinku Gupta, ANL | 21:00-21:15 |
| *4:15pm-4:35pm* |  | *Beak (live Q&A and demo of Kanban hands-on activities)* | *David E. Bernholdt and All* | *21:15-21:35* |
| 4:35pm-4:50pm | 06 | Software Testing 2 | Anshu Dubey, ANL | 21:35-21:50 |
| 4:50pm-5:35pm | 07 | Refactoring | Anshu Dubey, ANL | 21:50-22:35 |
| 5:35pm-5:50pm | 08 | Continuous Integration | David E. Bernholdt, ORNL | 22:35-22:50 |
| 5:50pm-6:05pm | 09 | Reproducibility | Patricia Grubel, LANL | 22:50-23:05 |
| 6:05pm-6:10pm | 10 | Summary | David E. Bernholdt, ORNL | 23:05-23:10 |
| *6:10pm-6:30pm* |  | *Live Q&A and demo of CI hands-on activities* | *David E. Bernholdt and All* | *23:10-23:30* |

## Hands-On Exercises

### Module 9: Continuous Integration
#### Prerequisites
* A [GitHub](https://github.com) account
* A [Travis-CI](https://travis-ci.com) account linked to your GitHub account
* A [Codecov](https://codecov.io) account linked to your GitHub account

#### Instructions
1. Fork the hello-numerical-world-sc20 repository
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


## Resources from Presentations
*These are the links included in the tutorial presentations, for easier access*

* Module 0:
* Module 1:
* Module 2:
* Module 3:
* Module 4:
* Module 5:
* Module 6:
* Module 7:
* Module 8:
* Module 9: Continuous Integration
* Module 10:
* Module 11:

## Acknowledgements

The BSSw tutorial is produced by the [IDEAS Productivity project](https://ideas-productivity.org).

This work was supported by the U.S. Department of Energy Office of Science, Office of Advanced Scientific Computing Research (ASCR), and by the Exascale Computing Project (17-SC-20-SC), a collaborative effort of the U.S. Department of Energy Office of Science and the National Nuclear Security Administration.