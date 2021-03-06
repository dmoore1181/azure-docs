---
title: SaaS offer creation checklist in Microsoft commercial marketplace
description: The details you can provide in the SaaS offer creation process in Partner Center. 
ms.service: marketplace 
ms.subservice: partnercenter-marketplace-publisher
ms.topic: conceptual
ms.date: 05/08/2020
author: mingshen-ms
ms.author: mingshen
---

# SaaS offer creation checklist in Partner Center

The SaaS offer creation process takes you through multiple pages.  This article describes the details you can provide on each page, with links to learn more about each item.

> [!NOTE]
> If you're creating a transactable SaaS offer please make sure you implement integration with [SaaS fulfillment APIs](./pc-saas-fulfillment-apis.md).  Integration with the APIs is the only way for the transactability in Marketplace to work properly. You also need to make sure your app uses Azure AD authentication with single sign on (SSO). See [Azure AD and transactable SaaS offers in the commercial marketplace](../azure-ad-saas.md).

Items you're required to provide or specify are noted below.  Some areas are optional or have default values provided, that you can change as desired.  You don't have to work on these sections in the order listed here.

| Item | Purpose |
| ---------- | -------------------|
| [**New offer modal**](#new-offer-modal) | Collects offer identity information.  |
| [Offer setup page](#offer-setup-page) | Allows you to opt in to use key features and choose how to sell your offer through Microsoft.  |
| [Properties page](#properties-page) | Define the categories and industries used to group your offer on the marketplaces, the legal contracts supporting your offer, and your app version. |
| [Offer listing page](#offer-listing-page) | Define the offer details to be displayed in the marketplace, including descriptions of your offer and marketing assets.|
| [Preview page](#preview-page) | Define a limited Preview Audience for releasing your offer prior to publishing your offer live to the broader marketplace audience(s).|
| [Technical configuration page](#technical-configuration-page)  |  Only available if you select to sell the offer through Microsoft.  Define the technical details (Landing page URL, Connection webhook URL, Azure AD tenant ID, and Azure AD app ID) used by marketplace to connect to your offer.  These parameters are required to integrate correctly with SaaS fulfillment and the Marketplace metered billing APIs.|
| [**New plan modal**](#plan-identity-modal) | Collects plan identity information.  |
| [Plan listing page](#plan-listing-page)  | Only available if you select to sell the offer through Microsoft. Define the details used to list the Plan in the marketplace.  |
| [Plan pricing and availability page](#plan-pricing-and-availability-page)  | Only available if you select to sell the offer through Microsoft.  Collects the business characteristics (pricing model), audience and market availability for each plan (version) of your offer.  |
| [Test drive listing page](#test-drive-listing-page)  | Only available if you select to offer a test drive for your offer. Define the details used to list the test drive in the marketplace.  |
| Test Drive Technical Configuration Page  | Only available if you select to offer a test drive for your offer. Define the technical details for the  demonstration (or "test drive") which will enable customers to try your offer before committing to purchase it.  |
| [Review and publish page](#review-and-publish-page)  | Select the changes you want to publish, see the status of each page, and provide notes to the certification team.  |
|

## New offer modal

The first pieces of information you will be asked to provide are an ID and alias for your offer.

| Field name | Notes |  
| ---------------- | -----------|
| Offer ID  | Required, can't be changed after creation. Max 50 characters and must consist only of lowercase, alphanumeric characters, dashes, or underscores. |
| Offer alias  | Required |
|

## Offer setup page

The offer setup page is where you can opt into different channels and selling motions, as well as declare the use of key features, such as test drive and customer leads.

| Field name | Notes |
| ---------------- | -----------|  
| Would you like to sell through Microsoft?  | Required. Default: Yes. |
| How do you want potential customers to interact with the offer listing? (Call to action)  | Required if not selling through Microsoft. Default: Free Trial, Options: "Get it now", "Free Trial", "Contact me." |
| Trial URL  | Required if "Free Trial" is selected, as the way customers should interact with the offer listing. |
| Offer URL  | Required if "Get it Now" is selected, as the way customers should interact with the offer listing. |
| Channels  | Optional. Default: Not opted into the CSP (reseller) channel.  |
| Test Drive | Optional. Default: No test drive enabled.  |
| Type of Test Drive | Required if enabled a test drive. Default: None selected. Options: Azure Resource Manager, Dynamics 365 for Business Central, Dynamics 365 for Customer Engagement, Dynamics 365 for Operations, Logic app, Power BI.  |
| Customer leads - connect to a CRM system | Required if selling through Microsoft, or if listing offers as "Contact me." Default: no CRM system connected. CRM options: Azure table, Azure blob, Dynamics CRM online, HTTPs' endpoint, Marketo, Salesforce.  |
|

## Properties page

The properties page is where you define the categories and industries used to group your offer on the marketplaces, the legal contracts supporting your offer, and your app version. Be sure to provide complete and accurate details about your offer on this page, so that it's displayed appropriately and offered to the right set of customers.

| Field name | Notes |
| ---------------- | -----------|  
| Category and subcategory | Required 1 and max 3. Default: None selected. |
| Industries and subindustries | Optional. max 2 L1 Industries and max 2 subindustries within each L1 industry, Default: None selected |
| App version  | Optional. Default: None. |
| Use Standard Contract  | Optional. Default: not selected.  |
| Terms of use  | Required if Standard Contract is not selected.  |
|

## Offer listing page

The listing page is where you provide the text and images that customers see when viewing your offer's listing in the marketplace.

| Field name | Notes |
| ---------------- | -----------|
| Name  | Required, max 50 chars. |
| Summary  | Required, max 100 chars. |
| Description  | Required, max 3000 chars. |
| Getting Started Instructions  | Required, max 3000 chars. |
| Getting Started Instructions  | Required, max 3000 chars. |
| Search keywords  | Optional, recommended, max 3 keywords. |
| Privacy policy URL  | Required |
| CSP Program Marketing Materials URL  | Optional |
| Useful links Title + URL  | Optional |
| Supporting Documents Title + File  | Required, min 1 and max 3. Must be PDF file format. |
| Screenshots  | Required, min 1 screenshot and max 5; four or more recommended. Must be 1280 X 720 in PNG format. |
| Store logos (Small, Medium, Large)  | The Large logo (from 216 x 216 to 350 x 350 px) is required. Partner Center will use this to create a Small (48 x 48 px) and Medium (90 x 90 px) logo. You can optionally replace these with different images later. Logos must be in PNG format. |
| Videos name + URL + thumbnail  | Optional, recommended, max 4 videos. Thumbnail must be 1280 x 720 in PNG format. Video must be hosted in YouTube or Vimeo. |
| Contacts (CSP Program,  Engineering, Support)  | Engineering and Support contact required (Name, email, and phone number); CSP Program contact optional but recommended. |
| Support URL  | Required |
|

## Preview page

The preview page is where you specify the audience to have access to your offer preview, to verify that the offer meets all your requirements before it goes live.

| Field name | Notes |
| ---------------- | -----------|
| AAD/MSA email + description | Required, min 1  and max 10 if entered manually, or up to 20 if uploading a CSV file. |
|

## Technical configuration page

The technical configuration page is where you specify the technical details used by Microsoft to connect to your offer. This page is not visible to you if you decided not to sell through Microsoft.

> [!NOTE]
> For transactable offers, you must create a landing page and your app must use Azure AD authentication with single sign on (SSO). For more information, see [Azure AD and transactable SaaS offers in the commercial marketplace](../azure-ad-saas.md).

| Field name | Notes |  
| ---------------- | -----------| 
| Landing Page URL | Required if selling through Microsoft. |
| Connection webhook | Required if selling through Microsoft. |
| Azure AD tenant ID | Required if selling through Microsoft. |
| Azure AD app ID | Required if selling through Microsoft. |
|

## Plan identity modal

The first pieces of information you are asked to provide are a name and an ID for your Plan. This page is not visible to you if you have decided not to sell through Microsoft.

| Field name | Notes |  
| ---------------- | -----------|
| Plan ID  | Required if selling through Microsoft. It can't be changed after creation. Max 50 characters and must consist only of lowercase, alphanumeric characters, dashes, or underscores. |
| Plan Name  | Required if selling through Microsoft. Must be unique across all the plans in the offer. Max 50 characters. |
|

## Plan listing page

The plan listing page is where you provide the text for customers to see when viewing the plan in the marketplace. This page is not visible to you if you decided not to sell through Microsoft.

| Field name | Notes |  
| ---------------- | -----------|
| Plan Description   | Required if selling through Microsoft. Max 500 characters. |
|

## Plan pricing and availability page

The plan pricing and availability page is where you define the business characteristics, audience, and market availability for each plan (version) of your offer. This page is not visible to you if you decided not to sell through Microsoft.

| Field name | Notes |
| ---------------- | -----------|
| Market availability  | Required, min 1 and max 141. |
| Pricing Model  | Required. Default: Flat rate. Options: Flat rate, per user. |
| Minimum and maximum seats  | Optional, only available if seat-based pricing model selected. |
| Billing Term  | Required. Default: Monthly. Options: Monthly, Annual. |
| Price  | Required USD per month, if monthly billing term selected; or USD per year if annual billing term selected. |
| Plan Audience  | Optional. Default: Public plan. Options: Public, Private by tenant ID |
| Restricted Plan Audience (tenant ID + description)  | Required if private plan selected. Min 1 and max 10 tenant IDs if entered manually. Max 20000 if CSV file import. |
|

## Test drive listing page

Only available if you select to offer a test drive for your offer. Define the details used to list the test drive in the marketplace.

| Field name | Notes |
| ---------------- | -----------|
| Description  | Required |
| User Manual name + file  | Required, max 1 doc. Must be PDF format. |
| Video name, URL + thumbnail  | Optional, recommended. Thumbnail must be 533 x 324 in JPGP or PNG format. Video must be hosted in YouTube or Vimeo. |
|

## Review and publish page

| Field name | Notes |
| ---------------- | -----------|
| Notes for certification  | Optional |
|

## Next steps

- [Create a new SaaS offer](./create-new-saas-offer.md)
