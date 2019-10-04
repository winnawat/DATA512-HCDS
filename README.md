# data-512-a1
Repository DATA512 A1 assignments

## Goal

To visualize the traffic data on wikipedia page on the monthly basis. This should shed insights into both the interest the website recevies and the modes in which the visitors use to visit the site.

## Data source

Wikimedia API: https://www.mediawiki.org/wiki/REST_API

By using the REST API, you agree to Wikimedia's general [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en) and [Privacy Policy](https://foundation.wikimedia.org/wiki/Privacy_policy).

## Data file
The final combined data file is en-wikipedia_traffic_200712-201908.csv
The fields are:
- year: The year in which the traffic data is collected. Formated as YYYY
- month: The month in which the traffic data is collected. Formatted as mm
- pagecount_desktop_views: The sum of the view count from desktop users collected from the legacy pagecount API.
- pagecount_mobile_views: The sum of the view count from mobile users collected from the legacy pagecount API.
- pageview_desktop_views: The sum of the view count from desktop users collected from the pageview API.
- pageview_mobile_views: The sum of the view count from mobile users collected from the pageview API.
- pagecount_all_views:  The sum of the view count from both desktop and mobile users collected from the legacy pagecount API.
- pageview_all_views: The sum of the view count from both desktop and mobile users collected from the pageview API.

5 JSON files are also included. These are the data generated from the APIs.

## Any other things to note
- data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
- Zero values in the CSV table represent NaN. That is, the data is unavailable. 
  - `df.replace(0, np.nan, inplace=True)` can be used to remove the zeroes to create the visualization.
