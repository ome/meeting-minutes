Attending: Josh, Seb, Jason, Dominik, June, Mark, Wilma, Petr, Frances,

J-m, Will, Melissa, David, Emil

Start: 2:00 pm

1. Accepting minutes from [<u>last meeting</u>](https://drive.google.com/open?id=0B9Xg53EhqUycZEVHclBwRHNFRGM)
--------------------------------------------------------------------------------------------------------------

2. Project Status
-----------------

(2-3 minutes each)

-   IDR

    -   Prod87 released

    -   Running out of space. Need a few hundred TBs (S3 isn’t backed
        > up)

-   NGFF

    -   Colors PR open using spare-array (rather than dictionary) -
        > discussion ongoing

    -   Array investigation: differences in tuple-of-objects handling
        > between n5 and zarr

        -   Looked at storing look-up table

    -   S3 fun (CORS needed to allow browser to access data)

        -   May need to add our own proxy server

    -   QuPath export

        -   Testing export to zarr with downsampling

    -   Use cases: Single cell call (WSSS),

-   OMERO 5

    -   Deep copy seems to work so far so it is now included with other
        > PRs on merge-ci.

        -   As with Duplicate since OMERO 5.2.1 the current group
            > context needs to be that of the data being duplicated,
            > noted as [<u>blitz
            > \#103</u>](https://github.com/ome/omero-blitz/issues/103).
            > With [<u>CLI
            > plugin</u>](https://pypi.org/project/omero-cli-duplicate/)
            > can use -g option.

        -   Keeps MIFs together for now, [<u>wider
            > discussion</u>](https://github.com/ome/design/issues/107)
            > ongoing.

    -   Timetable for next release of blitz (and omero.server)? Etc.

        -   Mark: duplicate is pretty flexible - how to expose it in UI
            > in usable form?

        -   JM: Many users will be able to use the CLI initially. Can
            > release without webclient.

        -   Josh: any CLI changes to make it more usable?

            -   Petr: group context - need to know up front

            -   Josh: what about copy/link annotations options?

            -   Petr: maybe too much freedom for regular users. Admins
                > may not want their users to do too much.

            -   But feature is working OK as it is.

        -   Mark: annotation linking options for different workflows -
            > e.g. publish (in different group)

        -   Release will be 5.6.3

-   SA. -

    -   JRS: status of SLS-IT

-   Glencoe - Emil:

    -   TileDB - bioformats2raw.

    -   Update image region microservice to support masks/labels

-   Community

    -   doc/guides discussion on Thursday 1-2pm UK - submodules etc. See
        > [<u>Options
        > considered</u>](https://github.com/ome/omero-guides/pull/23)

    -   File formats in the community (Seb):

        -   OME-TIFF. Tiff creation in python. ‘Big Fish’ fails (too
            > big)

        -   OME-TIFF writing in C++ - needs investment to do this right.

3. AOB
------

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

Dundee: Please submit OSAR forms by due dates

4. Main Topic
-------------

(20-25 minutes plus 15 minutes questions max)
