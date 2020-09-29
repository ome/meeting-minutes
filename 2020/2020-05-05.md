Attending: Petr, Josh, J-m, Seb, Dom, Frances, Simon, Mark, Jason, Liza,
Kevin, Wilma, David, Melissa

Andreas, Will (notes), Chris

Start: 2:00 pm

1. Accepting minutes from [<u>last meeting</u>](https://drive.google.com/open?id=0B9Xg53EhqUycZEVHclBwRHNFRGM)
--------------------------------------------------------------------------------------------------------------

2. Project Status
-----------------

(2-3 minutes each)

-   IDR - 14:01 UK

    -   idr0083 released

        -   Jason quoted in the UK’s biggest paid-for newspaper!

            -   Funders pleased with publicity

    -   Next release (prod82):

        -   IDR BioFormats updated (non-breaking change), PostgreSQL
            > updated to 11

        -   OMERO.server 5.6.1 upgrade reverted again due to BFMemo
            > files being regenerated

            -   JRS: announce but rollback? Unclear.

            -   Comment in Image.sc + add to history for future doc
                > releases

            -   JM: is there future work to prevent invalidation? No but
                > Glencoe have tools and workflows for regenerating
                > files

        -   New datasets: idr0079 and idr0081

-   IO

    -   Positive reception of all the work re: idr0083 release (Twitter,
        > multiple chatrooms, image.sc)

        -   Feedback regarding the CLI usage

    -   Next steps

        -   General cleanup of code (migration, renamings, tagging, etc)

        -   Write up about the enabled workflows
            > ([<u>draft</u>](https://docs.google.com/document/d/1p2yuZVphyb9oGzUuECQOSiCmYlluK3qICZaLk8-kDXM/edit#heading=h.48a79sdg42iw))

        -   Introduction of more metadata into the zarr datasets

            -   Aim: avoid needing to login to OMERO

            -   OME-XML

            -   OMERO

            -   IDR, etc.

            -   Rendering information in a JSON file

        -   BF Zarr reader/writer PR available for testing

        -   Large KLB file has been converted but no clients can handle
            > it at the moment

        -   Backblaze has an updated S3 compatible API. Glencoe has
            > experience with this as well as Digital Ocean Object
            > Store. Along with Cloud&lt;something&gt; for CDN(?) money
            > may be available for testing.

            -   Glencoe will assist with initial testing so numbers are
                > available in time for the OME Community Meeting

    -   Proposed another demo: **Friday afternoon** (@Josh to send
        > invite)

-   SA (learning/mail)

    -   Meeting about mailing lists after this meeting

-   Glencoe

    -   OSS team feedback on ROI tools for QuPath

    -   Updating conversion tools

    -   Looking at how existing microservices will interact with new
        > Zarr format

    -   Looking into jxrlib jars and extra dependencies

-   Community

    -   iRODS call (Josh):

        -   working on OMERO → iRODS synchronization for Michelle Itano.
            > (“we like interface”)

        -   iRODS → OMERO is on hold.

        -   Doing this via
            > [<u>https://debezium.io</u>](https://debezium.io)

            -   Allows clients to watch a database such as PostgreSQL
                > for changes and respond, e.g. automatically update
                > Elasticsearch

        -   Reported on RIKEN event and zarr/s3 work. No feedback.

        -   UGM is 9-11 June and open for free registration.

    -   OME Community Meeting

        -   82 Registrants currently

        -   Everyone should register as Zoom links to join are unique!
            > [<u>https://docs.google.com/forms/d/1ZOl1wa\_oe5Pm4ho2co05ZD3otXpGY\_3hPaFxnlvGyiQ</u>](https://docs.google.com/forms/d/1ZOl1wa_oe5Pm4ho2co05ZD3otXpGY_3hPaFxnlvGyiQ)

        -   Speakers confirmed

        -   Additional Talks?

            -   UMass

            -   iRODS?

        -   Video recording and hosting

            -   [<u>Walkthrough for lightning talks OME 2020 capture
                > software
                > (OBS)</u>](https://docs.google.com/document/d/1y45N7aWzN9SR8fn1K_3kRMYPWiWJgmFlW2hXFcB9sVE/edit)

<!-- -->

-   Windows testers ?

    -   One test using Win7 laptop (and one on Mac OS) done by Petr -
        > success

-   Need to figure out how to record talks. Nearly all talks will be
    > pre-recorded in advance to avoid time-zone issues. Includes
    > planned invited talks and lightning talks.

    -   Keynotes, OME and GS updates will be live

-   Publication platform? Youtube? Vimeo? OME website? Multiple?

    -   OME website for now

    -   After the meeting will consider publishing it elsewhere

-   Pre-registrants only to deter trolling or abuse

3. AOB
------

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

-   

4. Main Topic
-------------

(20-25 minutes plus 15 minutes questions max)
