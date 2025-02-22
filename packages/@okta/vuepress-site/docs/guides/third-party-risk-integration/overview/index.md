---
title: Third-party risk provider integration overview
---

<ApiLifecycle access="ea" />

The Okta Risk Engine evaluates authentication attempts by reviewing the risk score of the sign-in based on context and historical data. Using Okta Risk APIs, third-party risk providers can integrate with the Okta Risk Engine using a standard Okta service application. The third-party risk provider can send risk events, which can be used when calculating the authentication risk based on the risk policy configured in the Okta org. The risk events are additionally logged as part of the System Log.

This guide provides an example third-party risk provider implementation with your Okta org.

>**Note:** Third-party risk events are shared with and received from Non-Okta Applications.  Non-Okta Applications include web-based, offline, mobile, or other software application functionality that are provided by you or a third party and interoperate with the Okta Service. You are not required to receive or utilize third-party risk events within Okta Risk Engine, but if you configure Okta Risk Engine to utilize third-party risk events, then you agree on behalf of your organization that Okta may receive and share data with the Non-Okta Application as necessary to provide this functionality. You may only utilize these third-party risk events if you are a customer of both Okta and the Non-Okta Application. Okta cannot guarantee continued partnerships or functionality with any Non-Okta Applications.

### Prerequisites
To use this guide, you need the following:

- An Okta developer org. [Create an org for free](/signup/).
- To configure your Okta org for third-party risk providers. Contact your Okta customer support representative for this configuration.
- A [Postman client](https://www.postman.com/downloads/) to configure and test the risk provider integration. We recommend going through [Get Started with the Okta APIs](/code/rest/) to set up Postman.
- Download the Risk API Collection:
[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/47546754d382762468c6)

### High-level configurations
Creating a third-party risk provider integration follows the general configurations for creating an OAuth service application using the OAuth client credentials grant flow. The service application provides an integration for the default risk provider and the Okta Risk Engine, and Risk Event API calls can test for a successful setup. Follow the high-level steps below to set up an example third-party risk provider integration.

1. [Create self-service application for the risk provider](/docs/guides/third-party-risk-integration/create-service-app)
2. [Update the default risk provider](/docs/guides/third-party-risk-integration/update-default-provider)
3. [Test the integration](/docs/guides/third-party-risk-integration/test-integration)

### See also

- [Implement OAuth for Okta with a service app](/docs/guides/implement-oauth-for-okta-serviceapp/)
- [Risk Providers API](/docs/reference/api/risk-providers/)
- [Risk Events API](/docs/reference/api/risk-events/)
- [Risk Scoring and Risk Based Authentication](https://help.okta.com/okta_help.htm?id=csh-risk-scoring)

<!-- ## Support

If you need help or have an issue, post a question in our [Developer Forum](https://devforum.okta.com).-->

<NextSectionLink/>
