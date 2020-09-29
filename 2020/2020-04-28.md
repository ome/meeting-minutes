Attending: Petr, Jean-Marie, Mark, Dominik, Seb, Frances, June, Josh,
Liza, David, Will, Melissa, (12)

> Wilma, Jason, Kevin, Andreas, Emil, Simon, Chris, Ola (14:10)

Start: 2:00 pm

1. Accepting minutes from [<u>last meeting</u>](https://drive.google.com/open?id=0B9Xg53EhqUycZEVHclBwRHNFRGM)
--------------------------------------------------------------------------------------------------------------

No objections

2. Project Status
-----------------

(2-3 minutes each)

-   IDR

    -   Frances: released two datasets idr0064 (compound screen) and
        > idr0083 (first COVID dataset). Already working on next release

    -   Simon: OMERO 5.6.1 upgrade causes IDR to fall over.

        -   [<u>https://github.com/ome/omero-server/issues/93</u>](https://github.com/ome/omero-server/issues/93)

        -   Have not been able to reproduce so far. Used idr0044 to
            > reproduce

        -   Josh: setId call includes DB check. Turns into large queries
            > for images with many files. Might need to reproduce with
            > large DB + large filesets

        -   Possible for the issue to show up in the case of HCS data

        -   Mark: adding a DB index still took ages. Need environment to
            > reproduce

        -   Jason: possible to reproduce in Dundee production server?

        -   Chris: more details on the query in the public issue would
            > help getting involved

-   IO

    -   Josh: demo happened on Friday (video available on request).

        -   Thanks to Chris for being the remote demoer

        -   List of known limitations, questions and next steps

        -   Next step is to scale up. Increase the amount of data pulled
            > by visualization + cluster analysis against HCS data on S3

            -   Idr0044 (McDole et al. dataset) for large lightsheet
                > dataset

        -   Email with EBI cloud system is that current S3 is production
            > but will be shut down after June. Need to handle the
            > migration ourselves

            -   Potentially 500TB. Less than 70TB in Dundee so not
                > possible to maintain a full copy

            -   SImon: could free more space in UoD (\~100TB). Need to
                > be careful about file handles

            -   Simon: Planning to have second layout in EBI anyways.
                > Treat v0.1 as volatile? Main caveat is if people start
                > consuming the first endpoint

            -   Overlap between cloud deployments? Yes should be \~ one
                > month

        -   Jason: is 500TB sufficient? Josh ideally would need 3-4
            > times that

        -   URL?

            -   Not migrating it. Endpoint staying at
                > s3.embassy.ac.uk/idr/

-   SA (learning/mail) - 14:24 UK

    -   Mailing list decisions.

        -   Mark: Need to know more about what Google offers?

        -   How wants to be in the discussion? Send calendar invite to
            > everyone and let people decline if not needed

        -   Also tackle the ability to create mailing lists as part of
            > the meeting

    -   CentOS 8 repos. Preliminary work on Ice.

-   Glencoe

    -   Chris: supporting conversion work. Getting ready for first OMERO
        > 5.6.1 customer upgrade.

-   Community

    -   Community meeting

        -   Jason: link to registration form is in standup. Also trying
            > to include link to the program

        -   Website updated with work from Liza + Petr

        -   Getting ready to record invited speakers.

        -   J-M: preparation work? Jason: two types: oral
            > presentations + workshops

    -   Trying to coordinate press releases for idr0083

        -   Aim to have own press release one day after the one from
            > Maastricht.

        -   Then start the OME/IDR social media work (image.sc,
            > twitter…)

3. AOB
------

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

4. Main Topic
-------------

(20-25 minutes plus 15 minutes questions max)
