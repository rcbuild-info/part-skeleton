Part json files encode information about a part used on an RC Copter. This skeleton file is the basis for part files in the rcbuild.info-parts repo.

* url - list of urls to retail websites that sell the part.
* name - name of the part. May or may not match any retailers name.
* manufacturer - name of the manufacturer of the part.
* category - category of the part. Should match a key in the build json file.
* subpart - rcbuild.info IDs of parts that are included in this part. This is useful for replacement parts for frames for example.
* equivalent - rcbuild.info IDs of exact parts that are branded separately.
* replacement - rcbuild.info IDs of parts that fulfill the same purpose as this part.