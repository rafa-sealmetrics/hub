---
title: Conversions Endpoint
slug: conversions-endpoint
sidebar_label: Conversions Endpoint
---
[Skip to main content](#main-content)![Image](/img/a37799c64a3031dd8bee1ad2404decf7.png)

[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[All Collections](/en/)[API Documentation](https://help.sealmetrics.com/en/collections/12580132-api-documentation)Overview



The Conversions endpoint provides detailed analytics about conversion events on your website. This endpoint allows you to track and analyze sales, sign-ups, or other conversion events across different marketing channels and campaigns.



Endpoint Details



-URL: `https://app.sealmetrics.com/api/report/conversions`

[https://app.sealmetrics.com/api/report/conversions`](https://app.sealmetrics.com/api/report/conversions`)-Method: GET

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

No

No

ISO 3166-1 alpha-2 country code filter (e.g., "es" for Spain)

utm_medium

string

No

Filter by medium (e.g., email, cpc, social media)

utm_source

string

No

Filter by source (e.g., google, facebook, newsletter)

utm_campaign

string

No

Filter by campaign name



Example Request

cURL



```bash

curl --location 'https://app.sealmetrics.com/api/report/conversions?date_range=this_month&skip=0&limit=100&account_id=000000000000000000001234' \

[https://app.sealmetrics.com/api/report/conversions?date_range=this_month&skip=0&limit=100&account_id=000000000000000000001234](https://app.sealmetrics.com/api/report/conversions?date_range=this_month&skip=0&limit=100&account_id=000000000000000000001234)--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI:ImpoaS1Nzg5MzQzIn0...' \

--header 'Accept: application/json' \

--header 'Connection: keep-alive' \

--header 'Accept-Encoding: gzip, deflate, br'

```



Python



```python

import requests



url = "https://app.sealmetrics.com/api/report/conversions"

[https://app.sealmetrics.com/api/report/conversions](https://app.sealmetrics.com/api/report/conversions)

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



fetch("https://app.sealmetrics.com/api/report/conversions?date_range=this_month&skip=0&limit=100&account_id=000000000000000000001234", requestOptions)

[https://app.sealmetrics.com/api/report/conversions?date_range=this_month&skip=0&limit=100&account_id=000000000000000000001234](https://app.sealmetrics.com/api/report/conversions?date_range=this_month&skip=0&limit=100&account_id=000000000000000000001234).then(response => response.text())

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

Unique identifier for the conversion

amount

number

Monetary value of the conversion

utm_medium

string

Medium that drove the conversion (e.g., email, cpc)

utm_source

string

Source that drove the conversion (e.g., google, newsletter)

utm_campaign

string

Campaign associated with the conversion

utm_term

string

Term or URL associated with the conversion

utm_matchtype

string

Match type for search campaigns (may be null)

country

string

ISO 3166-1 alpha-2 country code

country_name

string

Full name of the country

date

string

Date of the conversion (YYYY-MM-DD)

label

string

Type of conversion (e.g., "sales")



Error Response (401 Unauthorized)



```json



```



### Error Response (400 Bad Request)



```json



```



Notes



- This endpoint provides detailed information about individual conversion events

- Use the filtering parameters to analyze conversions from specific marketing channels or campaigns

- The response includes both the country code and full country name for easier reporting

- The `amount` field represents the monetary value of each conversion, useful for ROI calculations



[Acquisition Endpoint](https://help.sealmetrics.com/en/articles/11125053-acquisition-endpoint)[Pages Endpoint](https://help.sealmetrics.com/en/articles/11125236-pages-endpoint)[Microconversions Endpoint](https://help.sealmetrics.com/en/articles/11125290-microconversions-endpoint)[ROAs Evolution Endpoint](https://help.sealmetrics.com/en/articles/11125318-roas-evolution-endpoint)[Funnel Endpoint](https://help.sealmetrics.com/en/articles/11125349-funnel-endpoint)[SealMetrics Help Center](/en/)Company

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