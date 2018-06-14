# HCPSS Search Result Bundles

Creating editorialized bundles of results to complement specific searches performed on [search.hcpss.org](https://search.hcpss.org).

## Naming the Bundle

Bundled resources should be structured around a *primary*" topic - i.e. JumpStart, Food Services, Canvas, etc. The primary topic should be included in the bundle's filename so that we can reference it directly as a RESTful resource addressable in Elasticsearch.

Example: `topic-jumpstart.json`

## JSON Document Structure

The JSON files are composed in three parts -

* an array of `search_terms` that capture specific terms and synonyms
* a singular `primary_result` that aligns with the chosen topic, and
* a `secondary_results` array that include secondary, supplemental, or associated resources.

The following example is built to bundle resources around the JumpStart program.

``` json

{
  "search_terms": [
    "jumpstart",
    "dual enrollment",
    "hcc",
    "howard community college",
    "college credit"
  ],
  "primary_result": {
    "title": "JumpStart",
    "url": "https://www.hcpss.org/jumpstart/",
    "description": "A partnership between HCPSS and Howard Community College to expand options"
   },
  "secondary_results": [
     {
       "title": "JumpStart - Sample Course Schedules",
        "url": "https://www.hcpss.org/jumpstart/course-schedule/",
        "description": "Course schedule samples detailing the possible dual enrollment opportunities."
     }
   ]
}

```  
