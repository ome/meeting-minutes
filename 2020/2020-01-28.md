Dundee: N/A

Remote: Frances, Josh, Mark, Simon, David,  
June, Dom, Chris, Liza, Melissa,  
Ola, Kevin, Andreas, Jason, Will, Emil

Start: 2:00 pm

1. Accepting minutes from [<u>last meeting</u>](https://drive.google.com/open?id=1TndXeC3wQSZVEaB5ZGpEAaPRl1QAufSI)
-------------------------------------------------------------------------------------------------------------------

2. Project Status
-----------------

(2-3 minutes each)

-   IDR

    -   Idr0056: Currently importing into idr-next (prod74; not to be
        > released)

        -   May be finished before downtime

    -   Idr0073: Images converted to ome.tiff and imported into
        > idr-testing

        -   Large png files, converted to OME-TIFF with Glencoe tools
            > (+1)

        -   Imported to idr-testing; FW thumbs up

    -   Migration

        -   Second rsync is done. Re-running playbooks.

        -   Hopefully can test later this week. (Frances can start
            > early)

-   Next release - 14:04

    -   Mark: reviews all look successful. Building a RC soon.

    -   Josh: Petr to check/approve new features
        > (sessions/open\_tables/…)

    -   Scheduling a next milestone

-   SA (learning/mail)

    -   Deployments

        -   Demo (Mark): omero-signup has an issue (playbook is ready)

            -   TypeError: context must be a dict rather than
                > RequestContext.

            -   [<u>https://github.com/ome/prod-playbooks/pull/229</u>](https://github.com/ome/prod-playbooks/pull/229)

        -   Nightshade (Simon): needs webtagging released. Wed?

        -   Learning (Mark): done

    -   JRS: CB PIs + JD & Chris S.

        -   GPFS/licensing request is being worked on

-   Glencoe - 14:18

    -   See above re: sessions PRs

    -   Few Bio-Formats things coming

    -   Starting to reach the need for capacity management

        -   JRS: sharing scaling experiences? (e.g. Large-Z)

            -   CA: access to some should be feasible

            -   Approx. 100s of GB per TIFF

        -   CA: UI/UX easy doesn’t always map to scalable

            -   E.g. “all channels on”

-   Community

    -   J-m/Petr on the road; Will leaving…

    -   Trip to Freiburg upcoming as well.

    -   Challenge of responding to ongoing requests/invites

    -   Wellcome visit! (Thanks all around)

    -   Sharing around tasks to help cover off-time and community items,
        > etc.

    -   OME Meeting

        -   No feedback (yet)

        -   JRS to write down few themes and pass it around

        -   GS likely to attend in various ways

3. AOB
------

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

-   Calendaring - 14:31

    -   Challenge: concerted effort at UoD to adopt Outlook workflows

        -   School admins are using concerted calendaring for room
            > scheduling, etc.

    -   Josh: No group-based solutions

    -   JRS: Download (free) applications if you don’t want to use the
        > web (No Linux version)

    -   June: OME Scheduling is now working

    -   JRS: ok. Need to discuss. Please don’t delete the invites.

    -   Josh/Mark: Windows licenses - JRS: site licensed

        -   CA: “have Windows be your primary operating system, use
            > Linux in a VM”

        -   JRS: Chris Scott was willing to work with computationalists.
            > Let’s propose.

4. Main Topic
-------------

(20-25 minutes plus 15 minutes questions max)

Done: 14:48
