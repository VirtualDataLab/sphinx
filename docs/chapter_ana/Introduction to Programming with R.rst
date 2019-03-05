Introduction to Programming with R
##################################

Perhaps the question I am confronted with most when teaching statistics courses to psychology undergrads is "Why should I need this, when I become a therapist"? That's a difficult one to answer in a single sentence, but I will give it a try, nonetheless: "Because everything we know in psychology - and the social sciences in general - is connected to empirical data". Well, it was a first try. As the previous sections of this volume have shown you, in scientific psychology we strive to test our claims using data. Testing our claims (ideally) leads to appropriate theories becoming successful and inappropriate theories being discarded. When you are working with patients or clients, would you not rather use techniques that have been proven to be successful in reducing negative symptoms?

Even more baffling to many of you, now reading these words, is the idea of learning a programming language like R in the first year of studying psychology. But the same reasons for learning statistics in general apply to learning R. To move from observations to conclusions requires multiple steps: encoding observations in data, organizing data, describing data, and testing hypotheses using data. The previous section showed you how to collect data in experimental settings using Python. In this and the following sections we will try to turn the data we gathered into conclusions about our hypotheses by using R - a multi-purpose tool that can be used for almost anything data-related.


Why R?
******

Many blogs are filled with heaps of reasons to use R over other software that was traditionally more prominent in the behavioral and social sciences. Here's a rundown of the "best of":

1. It's free

This is the obvious one: R costs you nothing to obtain or use. A lot of other software for data analysis requires you to either buy a specific version or rent a yearly license. R, on the other hand, you can simply download, install, and use. R is developed and maintained by `non-profit foundation<https://www.r-project.org/foundation/>`_, meaning it is free of commercial interests.

2. It's free

Yes, I've said this already, but this time it has a different meaning. This "free" pertains to the `definition of free software as proposed by GNU<https://www.gnu.org/philosophy/free-sw.en.html>`_, which can be boiled down to the phrase "the users have the freedom to run, copy, distribute, study, change and improve the software". This means that R is an open source software and this applies not only to the R-core itself, but also to the packages, which you can obtain via the official repository. This allows everyone to see what is actually happening - e.g. which formulas are used to compute statistics - and catch mistakes in the software before you publish research that is flawed (see :cite:`Eklund2016` for what may happen, when software is not open for such checks).

3. Researchers develop their tools in R and make them available as R packages

One important aspect of doing research is using the correct tools. Correct is often understood to simply mean "not wrong", but in science there is a lot of nuance to "not wrong". Some approaches may simply become outdated, because newer alternatives are available or because someone has developed an adapted version which is better suited for your specific case. Currently, many new methodological developments are implemented as R packages and made available for anyone to use. Commercial software is often slower to react, because there is not enough demand for the approach you might need, in order to implement it into a specific software. Thus, R is a more direct channel to current developments in analysis tools. To be able to use newly developed analysis tools comes with a few caveats, of course, because you lose the vetting process performed by commercial providers.

4. You can develop your own approach and implement it in R

A lot of software is limited to what has been implemented by the developers. This is where R can really shine, because it allows you to implement whatever analysis you want, as long as you are able to formulate it in the R language. Because the most basic building blocks of R are simply mathematical operations and relations there is almost no limit to what you can implement. Be aware, that this does not mean that R is the best tool to implement whatever it is, you're trying to implement; it simply means it is a tool that makes it possible at least.

5. The community

There are hundreds of resources and websites containing tutorials, guides, comparisons of approaches, and assistance. Of course, R comes with help-files and examples and there is `an extensive list of FAQs<https://cran.r-project.org/doc/FAQ/R-FAQ.html>`_, but as is the case with most programming languages, the premier resource for specific questions is `stack overflow<https://stackoverflow.com/>`_. As I am writing this, there are currently 278380 questions tagged "R" on stack overflow, most of them with well-meaning, detailed responses.

But before we can get to experts' opinions on stack overflow, there are some additional resources you can check, if the presentation in this volume leaves you with open questions. Maybe one of the websites that is visited most often in the early stages of learning R is the `Quick-R website by DataCamp<https://www.statmethods.net/>`_, where you will get quick glance answers to some of the early questions in an alternative way to our presentation here. Another way you may want to try to learn the first steps of R is through online courses like `Harvard's "Statistics and R"<https://online-learning.harvard.edu/course/statistics-and-r>`_ or `DataCamp's interactive "Introduction to R"<https://www.datacamp.com/courses/free-introduction-to-r>`_. There are also a lot of other courses out there, most of which are not free, however. Our hope is, of course, that you will be in no need for such resources once you are done with this and the following sections, but it cannot hurt, to have alternatives.

6. Everyone uses it

As, no doubt, your parents have told you on multiple occasions, this is perhaps the single worst argument on the planet to do something: "Would you jump off a bridge, if your friends did it?" Well, in this case, you might want to, because one of the core necessities for open and reproducible science is communicating your work. Not just results and conclusions, but also how you got there. As I stated above, R can be used for basically all steps between assessing data and producing manuscripts and if others use it, it may be necessary for you to be able to read what they wrote, to gain an understanding of how they structured, analyzed, and visualized their data. On the other hand, writing R code also allows other people to retrace the steps you took, because many people can read it. In 2017, Python and R were among the fastest growing programming languages - measured by the number of Stackoverflow views of questions tagged for either one of those languages (:cite:`Robinson2017a`, :cite:`Robinson2017b`). On `Bob Muenchen's Website r4stats<http://r4stats.com/>`_ you will find a continuously updated Article with current numbers on the popularity of R (:cite:`Muenchen2019`), where it is among the most sought after skills in job descriptions and the second most common software cited in scientific articles.


Gathering your tools
********************

Enough chit-chat about the benefits of R - chances are, that if you are still reading at this point, I do not need to convince you any further to use it. So, let us begin by gathering the necessary materials:


The R-Core
==========

The best way to get R is to simply grab it directly from its provider. R itself and most utensils you can add on to it are gathered in what is called CRAN (Comprehensive R Archive Network). For some nice 90s nostalgia you can visit the `CRAN website<https://cran.r-project.org/>`_ directly, but we also provide short descriptions of how to `Install R on Windows`_, `Install R on Mac OS X`_, and `Install R on Ubuntu`_ below. And for those of you who do not want to run the risk of R withdrawal symptoms: `here's a link to a short description of how to install it on an Android device<https://selbydavid.com/2017/12/29/r-android/>`_.

Install R on Windows
--------------------

Installing R on Windows machines is pretty straightforward. The CRAN Website provides you with an executable for the installation of the latest stable R Version, which you can `download here<https://cran.r-project.org/bin/windows/base/release.htm>`_. The only thing you have to keep in mind is that R does not perform automatic updates. That's where it becomes a bit tricky: it is advisable to check for a new R version every now and again - a good estimate going by `the R version history<https://cran.r-project.org/bin/windows/base/old/>`_ is every three months. To update R it is recommended to install a new R version alongside your current version, just in case the new R version broke something that worked before. For some more details on this procedure (and many others), feel free to check the `R for Windows FAQ<https://cran.r-project.org/bin/windows/base/rw-FAQ.html>`_


Install R on Mac OS X
---------------------

Current versions of R are only available for OS X 10.11 (El Capitan) and above. Since this OS is now five years old, the newer versions should cover most users, but if you are among those running an older version of OS X, you will need to install either R Version 3.3.3 (OS X 10.9 and 10.10) or R Version 3.2.1 (OS X 10.6 to 10.8). All three versions can be `found here<https://cran.r-project.org/bin/macosx/>`_.

Prior to installing R on OS X 10.8 or above, you will need to install XQuartz. Simply `download the dmg-file from the XQuartz-Website<https://www.xquartz.org/>`_ and follow the instructions provided in the installer. Afterwards, please restart your computer, before installing R.

To install R after having installed XQuartz, again simply download the `installer provided by CRAN<https://cran.r-project.org/bin/macosx/>`_ and run it. Should you be asked to install XCode during this process, please do so. As was the case with R for Windows, R does not perform automatic updates, so you should check for a new version every three months or so.

Install R on Ubuntu
-------------------

R is can be installed from the repositories for many Linux distributions. We will cover the case for Ubuntu here, but you can find an online tutorial for installing R on RedHat on `this blog<https://blog.sellorm.com/2017/11/11/basic-installation-of-r-on-redhat-linux-7/>`_, for example.

To install R on a Ubuntu machine, you will need sudo-permissions. Because R is part of the Ubuntu repositories, you can simply install it via::

  sudo apt install r-base

However, this will provide you with an outdated version of R in most cases. To obtain the new version of R (and have it update automatically), there are some additional hoops. First, you need to add the necessary GPG key::

  sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9

Then, you need to add the R repository to your sources list. Depending on the Ubuntu release you are running, this may look like this::

  sudo add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/'

if you are running Bionic Beaver, or like this::

  sudo add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu cosmic-cran35/'

if you are running Cosmic Cuttlefish. If you are running a different release, simply replace the :code:`bionic` or :code:`cosmic` by the name of your version.

Because this changes the :code:`/etc/apt/sources.list` file, you will need to::

  sudo apt update

which may take a few seconds. Afterwards, you can install R using::

  sudo apt install r-base

which should provide you with the current version. In contrast to installing R on Windows or OS X, this will provide you with automatic updates for R.

References
**********

.. bibliography::

  references.bib
