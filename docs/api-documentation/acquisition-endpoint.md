---
title: Acquisition Endpoint
slug: acquisition-endpoint
sidebar_label: Acquisition Endpoint
---
[Skip to main content](#main-content)![Image](/img/a37799c64a3031dd8bee1ad2404decf7.png)

[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[All Collections](/en/)[API Documentation](https://help.sealmetrics.com/en/collections/12580132-api-documentation)Overview



The Acquisition endpoint provides detailed information about your customer acquisition metrics, including traffic sources, campaigns, and their performance.



Endpoint Details



-URL: `https://app.sealmetrics.com/api/report/acquisition`

[https://app.sealmetrics.com/api/report/acquisition`](https://app.sealmetrics.com/api/report/acquisition`)-Method: GET

-Authentication: Bearer Token required



Request Parameters



Headers

Header

Value

Required

Authorization

Bearer 

Yes

Accept

application/json

Yes

Connection

keep-alive

Recommended

Accept-Encoding

gzip, deflate, br

Recommended



Query Parameters



Parameter

Type

Required

Description

account_id

string

Yes

Your account identifier

report_type

string

Yes

Type of report to generate (Source, Medium, Campaign, Term, Device, or Os)

date_range

string

Yes

Date range for the data (format: YYYYMMDD,YYYYMMDD or predefined values)

skip

integer

No

Number of records to skip (for pagination), defaults to 0

limit

integer

No

Maximum number of records to return, defaults to 100 with max value of 100

country

string

No

ISO 3166-1 alpha-2 country code filter



Example Request



cURL



```bash

curl --location 'https://app.sealmetrics.com/api/report/acquisition?account_id=000000000000000000001234&report_type=Source&date_range=20230601,20230630&skip=0&limit=100' \

[https://app.sealmetrics.com/api/report/acquisition?account_id=000000000000000000001234&report_type=Source&date_range=20230601,20230630&skip=0&limit=100](https://app.sealmetrics.com/api/report/acquisition?account_id=000000000000000000001234&report_type=Source&date_range=20230601,20230630&skip=0&limit=100)--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI:ImpoaS1Nzg5MzQzIn0...' \

--header 'Accept: application/json' \

--header 'Connection: keep-alive' \

--header 'Accept-Encoding: gzip, deflate, br'

```



Python



```python

import requests



url = "https://app.sealmetrics.com/api/report/acquisition"

[https://app.sealmetrics.com/api/report/acquisition](https://app.sealmetrics.com/api/report/acquisition)

querystring = 



headers = 



response = requests.request("GET", url, headers=headers, params=querystring)



print(response.text)

```



JavaScript



```javascript

var myHeaders = new Headers();

myHeaders.append("Authorization", "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI:ImpoaS1Nzg5MzQzIn0...");

myHeaders.append("Accept", "application/json");

myHeaders.append("Connection", "keep-alive");

myHeaders.append("Accept-Encoding", "gzip, deflate, br");



var requestOptions = ;



fetch("https://app.sealmetrics.com/api/report/acquisition?account_id=000000000000000000001234&report_type=Source&date_range=20230601,20230630&skip=0&limit=100", requestOptions)

[https://app.sealmetrics.com/api/report/acquisition?account_id=000000000000000000001234&report_type=Source&date_range=20230601,20230630&skip=0&limit=100](https://app.sealmetrics.com/api/report/acquisition?account_id=000000000000000000001234&report_type=Source&date_range=20230601,20230630&skip=0&limit=100).then(response => response.text())

.then(result => console.log(result))

.catch(error => console.log('error', error));

```



Response

Success Response (200 OK)



```json

,

,



// Additional results...

]

}

```



Response Parameters



The response data array contains objects with metrics grouped by the requested report_type. Common fields include:



Field

Type

Description

_id

string

Identifier for the group (source name, medium name, etc.)

clicks

number

Number of clicks for this group

page_views

number

Number of page views for this group

conversions

number

Number of conversions for this group

microconversions

number

Number of microconversions for this group

revenue

number

Total revenue generated from this group



Error Response (401 Unauthorized)



```json



```



Error Response (400 Bad Request)



```json



```



Notes



- The `report_type` parameter determines how the data is grouped in the response

- Use pagination parameters (`skip` and `limit`) for large datasets

- Date range can be specified as exact dates or using predefined values like `this_month`



[Pages Endpoint](https://help.sealmetrics.com/en/articles/11125236-pages-endpoint)[Conversions Endpoint](https://help.sealmetrics.com/en/articles/11125264-conversions-endpoint)[Microconversions Endpoint](https://help.sealmetrics.com/en/articles/11125290-microconversions-endpoint)[ROAs Evolution Endpoint](https://help.sealmetrics.com/en/articles/11125318-roas-evolution-endpoint)[Funnel Endpoint](https://help.sealmetrics.com/en/articles/11125349-funnel-endpoint)[SealMetrics Help Center](/en/)Company

Privacy PolicyDPATerms of UseData Privacy Audit

Privacy Policy

[Privacy Policy](https://legal.sealmetrics.com/privacy-notice)DPA

[DPA](https://legal.sealmetrics.com/DPA)Terms of Use

[Terms of Use](https://sealmetrics.com/terms-of-use/)Data Privacy Audit

[Data Privacy Audit](https://app.comply.org/attest/sealmetrics)Guides

Cookie Consent GuideSocial Media AuditCookieless & Google

Cookie Consent Guide

[Cookie Consent Guide](https://sealmetrics.com/mastering-the-cookie-consent-banner/)Social Media Audit

[Social Media Audit](https://sealmetrics.com/in-depth-analysis-of-social-media-privacy-policies/)Cookieless & Google

[Cookieless & Google](https://sealmetrics.com/how-google-is-navigating-the-cookieless-future/)Explore

Check out the live demoNewsletter

Check out the live demo

[Check out the live demo](https://app.sealmetrics.com/reports/cookieless/dashboard)Newsletter

[Newsletter](https://sealmetrics.com/privacy-marketing-newsletter/)