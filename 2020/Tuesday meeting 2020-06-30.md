Attending: Petr, Seb, Frances, Mark, Jean-Marie, Simon, Josh, Dominik,
June, David, Melissa, Kevin, Jason, Will

Start: 2:00 pm

1. Accepting minutes from [<u>last meeting</u>](https://drive.google.com/open?id=0B9Xg53EhqUycZEVHclBwRHNFRGM)
--------------------------------------------------------------------------------------------------------------

2. Project Status
-----------------

(2-3 minutes each)

-   IDR

    -   Frances: released Prod84 this morning with 3 developmental
        > biology studies (idr0070/HDBR atlas, idr0077/flower
        > development via SPIM, idr0079/3D confocal imaging in
        > zebrafish)

    -   Josh: publication as zarr? (Holding off on masks. See below)

        -   Seb: interested in idr0077 (multi-angle SPIM - something we
            > might come back to in the future)

        -   Ease of distributing the work. Main issue is related to
            > ManagedRepository vs client path.

        -   Jason: need a decision soon? Not particularly, wanted to
            > have the discussion as the datasets are published.

        -   Simon: also question of next specification, i.e. will need
            > to

            -   JRS: good to test the migration strategy

        -   Tl;dr -- no objections but no requirement to release
            > simultaneously

        -   Simon: can submitters *expect* there to be a zarr? No.

            -   JRS: let’s not raise the bar on what it takes to release
                > a dataset

            -   Josh: doing only a subset might help reducing these
                > expectations

            -   JRS: zarr is currently something we do on the *OME*
                > side.

            -   Chris: community doesn’t understand that. OME == IDR

                -   Also fanfare on image.sc. Might already be the
                    > expectation.

                -   Stating the intention?

            -   JRS: all in good time.

            -   Seb: like the download (aspera) page

            -   Chris: “*some* datasets are available from Zarr”

            -   JRS: service provision is evolving.

            -   Mark: S3 storage? Josh: new minimal date is September

    -   Jason: huge achievement

-   NGFF

    -   Bug in stack (s3fs/fsspec/dask) when arrays are sparse

        -   Restrictive S3 server. Missing chunk -&gt; access dies.

        -   Probably a classical issue with masks

    -   Three mask options:

        -   Labelled image **but** doesn’t support overlaps.

        -   6D booleans **but** 8x storage (Better as probability mask)

        -   One array per mask **but** 8x storage and lots of groups

    -   Overlapping

        -   Simon: first idr study with masks was overlapping

        -   Emil: case of multiple segmentation with varying parameters

        -   Storing each “segmentation” as a separate group?

            -   Simon: need to deal with multiple groups in all cases?

            -   Josh: question of the distribution of masks into these
                > groups. Avoid 150K groups

            -   Chris: hard to prevent people from making bad data
                > management decisions

        -   Summary: smallish number of non-overlapping labelled images

            -   Chris: semantics of the group up to the user

    -   Simon: metadata?

        -   Next question alongside multiscale

-   SA (learning/mail)

    -   Mark: Tomorrow morning we switch to having Google handle
        > incoming OME mail.

        -   Report any weirdnesses asap.

        -   Will: Instructions for standup prep? To be reviewed for
            > Thursday

        -   

-   Glencoe

    -   Looking at using imglib2 for bioformats2raw etc. Avoids the
        > math.

    -   Can then start heavily on the thumbnail front.

    -   Investigating various S3 implementations with customers. What’s
        > in the wild.

-   Community

    -   JRS: people asking about how OME2020 was done.

        -   How were videos done.

        -   Breakouts for fun.

3. AOB
------

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

4. Main Topic
-------------

(20-25 minutes plus 15 minutes questions max)
