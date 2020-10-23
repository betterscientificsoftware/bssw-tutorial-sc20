---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# Welcome to Better Scientific Software

The [Better Scientific Software tutorial](https://sc20.supercomputing.org/presentation/?id=tut146&sess=sess275) will be presented on Tuesday 10 November 2020 as part of the [Supercomputing 2020](https://sc20.supercomputing.org) (SC20) conference.  [Registration](https://sc20.supercomputing.org/attend/register/) for the tutorial program ("TUT") will be required to participate.

This site will provide late-breaking updates and additional information and resources for participants in the tutorial.  Expect updates to this site up to, and perhaps shortly after, the date of the tutorial.

*Last update: {{ "now" | date: "%F" }}*

---
## Table of Contents
* [How to Participate](#how-to-participate) 
* [Stay in Touch](#stay-in-touch) 
* [Presentation Slides](#presentation-slides) 
* [Agenda](#agenda) 
* [Hands-On Exercises](#hands-on-exercises) 
* [Resources from Presentations](#resources-from-presentations) 
* [Requested Citation](#requested-citation)
* [Acknowledgements](#acknowledgements) 

---

## How to Participate

* Most presentations have been pre-recorded, though there are several live sessions interspersed.

* Please use the chat tool to ask questions *at any time*. The speaker and the rest of the tutorial team will be monitoring and will respond.  

* The schedule includes a break in the middle, where we plan to do more Q&A and if there is interest, some demos from the hands-on exercises.  There is also a segment at the end for additional Q&A and demos.

* Participation in the Q&A and demonstrations is optional – we know you need breaks too.

* **Your feedback is important both to us and to the SC20 organizers.  Please remember to [evaluate us](https://submissions.supercomputing.org/?page=Submit&id=TutorialEvaluation&site=sc20)!**

---
## Stay in Touch

* If you think of more questions you'd like to ask, or you're not able to participate in the live session, please feel free to email the BSSw tutorial team at <bssw-tutorial@lists.mcs.anl.gov>.

* If you want to do the hands-on exercises on your own, we're happy to provide feedback on your pull requests.

* To find out about future events organized by the IDEAS Productivity Project, you can [subscribe to our mailing list](http://eepurl.com/cQCyJ5) (usually ~2 messages/month).

* For monthly updates on the Better Scientific Software site, subscribe to our [monthly digest](https://bssw.io/pages/receive-our-email-digest).

---
## Presentation Slides

* The latest version of the slides will always be available at **<https://doi.org/10.6084/m9.figshare.12994376>**.

* This is currently the same version as you may have obtained through SC20.

* Note that these files may include additional slides that will not be discussed during the tutorial, but questions are welcome.

---
## Agenda

The live presentation takes place **2:30-6:30pm ET, Tuesday 10 November 2020 (19:30-23:30 UTC)**.

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

---
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

---
## Resources from Presentations
*These are the links included in the tutorial presentations, included here for easier access*

* Module 0: Introduction
  * [IDEAS Productivity Project](http://ideas-productivity.org)
    * [IDEAS Productivity mailing list](http://eepurl.com/cQCyJ5)
  * [Better Scientific Software site](https://bssw.io)
    * [BSSw Digest](https://bssw.io/pages/receive-our-email-digest)
    * [RSS Feed](https://bssw.io/items.rss)
  * [The IDEAS Report](https://exascaleproject.org/better-scientific-productivity-through-better-scientific-software-the-ideas-report)
  * [Tutorial Evaluation Link](https://submissions.supercomputing.org/?page=Submit&id=TutorialEvaluation&site=sc20)
  * [Write to the tutorial authors](mailto:bssw-tutorial@lists.mcs.anl.gov)
* Module 1: Motivation and Overview of Best Practices in HPC Software Development
  * *none*
* Module 2: Agile Methodologies
* Module 3: Git Workflows	
* Module 4: Software Design
* Module 5: Software Testing 1
* Module 6: Software Testing 2
* Module 7: Refactoring
* Module 8: Continuous Integration
  * [Exascale Computing Project CI documentation](https://ecp-ci.gitlab.io/)
  * [Travis CI service](https://travis-ci.com)
  * [Codecov service](https://codecov.io)
* Module 9: Reproducibility
* Module 10: Summary
  * COVID-19 epidemiology saga
    * <https://doi.org/10.25561/77482>
    * <https://www.nicholaslewis.org/imperial-college-uk-covid-19-numbers-dont-seem-to-add-up/>
    * <https://www.nature.com/articles/d41586-020-01003-6>
    * <https://www.foxnews.com/world/imperial-college-britain-coronavirus-lockdown-buggy-mess-unreliable>
    * <https://www.telegraph.co.uk/technology/2020/05/16/coding-led-lockdown-totally-unreliable-buggy-mess-say-experts/>
    * <https://github.com/mrc-ide/covid-sim/>
    * <https://philbull.wordpress.com/2020/05/10/why-you-can-ignore-reviews-of-scientific-code-by-commercial-software-developers/amp/>
    * <http://doi.org/10.5281/zenodo.3865491>
  * [Productivity and Sustainability Improvement Planning](https://bssw.io/psip)
  * [Better Scientific Software web site](https://bssw.io/)

---
## Requested Citation
The requested citation the overall tutorial is: David E. Bernholdt, Anshu Dubey, Patricia A. Grubel, Rinku K. Gupta, Better Scientific Software tutorial, in SC ‘20: International Conference for High Performance Computing, Networking, Storage and Analysis, online, 2020. DOI: [10.6084/m9.figshare.12994376](https://doi.org/10.6084/m9.figshare.12994376)

Individual modules may be cited as *Speaker*, *Module Title*, in Better Scientific Software tutorial…

---
## Acknowledgements

The BSSw tutorial is produced by the [IDEAS Productivity project](https://ideas-productivity.org).

This work was supported by the U.S. Department of Energy Office of Science, Office of Advanced Scientific Computing Research (ASCR), and by the Exascale Computing Project (17-SC-20-SC), a collaborative effort of the U.S. Department of Energy Office of Science and the National Nuclear Security Administration.
