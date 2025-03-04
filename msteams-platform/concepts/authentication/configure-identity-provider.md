---
title: Configure OAuth 2.0 identity providers
description: Describes how to configure identity providers with a focus on Azure AD
ms.topic: how-to
ms.localizationpriority: medium
keywords: teams authentication AAD oauth identity provider
---
# Configure identity providers

## Configuring an application to use Azure Active Directory as an identity provider

Identity providers supporting OAuth 2.0 will not authenticate requests from unknown applications; applications must be registered ahead of time. To do this with Azure AD, follow these steps:

1. Open the [Application Registration Portal](https://ms.portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade).

2. Select your app to view its properties, or select the "New Registration" button. Find the **Redirect URI** section for the app.

3. Select **Web** from the dropdown menu. Update the URL to your authentication endpoint. For the TypeScript/Node.js and C# sample apps on GitHub, the redirect URLs will be similar to the following:

    Redirect URLs: `https://<hostname>/bot-auth/simple-start`

Replace `<hostname>` with your actual host, which might be a dedicated hosting site such as Azure, Glitch, or a ngrok tunnel to localhost on your development machine such as `abcd1234.ngrok.io`. You may not have this information if you haven't completed or hosted your app (or the sample app that's mentioned above), but you can always return to this page when that information is known.

## Other authentication providers

* **LinkedIn:** Follow the instructions in [Configuring your LinkedIn application](/linkedin/talent/apply-with-linkedin)

* **Google:** Obtain OAuth 2.0 client credentials from the [Google API Console](https://console.developers.google.com/)
