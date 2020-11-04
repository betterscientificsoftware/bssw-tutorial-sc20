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

* [Registration](https://sc20.supercomputing.org/attend/register/) for the tutorial program ("TUT") is required.

* Most presentations have been pre-recorded, though there are several live sessions interspersed.

* Please use the chat tool to ask questions *at any time*. The speaker and the rest of the tutorial team will be monitoring and will respond.  

* The schedule includes a break in the middle, where we plan to do more Q&A and if there is interest, some demos from the hands-on exercises.  There is also a segment at the end for additional Q&A and demos.

* Participation in the Q&A and demonstrations is optional – we know you need breaks too.

* **Your feedback is important both to us and to the SC20 organizers.  Please remember to [evaluate us](https://submissions.supercomputing.org/?page=Submit&id=TutorialEvaluation&site=sc20)!**

---
## Stay in Touch

* After the tutorial, or if you're not able to participate in the live session, please feel free to email the BSSw tutorial team at <bssw-tutorial@lists.mcs.anl.gov>.

* If you want to do the [hands-on exercises](#hands-on-exercises) on your own, we're happy to provide feedback on your pull requests.

* To find out about future events organized by the IDEAS Productivity Project, you can [subscribe to our mailing list](http://eepurl.com/cQCyJ5) (usually ~2 messages/month).

* For monthly updates on the Better Scientific Software site, subscribe to our [monthly digest](https://bssw.io/pages/receive-our-email-digest).

---
## Presentation Slides

* The latest version of the slides will always be available at **<https://doi.org/10.6084/m9.figshare.12994376>**.
  - Note that these files may include additional slides that will not be discussed during the tutorial, but questions are welcome.

* Latest version in FigShare: v2.  Differences from handouts uploaded to SC20 (v1):
  - Corrected "License, Citation, and Acknowledgements" slides in modules 02 and 05.

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

### Introduction

The hands-on exercises for this tutorial are based around a simple numerical model using the one-dimensional heat equation.  The example is described briefly in the repository's [README](https://github.com/betterscientificsoftware/hello-numerical-world-sc20#readme) file, and in greater detail in the ATPESC [Hands-On lesson](https://xsdk-project.github.io/MathPackagesTraining2020/lessons/hand_coded_heat/).  The ATPESC version focuses on the numerical aspects of the model.  But for the Better Scientific Software tutorial, we're focused on how to make the software better from a quality perspective, so **you don't need to understand the math to do these exercises**.

For the purposes of the BSSw hands-on exercises, you should imagine you've inherited an early version of the hello-numerical-world software from a colleague who's left the project, and you've been assigned to get it into better shape so that it can be used in the next [ATPESC](https://extremecomputingtraining.anl.gov/) summer school.

The repository you'll be working with is on GitHub: [betterscientificsoftware/hello-numerical-world-sc20](https://github.com/betterscientificsoftware/hello-numerical-world-sc20).
*Note: most of the screenshots will refer to the generic "hello-numerical-world" repository rather than the one specifically for this tutorial.*

### List of Hands-On Exercises
*Note that the exercise numbers align with the presentation modules.  Not every module has exercises (yet).*
* **[Exercise 0: Setting up the Prerequisites](handson-m00-prerequisites.md)**. Setup the accounts needed for these exercises.
* **[Exercise 2: Agile Methodologies](handson-m02-agile.md).**  You'll use GitHub issues and project boards to setup a simple "personal kanban" board.
* **[Exercise 3: Git Workflows](handson-m03-git-workflows.md).** You'll fork our hello-numerical-world repository, create a feature branch, and make a pull request
* **[Exercise 7a: Agile Redux](handson-m07a-agile-redux.md).**  You'll create epic, story, and task issues for the refactoring task and track them on a kanban board
* **[Exercise 7b: Refactoring Part 1](handson-m07b-refactoring1.md).**  You'll perform a small, well-defined refactoring exercise
* **[Exercise 7c: Refactoring Part 2](handson-m07c-refactoring2.md).**  You'll perform a a more open-ended refactoring exercise
* **[Exercise 8: Continuous Integration](handson-m08-continuous-integration.md).** You'll establish a simple continuous integration workflow and then refine it, adding code coverage assessment

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
  * [Agile Manifesto](http://agilemanifesto.org/)
  * [A-team tools for Agile practices](https://betterscientificsoftware.github.io/A-Team-Tools/)
  * [Policies: A Code of Conduct for Open Source Projects](https://www.contributor-covenant.org/)
  * Books
    * [The Agile Samurai: How Agile Masters Deliver Great Software, by Jonathan Rasmusson](https://www.amazon.com/dp/1934356581/ref=cm_sw_r_cp_ep_dp_ClBABbNGS7ZKS)
    * [Getting Things Done: The Art of Stress-Free Productivity, by David Allen](https://www.amazon.com/dp/0143126563/ref=cm_sw_r_cp_ep_dp_apBABbT2YZMMK)
    * [Code Complete: A Practical Handbook of Software Construction, by Steve McConnell](https://www.amazon.com/dp/0735619670/ref=cm_sw_r_cp_ep_dp_CkBABbXJWS8KV)
* Module 3: Git Workflows
  * [Atlassian/BitBucket (Comparing Workflows)](https://www.atlassian.com/git/tutorials/comparing-workflows)
  * [Git Flow (Driessen's Original Blog)](https://nvie.com/posts/a-successful-git-branching-model/)
      * [Git extensions](https://github.com/nvie/gitflow)
  * [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)
  * [GitLab Flow](https://docs.gitlab.com/ee/workflow/gitlab_flow.html)
* Module 4: Software Design
  * [Related Article](https://link.springer.com/chapter/10.1007/978-3-319-27308-2_19)
* Module 5: Software Testing 1
  * Tutorials for code coverage: [Online Tutorial](https://github.com/amklinv/morpheus), [Another example](https://github.com/jrdoneal/infrastructure)
  * [Useful How-to resources on test and test suites on ideas-productivity.org](https://ideas-productivity.org/resources/howtos/)
* Module 6: Software Testing 2
  * [Related Articles:1](https://ieeexplore.ieee.org/abstract/document/8449015),[2](https://onlinelibrary.wiley.com/doi/abs/10.1002/spe.2220)
* Module 7: Refactoring
  * [heatAll.C](https://github.com/betterscientificsoftware/hello-numerical-world-atpesc-2020)
  * [AMReX](https://amrex-codes.github.io/amrex/science.html)
  * [Related Article](https://link.springer.com/article/10.1007/s42979-020-0077-x)
* Module 8: Continuous Integration
  * [Exascale Computing Project CI documentation](https://ecp-ci.gitlab.io/)
  * [Travis CI service](https://travis-ci.com)
  * [Codecov service](https://codecov.io)
* Module 9: Reproducibility
  * [Floating Point Analysis Tools](http://fpanalysistools.org/)
  * [Code Ocean (Cloud platforms - publish and reproduce research code and data)](https://codeocean.com/)
  * DOIs and hosting of data, code, documents:
     * [Zenodo](https://zenodo.org/)
     * [FigShare](https://figshare.com/)
  * [National Science Foundation Data Management Plan Requirements](https://www.nsf.gov/bfa/dias/policy/dmp.jsp)
  * [SC20 Transparency and Reproducibility Initiative](https://sc20.supercomputing.org/submit/transparency-reproducibility-initiative/)
  * [ACM Transactions on Mathematical Software (TOMS)](http://toms.acm.org/replicated-computational-results.cfm)
  * [ACM Artifact Review and Badging](https://www.acm.org/publications/policies/artifact-review-and-badging-current)
  * [ National Information Standards Organization (NISO) on Reproducibility and Badging](https://www.niso.org/niso-io/2019/01/new-niso-project-badging-scheme-reproducibility-computational-and-computing)
  * [The FAIR Guiding Principles for Scientific Data Management and Stewardship. Mark D. Wilkinson, et al. 2016](https://doi.org/10.1038/sdata.2016.18)
  * [Editorial: ACM TOMS Replicated Computational Results Initiative. Michael A. Heroux. 2015](http://dx.doi.org/10.1145/2743015)
  * [Simple experiments in reproducibility and technical trust by Mike Heroux and students (work in progress)](https://betterscientificsoftware.github.io/Trust-Tools/)
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
