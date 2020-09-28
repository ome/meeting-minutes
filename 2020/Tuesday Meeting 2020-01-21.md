Dundee: Will, Petr, Mark, Dominik, Jean-Marie, Simon, Jason, June,

Remote: Josh, Ola, David, Wilma, Frances, Andreas, Chris, Liza, Melissa,

Start: 2:00 pm

1. Accepting minutes from [<u>last meeting</u>](https://drive.google.com/open?id=1TndXeC3wQSZVEaB5ZGpEAaPRl1QAufSI)
-------------------------------------------------------------------------------------------------------------------

2. Project Status
-----------------

(2-3 minutes each)

-   IDR

    -   [<u>IDR Flex reader
        > bug</u>](https://idr-redmine.openmicroscopy.org/issues/116#note-29)
        > affecting idr0072 and apparently idr0001: Is this tracked
        > somewhere? It’s on David’s radar. Maybe could add an issue,
        > trello card, etc?

        -   Some plates are working, some not. The ‘unsupported’ plates
            > have some format variant.

        -   David: will update redmine and create github issue.

        -   No extra ‘hidden’ fixes from Glencoe

        -   Josh: 2 variants of the format -&gt; 2 readers eventually?

            -   Maybe in future we just convert to n5

            -   In some cases need to walk up a directory.

        -   Jason: what is David’s recommendation for short-term vv
            > long-term fix?

            -   David: will consider

        -   JM: don’t want divergence between idr and regular
            > Bio-Formats

    -   Simon: Migration: manual VMWare install - too costly to
        > learn/use API in short term.

        -   Hopefully setup VMWare by end of the week.

    -   Josh: B-F work may prompt a new idr release

-   Next Release

    -   timing of IDR upgrade with provider downtime, end of Feb (or
        > early March at latest)

    -   Prod80 may use rc-release ahead of full release

    -   Josh: ordering of web releases. E.g. use json file to define
        > dependencies.

    -   Chris: want to know whether server release has particular
        > jar/fix.

        -   E.g. where is the 5.6.0 tag?

        -   Josh: etc properties is the artifact source

        -   More discipline in changelogs might be enough - no need for
            > script/json etc

    -   Chris: asking for no B-F changes that would need memo file
        > regeneration

-   SA (learning/mail)

-   Glencoe

    -   Several PRs opened this morning from backlog.

        -   Some PRs depend on each other. E.g. romio and sever.

        -   Need to consider ordering when merging

    -   Python: back-porting 5.4.0 fixes to 5.6 is not too painful - in
        > progress.

    -   Setting up microservices to e.g. update memo files on 2nd binary
        > repo with no downtime.

-   Community

    -   JM & Petr to Montpellier next week.

    -   JM working on mybinder, linked to omero guides. CellProfiler
        > running in python 2.

        -   Better visibility of notebooks with idr data (improvement
            > over ITR).

    -   Jason: would like to show some of this in presentations soon.

    -   Jason: rename “OME Users meeting” to “OME Community meeting”?

        -   Program preparation - by mid Feb

        -   Maybe do ‘all day workshop’?

3. AOB
------

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

Jason: OSARs!

4. Main Topic
-------------

(20-25 minutes plus 15 minutes questions max)
