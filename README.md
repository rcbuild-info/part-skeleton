# RCBuild.Info parts
[RCBuild.info](https://rcbuild.info) is in its early stages so many part haven't been imported into the repository. Your help in improving this data would be greatly appreciated.

## Getting started
RCBuild.Info's part information is stored in its [own GitHub repo](https://github.com/tannewt/rcbuild.info-parts). To get started, fork your own version of the repo. Now what do you want to do?
* [Find a part in my build](#find-a-part)
* [Add a new part](#add-a-part)
* [Curate parts for my build](#curate-a-part)
* [Bulk import more parts](#bulk-import)

## Find a part
Many more parts exist in the part repository than are listed on the [supported parts page](https://rcbuild.info/parts/supported). All of the known parts are listed [here](https://rcbuild.info/parts/all). Search in the page to find your part and use its ID as you would a supported part. If its still not there, [please add it](#add-a-part).

## Add a part
Adding a part is easy!
1. In your copy of the part repo verify there is a directory for the manufacturer of the part. If there isn't, create one with the name of the manufacturer where spaces are replaced with dashes.
2. Create a file with the name of the part with spaces replaced by dashes. Part names should not include the manufacturer name or the category of the product (for example a flight controller name should not include "Flight Controller" in its name.)
3. Copy the contents from the `part.json` file in this repository into the new file.
4. Fill it out based on the [reference](#reference) below.
5. Submit a pull request from your repo to the canonical one and wait for it to be accepted.

## Curate a part
Parts can be curated more easily with scripts in [here](https://github.com/tannewt/rcbuild.info-scrape/tree/master/refactor_scripts).

## Bulk import parts
Many parts have already be added tentatively by scraping popular RC part stores. The code that does it lives [here](https://github.com/tannewt/rcbuild.info-scrape). Its been done over [ReadyMadeRC](http://www.readymaderc.com/store/), [ReadyToFlyQuads](http://readytoflyquads.com/), [GetFPV](http://www.getfpv.com/), [Flyduino](http://flyduino.net/) and [UAVObjects](http://www.uavobjects.com/) so far.

## Reference
* `category` - category of the part. Should match a key in the [partCategories.json](partCategories.json) file in this repo.
* `equivalent` - rcbuild.info IDs of exact parts that are branded separately.
* `name` - name of the part. May or may not match any retailers name. Should not include the name of the manufacturer or its category.
* `manufacturer` - name of the manufacturer of the part.
* `replacement` - rcbuild.info IDs of parts that fulfill the same purpose as this part.
* `subpart` - rcbuild.info IDs of parts that are included in this part. This is useful for replacement parts for frames for example.
* `url` - grouped lists of related urls.
  * `store` - links to places where the part is available for purchase.
  * `manufacturer` - links to canonical part pages by the parts manufacturer.
  * `related` - links to anything related to the part such as its RCGroups thread.
