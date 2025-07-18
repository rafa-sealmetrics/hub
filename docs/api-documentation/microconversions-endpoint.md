---
title: Microconversions Endpoint
slug: microconversions-endpoint
sidebar_label: Microconversions Endpoint
---
[Skip to main content](#main-content)![Image](/img/a37799c64a3031dd8bee1ad2404decf7.png)

[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[All Collections](/en/)[API Documentation](https://help.sealmetrics.com/en/collections/12580132-api-documentation)Overview

The Microconversions endpoint provides detailed analytics about microconversion events on your website. Microconversions are small engagement actions that users take before completing a primary conversion, such as adding items to cart, viewing product details, or signing up for newsletters.



Endpoint Details



-URL: `https://app.sealmetrics.com/api/report/microconversions`

[https://app.sealmetrics.com/api/report/microconversions`](https://app.sealmetrics.com/api/report/microconversions`)-Method: GET

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

date_range

string

Yes

Date range for the data (format: YYYYMMDD,YYYYMMDD or predefined values like `this_month`)

skip

No

No

Number of records to skip (for pagination), defaults to 0

limit

No

No

Maximum number of records to return, defaults to 100 with max value of 100

country

string

No

ISO 3166-1 alpha-2 country code filter (e.g., "es" for Spain



Example Request



cURL



```bash

curl --location 'https://app.sealmetrics.com/api/report/microconversions?account_id=000000000000000000001234&date_range=this_month&skip=0&limit=100' \

[https://app.sealmetrics.com/api/report/microconversions?account_id=000000000000000000001234&date_range=this_month&skip=0&limit=100](https://app.sealmetrics.com/api/report/microconversions?account_id=000000000000000000001234&date_range=this_month&skip=0&limit=100)--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI:ImpoaS1Nzg5MzQzIn0...' \

--header 'Accept: application/json' \

--header 'Connection: keep-alive' \

--header 'Accept-Encoding: gzip, deflate, br'

```



Python



```python

import requests



url = "https://app.sealmetrics.com/api/report/microconversions"

[https://app.sealmetrics.com/api/report/microconversions](https://app.sealmetrics.com/api/report/microconversions)

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



fetch("https://app.sealmetrics.com/api/report/microconversions?account_id=000000000000000000001234&date_range=this_month&skip=0&limit=100", requestOptions)

[https://app.sealmetrics.com/api/report/microconversions?account_id=000000000000000000001234&date_range=this_month&skip=0&limit=100](https://app.sealmetrics.com/api/report/microconversions?account_id=000000000000000000001234&date_range=this_month&skip=0&limit=100).then(response => response.text())

.then(result => console.log(result))

.catch(error => console.log('error', error));

```



Response



Success Response (200 OK)



```json

,



// Additional results...

]

}

```



Response Parameters



The response data array contains objects with the following fields:

Field

Type

Description

_id

string

Unique identifier for the microconversion

date

string

Date of the microconversion (YYYY-MM-DD)

utm_medium

string

Medium that drove the microconversion (e.g., email, organic)

utm_source

string

Source that drove the microconversion (e.g., seo, newsletter)

utm_campaign

string

Campaign associated with the microconversion

utm_term

string

Term or URL associated with the microconversion

utm_matchtype

string

Match type for search campaigns (may be null)

label

string

Type of microconversion (e.g., "add-to-cart", "newsletter-signup"



Error Response (401 Unauthorized)



```json



```



Error Response (400 Bad Request)



```json



```



Notes



- Microconversions are valuable for understanding user engagement before final conversions

- Different microconversion types are identified by the `label` field

- Analyze microconversions alongside main conversions to optimize your conversion funnel

- Use date filtering to track changes in microconversion patterns over time



[Acquisition Endpoint](https://help.sealmetrics.com/en/articles/11125053-acquisition-endpoint)[Pages Endpoint](https://help.sealmetrics.com/en/articles/11125236-pages-endpoint)[Conversions Endpoint](https://help.sealmetrics.com/en/articles/11125264-conversions-endpoint)[ROAs Evolution Endpoint](https://help.sealmetrics.com/en/articles/11125318-roas-evolution-endpoint)[Funnel Endpoint](https://help.sealmetrics.com/en/articles/11125349-funnel-endpoint)[SealMetrics Help Center](/en/)Company

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