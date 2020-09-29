---
title: Tuesday meeting 2020-09-29
---

[![hackmd-github-sync-badge](https://hackmd.io/vyMSnzwMTTmfKWEQkgS9gg/badge)](https://hackmd.io/vyMSnzwMTTmfKWEQkgS9gg)


Attending: Will, Seb, Petr, David, Jason, June, Wilma, Frances, Dominik, Simon, Josh, Mark, Kevin, Jean-Marie, Erin, Melissa, Chris, Andreas, Emil, Ola

Start: 2:00 pm UK

## Accepting minutes from [<u>last meeting</u>](https://github.com/ome/meeting-minutes)

Accepted

## Project Status

(2-3 minutes each)

- IDR
  - prod88 released!
    - 3 studies idr0076, idr0078, idr0089.
    - Mapr may require some refactoring soon as it's taking over 10 minutes to refresh
      - Simon: Potentially reached the 6 month expiry. Going to continue to be an issue.
      - Seb: assume a discussion on Monday, but can we get stats? Value of UI?
      - Will: most studies - all images are same organism.
    - Next release - idr0094 only, will be a quick release. Don't need to fix mapr before then
    - Chris: we also find that this approach doesn't work with large-scale datasets. Solutions will benefit many.

- NGFF (Josh)
  - No feedback on [label issue](https://github.com/ome/ome-zarr-py/issues/49). Moving to image.sc if no vetos.
  - Investigation on dimension names. Multiscale is not compatible with xarray. All dimensions must be same size - not true for pyramids.
  - Polygon discussion with Glencoe. Short version: [WKT](https://en.wikipedia.org/wiki/Well-known_text_representation_of_geometry)
      - Need spec beyond OME-XML. For usage in JSON.
      - JM: Look at GeoJSON? Same 'spirit' if not exactly same. Used by QuPath.
      - Chris: GeoJSON uses 'world' context.
      - Josh: want OMERO.web to be able to load ROIs from different sources
  - Sending out community email. (Feedback on image.sc)
      - Many signed-up at OME 2020.
  - Ramping up. (See main topic below)
  - Jason: we are getting requirements from everywhere

- OMERO 5
  - Black autoformatter added to OMERO.web with default configuration (line-length 88)
    - Plan to extend this to other repos
    - Included in bug-fix release of OMERO.web 5.8.1 - fixes Python 3.5 support
  - OMERO 5.6 pre-release in prep for testing

- Bio-Formats
   - Bio-Formats 6.6 freeze upcoming
   - Includes bfoptions. bioformats2raw also starting to use them.
   - Now is the time to get involved on the API changes.

- SA
  - GPFS mostly updated, Nightshade still needs another bump (SLS will be in touch)
  - Necromancer is dead. 2006-2020 :tada:
  - Jason: waiting on multi-year discounts for Dell SLAs

- Glencoe - Chris:
    - label image progress with TileDB etc. String handling
    - Zarr/n5 community will also need to handle string encoding when outside of Python(3). E.g. C++ & C
      - Josh: https://github.com/zarr-developers/zarr-specs/issues/83 et al.
      - Mostly focusing on Python & Java support
    - Users now converting e.g. 40k x 50k 32 bit masks

- Community
  - Remote workshops in Canada and Sweden upcoming
  - Continuing local support
  - Sanger (Ola) running into session issues. To be written up

## AOB

(5 min. max; tech. Discussion should be highlighted to relevant people
and rescheduled)

 - https://github.com/ome/meeting-minutes as well as [www#403](https://github.com/ome/www.openmicroscopy.org/pull/403)
 - All previous meeting minutes have been converted to MarkDown.
 - Better access to community
 - Josh: Zoom link to be public? At least give directions for community - how to ask to join?
 - JRS: UoD offering office equipment (see e-mail)
 - J-m: review of documentation is ongoing, including IDR, categorizing which type of documentation.
   - Based on feedback that finding the correct docs are difficult.

## Main Topic

(20-25 minutes plus 15 minutes questions max)

 - Ramping up on the NGFF work for IDR
   - Similar push to pre-OME2020
   - Likely to be other similar projects coming online - Allen, Sanger, Hubmap etc.
       - Aim to use same architecture 
   - Targeting something before the end of the year
 - “Enrichment study” to drive the work rolled into a production IDR release
   - idr0015 - improving tara, cf. geolocalization metadata + [notebook](https://github.com/IDR/idr-notebooks/pull/70)
     - JRS: haven't received any comments.
   - idr0022 - mentioned by Jason
   - idr0033 - [open notebook PR](https://github.com/IDR/idr-notebooks/pull/34/files) (script), reference
   - idr0036 - reference
   - idr0041 + idr0052: mitotic atlas (3D masks) - [view](http://idr.openmicroscopy.org/webclient/img_detail/5514337/?dataset=6673)
     - No comments
   - Other ways to choose?
     - By frequently accessed
     - By ROIs? https://trello.com/b/50a1xTU5/investigation-analytics 
     - Is HCS study too large?
 - Features might include:
   - Microservice for faster thumbnails in IDR. Especially HCS studies.
   - json(-ld) in IDR web for SEO e.g. bioschemas. Embed info in Study pages
     - Potentially related to mapr update
   - Some subset of NGFF specs
     - *For example:* HCS, spatial context, polygons, tissues, dimension order, provenance (of masks), scaling of pyramids
     - *Note:* largely things not in OME-XML
   - Conversion of files to Zarr with those specs
     - might need cluster infrastructure for large-scale conversion
   - Notebooks showing how to use them for analysis
     - J-m: tools that work well with the new format
   - Improved out-of-band loading of ROIs - https://github.com/ome/omero-iviewer/pull/351 
       - avoid overhead of HQL and ICE
       - Clients will need to handle both
       - Backed by data in NGFF
   - ZarrReader for others to access the enriched images
       - Import NGFF data back into OMERO
 - For discussion
   - Avoiding updating the database (no DB upgrades)
   - Daily meetings

 - Notes
   - Studies
     - Seb: some of the studies listed were public before IDR existed. Perhaps we could look where someone said, "I want it in the IDR so that people can *use* it"
     - Simon: focus on publicity? JRS: 0033 and 0036
     - J-m: was worried about incorrect metadata since it impacts people who are working on cross-study results.
     - Seb: JRS, what does "reference" mean? Poor experience of downloading. Making them truly useful.
       - Can we talk to the people who want them? JRS: know who to ask.
       - JRS: another upcoming example is with idr0094 (Fraunhofer)
 - HCS metadata:
     - Simple hierarchy: Plate name -> Well -> Field/Image
     - Chris: s3 data for community to consume - may not contain labels.
     - Simon: benefit of serverless (no downtime). batch analysis.
     - J-m: showcase and then others can slurp the data to their own cloud ("federation")
       - CellProfiler is a good target for the parallelization
     - JRS: running analyzes in the EBI resources is currently slow. Speed up is good.
       - Also need to enable for download.
- TODO:
    - omero-cli-zarr export a Plate (bioformats2raw)
    - ome-zarr-py recognise a Plate
    - Simon: would want to have a visualization. Work with existing partners.
      - Chris: python based image analysis for a heatmap (Erin/StarDist)
      - Could then write out some ROIs that could be visualized. ilastik is another option.
    - NB (Seb): another submission (idr0080/Will) from the same folks as 0033 & 0036 (i.e. illum. corrected plate)
    - Thumbnails --> Chris: secondary cache location that could be read from directly.
      - Microservice could be updated to read scaled data from there.
      - Any other client would be able to read the downsampled data (non-rendered)
      - Dom: problem for IDR is the generation of the thumbnails
      - Chris: you'd pre-process the plate into a zarr and then expand the MS so that there is no generation.
      - Seb: play with windows & colors but raw data is immutable
      - Chris: deals with the metadata issues around thumbnails (group permissions, rendering settings)
      - “Thumbnails as a pyramidal level” or Thumbnails-as-a-service
      - JRS: for an OMERO in a large screening environment is there a limit?
        - Chris: feeling is that it accelerates substantially such that center panel could render in real time.
      - Josh: might not be available for OMERO users immediately as will require S3 connection
        - Simon: good to remember that at least for public S3 it's just another HTTP so it's easy to publish.
      - Will: you will also need to load the rendering def (Josh: json in the S3 metadata)
      - Chris: perhaps an impetus to accelerate the retrieval of the rendering settings (and/or exchange)
      - JRS: would significantly change the import process
      - Chris: already need to be transformed due to scale
    - Metadata
      - Josh: similar to the process above, but rather than binary, extracting metadata and putting it somewhere.
      - Simon: more top-level no? Josh: also at the lower-level, but it must be aggregated to search from the top
      - Seb: similar to recent IDR "I want to search across two dimensions"
      - JRS: thumbnails as discussed is nicely boundary, but then start scoping the metadata and look for the use cases to test the concept. Seb: just the metadata at the top-level may already be beneficial and give some search benefit.
      - Will: is the goal to use NGFF to fix as many problems as possible?
      - Josh: (long-winded response)
      - Simon: to put things in elasticsearch, for example, you have to have a schema, so why should that be different from the schema that we put in the NGFF?
      - JMB: look at the notebooks that take days to finish. Do not scale.
      - Chris: separating storage & exchange from the services. If you're doing real work, this is going to be dynamic. Need to consider the API.
      - Simon: can mapr survive on IDR for the next 2 months? (Seb: Other than organism. Don't know to what extent it's affecting people.)
      - ES, sparql, graphql, 
      - Mark: ignoring OMERO permissions? Chris previously had added filters. Need to define some conventions like "if you can read an image then you can read everything below". i.e. Document structure. But: ES is *not* a graph DB. E.g. many-to-manys need to be decided *a priori*. Need to expose that to the end-user.
    - ZarrReader?
      - David: doable with an extra jar. Production? Yes, but 0.0.1 or 0.1.0 is fine.
      - Can then decide how it gets rolled into non-IDR
      - Josh: at that point we'll need to start taking breakages into account
      - Simon: if we have a reader, then we can start planning those decisions.
      - Chris: users are accepting of upgrades processes that take many hours on release.
      - Seb: purely operationally, it's been a long-time and not many people have done it. We need more people who feel comfortable doing so. (Takes days?!)
      - Simon: set up people's expectations upfront "breaking changes that require an upgrade process"
      - David: first iteration is our existing API with no changes or are we implementing chunk-loading?
        - Seb: 2 months? Not hard to implement but agreeing on the API
        - Josh: experimental interface that only ZarrReader is implementing? Perhaps unique
        - Start with public method `if isAZarrThing(reader):`
