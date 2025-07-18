---
title: Set-Click Endpoint
slug: set-click-endpoint
sidebar_label: Set-Click Endpoint
---
[Skip to main content](#main-content)![Image](/img/a37799c64a3031dd8bee1ad2404decf7.png)

[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[Academy](https://sealmetrics.com/privacy-marketing-academy/)[Partners](https://sealmetrics.com/partners/)[All Collections](/en/)[API Documentation](https://help.sealmetrics.com/en/collections/12580132-api-documentation)Overview

The Set-Click endpoint allows you to record conversion events associated with user clicks. This endpoint is particularly useful for tracking offline conversions or conversions that happen outside your main website flow, such as phone calls or in-person visits that originated from online marketing efforts.



Endpoint Details



-URL: `https://app.sealmetrics.com/api/auth/v1.0/set-click`

[https://app.sealmetrics.com/api/auth/v1.0/set-click`](https://app.sealmetrics.com/api/auth/v1.0/set-click`)-Method: POST

-Authentication: Bearer Token required

-Content-Type: application/x-www-form-urlencoded



Request Parameters

Headers

Header

Value

Required

Authorization

Bearer 

Yes

Content-Type

application/x-www-form-urlencoded

Yes

Accept

application/json

Yes



Body Parameters

Parameter

Type

Required

Description

account_id

string

Yes

Your account identifier (must match with your client_id)

url_parameters

object

Yes

JSON object containing UTM parameters (utm_medium, utm_source, etc.)

click_time

number

Yes

Timestamp of the click (Unix timestamp in milliseconds)

settings

object

Yes

JSON object containing settings like email

referrer

string

No

Referrer URL

current_url

string

No

Current URL



Example Request

cURL



```bash

curl --location 'https://app.sealmetrics.com/api/auth/v1.0/set-click' \

[https://app.sealmetrics.com/api/auth/v1.0/set-click](https://app.sealmetrics.com/api/auth/v1.0/set-click)--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI:ImpoaS1Nzg5MzQzIn0...' \

--header 'Content-Type: application/x-www-form-urlencoded' \

--header 'Accept: application/json' \

--data-urlencode 'url_parameters=' \

--data-urlencode 'click_time=1634707888' \

--data-urlencode 'settings=' \

[[email protected]](/cdn-cgi/l/email-protection#d2b6b3a4bbb6fcbcb3a4b3a0a0bd92b3b6bbbca6bdbcfcb1bdbf)--data-urlencode 'referrer="https://facebook.com/"' \

[https://facebook.com/](https://facebook.com/)--data-urlencode 'current_url="https://sealmetrics.com/"' \

[https://sealmetrics.com/](https://sealmetrics.com/)--data-urlencode 'account_id=60a52f6ac660b269d13c3f53'

```



Python



```python

import requests



url = "https://app.sealmetrics.com/api/auth/v1.0/set-click"

[https://app.sealmetrics.com/api/auth/v1.0/set-click](https://app.sealmetrics.com/api/auth/v1.0/set-click)

payload = ',

'click_time': '1634707888',

'settings': '',

[[email protected]](/cdn-cgi/l/email-protection#7c181d0a151852121d0a1d0e0e133c1d181512081312521f1311)'referrer': '"https://facebook.com/"',

[https://facebook.com/](https://facebook.com/)'current_url': '"https://sealmetrics.com/"'

[https://sealmetrics.com/](https://sealmetrics.com/)}



headers = 



response = requests.request("POST", url, headers=headers, data=payload)



print(response.text)

```



JavaScript



```javascript

var myHeaders = new Headers();

myHeaders.append("Authorization", "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI:ImpoaS1Nzg5MzQzIn0...");

myHeaders.append("Content-Type", "application/x-www-form-urlencoded");

myHeaders.append("Accept", "application/json");



var urlencoded = new URLSearchParams();

urlencoded.append("account_id", "60a52f6ac660b269d13c3f53");

urlencoded.append("url_parameters", "");

urlencoded.append("click_time", "1634707888");

urlencoded.append("settings", "");

[[email protected]](/cdn-cgi/l/email-protection#aecacfd8c7ca80c0cfd8cfdcdcc1eecfcac7c0dac1c080cdc1c3)urlencoded.append("referrer", "\"https://facebook.com/\"");

[https://facebook.com/\](https://facebook.com/\)urlencoded.append("current_url", "\"https://sealmetrics.com/\"");

[https://sealmetrics.com/\](https://sealmetrics.com/\)

var requestOptions = ;



fetch("https://app.sealmetrics.com/api/auth/v1.0/set-click", requestOptions)

[https://app.sealmetrics.com/api/auth/v1.0/set-click](https://app.sealmetrics.com/api/auth/v1.0/set-click).then(response => response.text())

.then(result => console.log(result))

.catch(error => console.log('error', error));

```



Response



Success Response (200 OK)



This request doesn't return any response body when successful.



```

No response body

```



Error Response (401 Unauthorized)



```json



```



Error Response (400 Bad Request)



```json



```



Notes



- This endpoint applies a conversion to the last click of the journey

- You need offline-leads scope enabled in your Adinton user to use this method

- The `account_id` parameter must match with your client_id from your credentials

- The `url_parameters` should include all relevant UTM parameters as a JSON object

- If you want to create a microconversion, you have to include "microconversion":"1" in the lead parameter

- This endpoint is particularly useful for connecting offline conversions with online marketing efforts

- All parameters should be properly URL-encoded when sent in the request



[Acquisition Endpoint](https://help.sealmetrics.com/en/articles/11125053-acquisition-endpoint)[Account Endpoints](https://help.sealmetrics.com/en/articles/11125188-account-endpoints)[Pages Endpoint](https://help.sealmetrics.com/en/articles/11125236-pages-endpoint)[Conversions Endpoint](https://help.sealmetrics.com/en/articles/11125264-conversions-endpoint)[Microconversions Endpoint](https://help.sealmetrics.com/en/articles/11125290-microconversions-endpoint)[SealMetrics Help Center](/en/)Company

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