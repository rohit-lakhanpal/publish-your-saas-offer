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
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

This project, **`Publish Your SaaS Offer`**, aims to facilitate the deployment of a transactable SaaS offer to the Azure Marketplace. It leverages the [Commercial Marketplace SaaS Accelerator](https://azuremarketplace.microsoft.com/en-au/marketplace/apps/microsoft_commercial_marketplace_services.saas_accelerator?tab=Overview), enabling developers to streamline the publication process and ensure optimal integration with the marketplace platform. This project acts as a catalyst for software vendors, fostering a smooth and efficient transition to a market-ready state, and provides a pathway for increased visibility and accessibility of SaaS solutions within the Azure environment.

The [Commercial Marketplace SaaS Accelerator](https://azuremarketplace.microsoft.com/en-au/marketplace/apps/microsoft_commercial_marketplace_services.saas_accelerator?tab=Overview) by Microsoft is a robust solution designed to support Independent Software Vendors (ISVs) in crafting and deploying their SaaS offers. It provides a spectrum of resources such as technical guidance, integration expertise, and best practices. These are intended to expedite the time to market and refine the integration of solutions with the Microsoft Azure Marketplace. By utilizing this accelerator, ISVs are poised to navigate the complexities of SaaS publication, ensuring their offerings are well-positioned and competitive in the marketplace.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PRE-REQUISITES  -->
## Pre-Requisites

Before initiating the creation or publication of the offer, it's imperative to meet certain prerequisites. These are essential steps or requirements that need to be fulfilled to ensure a seamless process and are listed below for your convenience. Please review them carefully and ensure each one is satisfied before proceeding with the publication of your offer.

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

1. Log into the [Microsoft Partner Center](https://partner.microsoft.com/).
2. Once logged in, navigate to "My Access."
3. In the "My Access" section, check if "Marketplace Offers" is listed and if access is granted. 

Please note, if "Marketplace Offers" does not have access granted, you will need to secure the appropriate permissions before proceeding with creating or publishing Marketplace Offers.

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