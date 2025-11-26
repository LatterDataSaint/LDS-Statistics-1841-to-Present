# LDS-Statistics-1841-to-Present
This csv contains data from three datasets: the transcribed statistical data tables from cumorah.com's statistical images; the archived Facts and Statistics pages; and a much smaller dataset of just the years that temples went into operation (see the _op_temples_ field).  In the spirit of transparency and open data principles, this data may be used for any purpose.

Please read the following to better understand the fields in this csv.

**DATE**

**_date_value_**

cumorah: Dates have been inferred to be December 31st of the reported year.

FS: Typically, the Facts and Statistics pages were updated annually in the spring (after spring General Conference). That reported number is meant to be December 31st of the previous year. However, the Facts and Statistics pages were occasionally updated at irregular times throughout the year and it's unclear what that means in terms of when the number was determined versus when it appeared in the Facts and Statistics page. To account for this, I simply subtracted 1 year from the dates of the html pages. For example, let's say on April 1st, 2016 the Facts and Statistics page says memberhsip in a country is 75,000, then on July 1st, 2016 it gets updated to 85,000 - this would show up in this csv as 2015-04-01 75,000 and 2015-10-01 85,000. This would create a minor discrepancy in the visualization where the cumorah data and the Facts and Statistics data overlap because there would be 75,000 on April 1st (from Facts and Statistics), 85,000 on July 1st (also from Facts and Statistics), then 75,000 again on December 31st (from cumorah). This wouldn't mean that the actual membership went up and down 10,000 during that year, it's just the most accurate way I could come up with to represent the data. I may come up with a different way to normalize it in the future but, like I said, since I don't know what the irregular Facts and Statistics updates mean in terms of timing, how I have it now is the best I could do. For now, if you want to see a continuous record, I'd recommend avoiding any overlaps in those two series by simply defining specific cutoff dates.

Temples Only: Dates are December 31st of each year.

**STATISTICAL DATA**

**_membership_**

cumorah: As reported.

FS: As reported.

**_wards_**

cumorah: As reported.

FS: Wards weren't reported in the Facts and Statistics pages until 2018.

**_branches_**

cumorah: As reported.

FS: Branches weren't reported in the Facts and Statistics pages until 2018.

**_congregations_**

cumorah: Reports this value as "units". Since it's simply wards + branches, I didn't bother transcribing it, I've simply calculated the number after the fact.

FS: As reported. Congregations was always reported in the Facts and Statistics pages.

**_stakes_**

cumorah: As reported.

FS: Stakes weren't reported in the Facts and Statistics pages until 2018.

**_districts_**

cumorah: As reported.

FS: Districts weren't reported in the Facts and Statistics pages until 2018.

**_missions_**

As reported from each source. 

**_op_temples_**

Temples Only: cumorah's data reported the year a temple was announced. The Facts and Statistics pages reported an inconsistent mix of: _temples_; _temples as of October 2, 2022_; and _temples including operating and announced_. This mix of reporting rendered it effectively useless unless one wants to parse out that information so I created and populated this field to show a consistent metric - the number of operating temples at the end of the calendar year.

**GEOGRAPHIC INFORMATION**

**_state_, _country_, and _continent_** 

All states/provinces (for United United States and Canada), countries, and continents are populated as needed and correspond to the LDS church's regional designations.


**SOURCE INFORMATION**

**_footnotes_**

cumorah: All original footnotes from the cumorah data table images have been preserved.

Facts and Statistics: No footnotes added.

**_source_**

Description: A brief and informal description of the data source. 

cumorah: "Compiled by https://cumorah.com".

Facts and Statistics: "Archvied 'Facts and Statistics' pages from the Wayback Machine, 2012 - 2025"

Temples Only: ""https://en.wikipedia.org/wiki/List_of_temples_(LDS_Church)""

**_series_name_**

Description: A short series name appropriate for data analysis and chart legends.

cumorah: "cumorah.com (to 2019)"

Facts and Statistics: "Facts and Statistics (2012 - 2025)"

Temples Only: "Temples Only"
