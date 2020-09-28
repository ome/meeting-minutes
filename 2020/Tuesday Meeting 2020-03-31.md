Attending: Will, Petr, Frances, Mark, Simon, Dominik, Melissa, Kevin,
Wilma, Ola, June, David, Chris, Josh, Jason, Jean-Marie,

Start: 2:00 pm

1. Accepting minutes from [<u>last meeting</u>](https://drive.google.com/open?id=0B9Xg53EhqUycZEVHclBwRHNFRGM)
--------------------------------------------------------------------------------------------------------------

2. Project Status
-----------------

(2-3 minutes each)

-   IDR:

    -   Next release idr0064.

    -   Expecting update this week for migration progress. Hopefully
        > back up next week.

-   OMERO 5.6.1

    -   Released last Wednesday as planned. Production servers upgraded.

    -   Might have [<u>broken password
        > reset</u>](https://forum.image.sc/t/35701) in fixing 2019-SV3.

    -   Simon: add integration tests - Josh: add manual test to release
        > board in the meantime

    -   5.5.9 Insight via Fiji can’t connect to demo?

-   SA (learning/mail)

    -   Simon: Propose a new Outlook group as the official UoD IT
        > contact info for OME servers.

        -   Add sysadmin UoD users

-   Glencoe:

    -   Upgrading users - Few fixes for Django upgrade.

-   Community

    -   Josh / NGFF (next gen file formats) conversations

        -   Chat with Caterina / OWL extensions - find better
            > community-driven name (not just 4DN)

        -   Chat EMBL / platform discussion - linking tabular data to
            > image (cf parade)

        -   Monthly
            > [<u>http://www.researchobject.org</u>](http://www.researchobject.org)
            > call (“datasets & workflows”)

            -   Tie various files together - e.g. 2x csv or pdf/jpg etc.

            -   J-M: we have been in contact with C. Goble following
                > EOSC AGM, to follow up. Call 4th Thursday of every
                > month. 8pm UK

        -   Zarr/napari and spatial

            -   Nick has spatial-image on github

            -   Coordinates standardization. N dim, units etc.

            -   Jason: common coordinates system.

    -   Jason:

        -   NIH-HCA Meeting - 270 on a zoom call!

            -   Standards, standards,...

            -   [<u>CEDAR</u>](https://metadatacenter.org/)

            -   Useful example of remote meeting

        -   OME (Virtual) Community Meeting

            -   Zoom Capacity (c.f., NIH-HCA meeting)

            -   Registration Workflow

3. AOB
------

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

-   Dundee: OME leave over Easter, April 10 thru 13.🎉🎉🎉

    -   Let June know if you’re taking these off (assume yes).

4. Main Topic
-------------

(20-25 minutes plus 15 minutes questions max)

-   Planning next batch of work:

    -   New doc on work for next 2 months.

    -   New microservice endpoints for download of binary data. 2D or
        > nD. Chunked API

        -   Cf Zarr / Tiff / HDF5 - loading data directly via
            > Bio-Formats

        -   Useful for BIA

        -   Petr: omero-downloader? Josh: that’s part of the solution.
            > Tiffs cached or read on the fly.

        -   Petr: download of original files? Josh - not part of this
            > discussion.

            -   But there are benefits of storing data in an open format

            -   Jason: going full-circle (OMERO 4 converted data into
                > common Pixels data)

        -   Simon: zarr has remote APIs? Josh: yes http, etc.

        -   Chris: explored microservices reading from managed-repo
            > directly.

            -   Future solution will likely be something ‘new’ (not
                > added to OMERO api)

        -   Jason: need this for IDR. Data out and data in - higher
            > throughput.
