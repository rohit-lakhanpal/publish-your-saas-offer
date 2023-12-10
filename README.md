<a id="readme-top"></a>

<!-- PROJECT SHIELDS -->
<!--
*** Using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">
    Publish Your SaaS Offer
  </h3>

  <p align="center">
    powered by
    <br />
    <a href="https://github.com/rohit-lakhanpal/build-your-own-copilot">
    <img src="docs/img/logo.png" alt="Logo" height="80">
  </a>
    <br />
    <a href="https://github.com/rohit-lakhanpal/build-your-own-copilot"><strong>Explore the docs »</strong></a>
    <br />
    <br />    
    <a href="https://github.com/rohit-lakhanpal/publish-your-saas-offer/issues">Report Bug</a>
    ·
    <a href="https://github.com/rohit-lakhanpal/publish-your-saas-offer/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>      
    </li>
    <li>
      <a href="#pre-requisites">Pre-Requisites</a>
      <ul>
        <li><a href="#pre-requisite-1">Get Microsoft Edge (or similar)</a></li>
        <li><a href="#pre-requisite-2">Permissions to create offers in Partner Center</a></li>
        <li><a href="#pre-requisite-3">Permissions to create apps and app registrations on Azure</a></li>
        <li><a href="#pre-requisite-4">Separate Azure Tenant to test "Purchasing"</a></li>
      </ul>
    </li>
    <li>
      <a href="#step-1">Deploy Commercial Marketplace SaaS Accelerator</a>
      <ul>
        <li><a href="#step-1-1">Create App Registrations</a></li>        
        <li><a href="#step-1-2">Deploy the SaaS Accelerator</a></li>                
      </ul>
    </li>
    <li>
      <a href="#step-2">Create a SaaS Offer on the Azure Marketplace</a>
      <ul>
        <li><a href="#step-2-1">Basic Setup</a></li>
        <li><a href="#step-2-2">Setup Properties</a></li>
        <li><a href="#step-2-3">Setup Offer Listing</a></li>
        <li><a href="#step-2-4">Setup Plan Overview</a></li>
        <li><a href="#step-2-5">Setup Preview Audience</a></li>
        <li><a href="#step-2-6">Setup Resell through CSPs</a></li>
        <li><a href="#step-2-7">Setup Technical Configuration</a></li>
      </ul>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This project, **`Publish Your SaaS Offer`**, aims to facilitate the deployment of a transactable SaaS offer to the Azure Marketplace. It leverages the [Commercial Marketplace SaaS Accelerator](https://azuremarketplace.microsoft.com/en-au/marketplace/apps/microsoft_commercial_marketplace_services.saas_accelerator?tab=Overview), enabling developers to streamline the publication process and ensure optimal integration with the marketplace platform. This project acts as a catalyst for software vendors, fostering a smooth and efficient transition to a market-ready state, and provides a pathway for increased visibility and accessibility of SaaS solutions within the Azure environment.

The [Commercial Marketplace SaaS Accelerator](https://azuremarketplace.microsoft.com/en-au/marketplace/apps/microsoft_commercial_marketplace_services.saas_accelerator?tab=Overview) by Microsoft is a robust solution designed to support Independent Software Vendors (ISVs) in crafting and deploying their SaaS offers. It provides a spectrum of resources such as technical guidance, integration expertise, and best practices. These are intended to expedite the time to market and refine the integration of solutions with the Microsoft Azure Marketplace. By utilizing this accelerator, ISVs are poised to navigate the complexities of SaaS publication, ensuring their offerings are well-positioned and competitive in the marketplace. The SaaS Accelerator is open source on GitHub and available for forking or modifying if you wish.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PRE-REQUISITES  -->
## Pre-Requisites

There are several prerequisites to meet before starting the creation or publication of an offer. Please review them carefully and ensure each one is satisfied before proceeding with the publication of your offer.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Pre-Requisite 1  -->
### Pre-Requisite 1
#### Get Microsoft Edge (or similar)

We recommend utilizing a browser like Microsoft Edge for an optimal experience, especially when you need to log in with multiple identities. The "Sign in and create multiple profiles in Microsoft Edge" feature can efficiently manage multiple log-ins, allowing for seamless transition between different profiles. To utilize this feature, follow the instructions provided [here](https://support.microsoft.com/en-us/topic/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435). This approach ensures a smoother, more integrated user experience, mitigating the hassles associated with managing multiple online identities.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Pre-Requisite 2  -->
### Pre-Requisite 2
#### Permissions to create offers in Partner Center

Before starting the creation or publication of your offer, follow the steps below to verify if you have the necessary permissions to create Marketplace Offers in the Microsoft Partner Center:

1. Log into the [Microsoft Partner Center](https://partner.microsoft.com/dashboard).
2. Once logged in, navigate to "My Access."
3. In the "My Access" section, check if "Marketplace Offers" is listed and if access is granted. 

<i>For internal Microsoft employees:<br>
Please note, if "Marketplace Offers" does not have access granted, follow these instructions to create a test account to publish offers on Partner Center: [Create a Test Account for Marketplace Publishing](https://microsoft.sharepoint.com/:w:/t/MasteringtheMarketplace/EQ7xYtzBWIdMpRyIwnfvjqMBavINIAHy717HZCK-2IlLLg?e=2NpKlN). These instructions will result in a new test Azure AD tenant that must be used for the app registrations in step 1 below, as well as for logging in to Partner Center with the point of view of a Global Admin of a publisher (as opposed to a Microsoft employee).  NOTE: 
  * Azure Active Directory is now Microsoft Entra ID
  * Only complete up to "Working with Partner Center Step 2: Enrolling into the Commercial Marketplace Program".  There is no need to complete "Step 3: Completing vetting and authorization" which is only needed for production offers</i>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Pre-Requisite 3  -->
### Pre-Requisite 3
#### Permissions to create apps and app registrations on Azure

To ensure a seamless deployment of managed applications, begin by verifying your access and permissions within the [Azure Portal](https://portal.azure.com/). Managed applications require the creation of app registrations in Azure Active Directory (Azure AD), so it is crucial to confirm your ability to perform such tasks.

1. Log in to the [Azure Portal](https://portal.azure.com/).
2. Verify your permissions to create app registrations.
3. Confirm your ability to create and manage applications, focusing especially on managed applications.

Ensuring that all requisite permissions are correctly assigned and operational before proceeding will help in avoiding potential roadblocks, allowing for a smoother navigation and execution of your project within the Azure environment.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Pre-Requisite 4  -->
### Pre-Requisite 4
#### Separate Azure Tenant to test "Purchasing"

Ensure you have access to a separate Azure Tenant to test the "Purchasing" functionality effectively. If needed, create a separate one using [cdx.transform.microsoft.com](https://cdx.transform.microsoft.com/). Having a dedicated tenant for testing purposes is crucial to isolate variables and accurately assess the purchasing process, ensuring that any modifications or updates do not interfere with the live environment.

Alternatively, you might have a `Personal` Azure Subscription (the free one). That should work too.

Once you have it, all you need is the `Azure Active Directory or Microsoft Account email address` associated with this Azure Subscription. When you publish or update an offer, we will create a preview version accessible to only the audience that you specify based on the email address captured. In my example this is `admin@my-domain.org` but you should capture your own.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- Steps to Publish a SaaS Offer  -->
## Steps to Publish a SaaS Offer

To publish a SaaS offer, please complete the steps outlined below, ensuring all prerequisites are met beforehand. It's imperative to comply with all the preparatory requirements to avoid any hindrances during the publication process. Careful adherence to each step and prerequisite ensures a smoother, more streamlined experience, enabling the successful deployment of your SaaS offer.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-1"></a>

<!-- STEP 1  -->
### STEP 1: Initial Setup: App Registrations and SaaS Accelerator Deployment

This initial step involves creating app registrations as depicted in Step 1.1 and deploying the SaaS accelerator in Step 1.2.

<a id="step-1-1"></a>

#### 1. Create App Registrations

1. **Login to Azure Portal**: As the "Publisher", log into the [Azure Portal](https://portal.azure.com/).  Remember to log in or switch to the Azure AD tenant created in pre-requisite 2 above, as the app registrations must be created within the correct Azure AD tenant that has permission to publish SaaS offers.

2. **Access Azure AD and Create App Registrations**: Open Azure AD and create two app registrations as described below:
   
3. **App Registration 1 - Single Tenant App Registration**:
    - Create this registration.
    - After creation, add a client secret.
    - Capture the following details: tenant ID, client ID, and client secret.

4. **App Registration 2 - Multi Tenant App Registration**:
    - This registration supports the login of the WebApps created as part of this deployment.
    - You will need to update the App Reg Redirect URIs post-deployment (see step 3 below)
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-1-2"></a>

#### 2. Deploy the SaaS Accelerator

1. **Login to Azure Portal**: Make sure you are logged in as your @microsoft.com address to the FDPO Microsoft tenant.  It is recommended to use the FDPO tenant as the SaaS Accelerator provisions chargable Azure resources such as SQL DB, App Service etc.  Provisioning under the FDPO tenant ensures that you don't have to pay a separate Azure bill.

2. **Initiate Resource Creation**: Click on "Create a Resource".

3. **Search for SaaS Accelerator**: Enter “SaaS Accelerator” in the search bar.

4. **Verify Publisher**: In your search results, ensure that "Microsoft Commercial Marketplace" is the listed publisher.

5. **Initiate Deployment**: Click "Create" and select a "Basic Deployment".

6. Fill out the required information in the "Create SaaS Accelerator" page click "Review + create", then "Create".  NOTE: use a relatively short unique identifier as a long identifier will cause the deployment to fail.  Ten characters or less is confirmed to work.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-2"></a>

#### 3. Update multi-tenant app registration

1. Open the multi-tenant app registration in the Azure portal
2. Click "Add a redirect URI" or select "Authentication" in the "Manage" segment of the left hand navigation bar
3. Click "Add a platform" and click "Web"
4. Enter the landing page portal URL from the SaaS Accelerator with the path /Home/index in the redirect URI eg https://uniqueid-portal.azurewebsites.net/Home/Index
5. Enable the ID token option
6. Click "Configure"
7. Click "Add URI" and add the admin portal URI with /Home/Index in addition to the landing page portal added in step 4 above and click "Save"

<!-- STEP 2  -->
### STEP 2: Create a SaaS Offer on the Azure Marketplace

To create a new SaaS offer, follow the steps below:

<a id="step-2-1"></a>

#### 1. Basic Setup
   1. **Navigate to Partner Center**: Go to [Partner Center](https://partner.microsoft.com/).
   2. **Access Marketplace Offers**: Click on "Marketplace Offers."
   3. **Initiate New Offer**: Click "New Offer" and select "Software as a Service."
   4. **Configure Offer ID**: Add a new Offer ID (e.g., `your-biz-name_your-prod-name-offer-001` or `example_company_example_product_offer_001`). Use only lowercase, alphanumeric characters, dashes, or underscores. The ID cannot end with "-preview" and is immutable after "Create" is selected.
   5. **Set Offer Alias**: Add an Offer alias (e.g., `Example Product Offer 001`). This alias is for internal reference within Partner Center and won’t be visible in the marketplace listing.
   6. **Create the Offer**: Click "Create." You will be redirected to the "Offer Setup" page, with some details pre-filled. Retain the default settings.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-2-2"></a>

#### 2. Setup `Properties`
   1. **Access Properties Page**: Navigate to the "Properties" page.
   2. **Select Category and Subcategory**: Click "Categories," then choose a category and a subcategory (e.g., `AI + Machine Learning` as the category and `Knowledge Mining` as the subcategory). Any available pair should suffice.
   3. **Choose Industry and Vertical**: Click `Industries` and select an industry and its corresponding vertical (e.g., `Education` as the industry and `Libraries and Museums` as the vertical). Any available options are suitable.
   4. **Agree to Standard Contract**: Select the checkbox corresponding to "Use the Standard Contract for Microsoft’s commercial marketplace?"
   5. **Save draft**: Lastly, click the "Save draft" button.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-2-3"></a>

#### 3. Setup `Offer Listing`
   1. **Access Listing Page**: Once the basic setup and offer properties are configured, navigate to the "Offer Listing" page from the offer’s menu.
   2. **Input Offer Details**: In this section, enter all relevant details about the offer. These details will be displayed in the marketplace and will include:
        - **Name**: (e.g. `Edu Insight Miner SaaS App`) 
        - **Search results summary**: Write a concise summary highlighting the key features and benefits of your offer.

            e.g. `Knowledge Mining Software as a Service solution designed to empower education.`
        - **Description**: Provide a detailed description of your offer, elaborating on its features, benefits, and use cases. Utilize markdown formatting to structure the content effectively.

            e.g. `This offer provides a Knowledge Mining Software as a Service solution designed to empower education sector entities such as libraries and museums by extracting valuable insights from their data resources to enhance learning and research outcomes.`
        - **Getting Started Instructions**: 
            e.g. `To embark on your knowledge mining journey with EduInsight Miner, start by pointing the service to your school or museum's catalog or database. Navigate to our user-friendly interface and follow the intuitive, step-by-step instructions to link your institutional resources. Once connected, you can immediately begin leveraging the power of advanced data analysis to uncover insights and enrich the learning and research experience at your institution. Our dedicated support team is available to assist you with any queries or challenges you might encounter as you explore the untapped knowledge within your establishment.`
        - **Privacy policy link**: e.g. `https://privacy.microsoft.com/en-us/privacystatement`
        - **Support and Engineering contact Details**: 
            - Name: John Smith
            - Email: johnsmith@contoso.com
            - Phone: e.g. `13 20 58`
            - Support link: `https://support.microsoft.com/en-au`
        - **Supporting Documents**: Add the following document:
            - e.g. Upload this [sample document](docs/sample/supporting-document.pdf)
            - Note: Don't forget to add a Name after uploading the document.
        - **Logos**: Add the following logos
            - e.g. use this for [216x216](docs/sample/logo-216x216.png)             
        - **Screenshots**: Add the following screenshots
            - e.g. use this [screenshot](docs/sample/screenshot.png)
            - Note: Don't forget to add a caption after uploading the image.
        3. **Save draft**: Lastly, click the "Save draft" button.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-2-4"></a>

#### 4. Setup `Plan Overview`

To set up the Plan Overview, please perform the following steps:

   1. **Navigate to Plan Overview**: Begin by accessing the “Plan Overview” section.
   2. **Create a New Plan**: Select the "Create new plan" option.
   3. **Input Plan ID**: Enter a Plan ID with less than 50 characters (e.g., `edu-insights-miner-basic-plan`). Utilize only lowercase, alphanumeric characters, dashes, or underscores. Note that the ID cannot end with "-preview" and is unmodifiable after "Create" is selected.
   4. **Specify Plan Name**: Designate a Plan Name (e.g., `Edu Insight Miner SaaS Basic Plan`).
   5. **Create the Plan**: Click "Create."
   6. **Add a Description**: Input a brief description for the plan (e.g., `This is a basic free plan.`).
   7. **Save the Draft**: Press the "Save draft" button.
   8. **Configure Pricing and Availability**: Proceed to the "Pricing and availability" section and:
        1. **Edit Markets**: Click “edit markets,” select all available markets, and press “save.”
        2. **Set Pricing**: Choose “Per User” for Pricing.
        3. **Define Billing Term**: Opt for “1-year” as the billing term, “One-time” as the payment option, and set the Price per payment per user to “0 USD.”
        4. **Enable Free Trial**: Allow users a one-month free trial by selecting the "Free Trial" option.
   9. **Save the Draft Again**: Ensure all the entered details are correct and click "Save draft."
   10. **Review and Await Confirmation**: After saving, please wait a moment for a notification stating “Complete and ready for publish.” Once this notification appears, proceed to “Review and Publish.”
   11. This should now re-direct you to the `Offer overview` page. At this stage you should see the following are complete:
        1. Offer setup
        2. Properties
        3. Offer listing
        4. Plan overview
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-2-5"></a>

#### 5. Setup `Preview Audience`

Setting up a Preview Audience allows a select group to access and verify your offer before it goes live. This preview version is only available to the audience you designate. To include individuals in your preview audience, you'll need to use either their Azure Active Directory (AAD) or Microsoft Account (MSA) email addresses. Here's how to set it up:

   1. **Navigate to Preview Audience**: Start by going to the “Preview Audience” section.
   2. **Add Email Addresses**: Input the “Azure Active Directory or Microsoft Account email address” that was recorded during ["Pre-Requisite 4"](#pre-requisite-4).
   3. **Save the Draft**: After adding the email addresses, click the "Save Draft" button to secure your changes.

Ensuring that your preview audience is correctly set up will facilitate a smoother verification process for your offer’s details before they are made publicly available.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-2-6"></a>

#### 6. Setup `Resell through CSPs`

Making your offer available through the Cloud Solution Providers (CSP) program can extend its reach, enabling resellers to offer your solution to their customer base and to incorporate it into bundled solutions. Once live, you may also incentivize your preferred CSP partners by creating margins. For more extensive details about leveraging CSP Private Offers, please refer to the [available documentation](https://learn.microsoft.com/en-au/partner-center/marketplace/azure-private-plan-troubleshooting). 

To configure the resell options through CSPs, perform the following steps:

   1. **Choose CSP Program Partners**: Initially, opt for `No partners in the CSP program`.
   2. **Save the Draft**: Click "Save draft" to apply your selection.

Remember, the decisions made at this stage can be revised later, allowing you to change your CSP preferences as your offering evolves.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<a id="step-2-7"></a>

#### 7. Setup `Technical Configuration`

In this step, you will link the offer to the "Commercial Marketplace SaaS Accelerator" app which was established in [Step 1](#step-1). Follow the guide below to integrate the information accumulated from the preceding steps:

   1. **Access Technical Configuration**: Navigate your way to the “Technical Configuration” section.
   
   2. **Enter Required Details**: Based on the information collected previously, populate the following fields:
      - **Landing Page URL**: Input the appropriate URL where users will land when they access your offer.  This is the landing page of the SaaS Accelerator portal (eg https://mpndemo-portal.azurewebsites.net)
      - **Connection Webhook**: Provide the connection webhook that will be used to communicate with the offer.  This is the landing page URL with /Api/AzureWebhook added (eg https://mpndemo-portal.azurewebsites.net/Api/AzureWebhook)
      - **Microsoft Entra Tenant ID**: Insert the tenant ID related to Microsoft Entra for your single tenant app registration.
      - **Microsoft Entra Identity Application ID**: Specify the application ID from Microsoft Entra Identity for your single tenant app registration.

Ensure that all the provided details are accurate and correspond to the information gathered in the initial steps, as this will establish the essential connections for your offer’s functionality in the Commercial Marketplace.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### 8. Click 'Review and Publish'

Click the review and publish button. The offer will take about 20-30 minutes to publish, at which point you will receive an "app source preview" link under the "Publisher signoff" column.  Use this app source preview link to test a purchase using one of the accounts listed in 'Preview Audience" above.

<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/rohit-lakhanpal/publish-your-saas-offer.svg?style=for-the-badge
[contributors-url]: https://github.com/rohit-lakhanpal/publish-your-saas-offer/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/rohit-lakhanpal/publish-your-saas-offer.svg?style=for-the-badge
[forks-url]: https://github.com/rohit-lakhanpal/publish-your-saas-offer/network/members
[stars-shield]: https://img.shields.io/github/stars/rohit-lakhanpal/publish-your-saas-offer.svg?style=for-the-badge
[stars-url]: https://github.com/rohit-lakhanpal/publish-your-saas-offer/stargazers
[issues-shield]: https://img.shields.io/github/issues/rohit-lakhanpal/publish-your-saas-offer.svg?style=for-the-badge
[issues-url]: https://github.com/rohit-lakhanpal/publish-your-saas-offer/issues
[license-shield]: https://img.shields.io/github/license/rohit-lakhanpal/publish-your-saas-offer.svg?style=for-the-badge
[license-url]: https://github.com/rohit-lakhanpal/publish-your-saas-offer/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/rohitlakhanpal
