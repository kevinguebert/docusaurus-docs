---
id: introduction
title: Introduction
sidebar_label: Introduction
slug: /
---

## Welcome to the Business Services Platform

The Business Services Platform (BSP) powers some of the largest retailers, restaurants, and companies across the globe. With our powerful APIs, one can take online orders, handle user data within the cloud, recall historical transactions, manage restaurant menus, maintain your company's location, and more.

## Getting Started

:::important

In order to use BSP APIs you'll need:

- A [developer.ncrcloud.com](https://developer.ncrcloud.com) account
- A sandbox environment with an organization, a shared key, and a secret key.

Follow the instructions below to learn how to get setup.
:::

### Creating Your Account

To setup your account with BSP, visit [developer.ncrcloud.com](https://developer.ncrcloud.com).

In the top right, click on "Sign Up" to create your account.

:::tip

Be sure to check your email for the confirmation link

:::

![Sign Up](../../static/img/business-services-platform/sign-up.png)

### Creating Your Sandbox

After confirming your account, log in to [developer.ncrcloud.com](https://developer.ncrcloud.com) and visit the ["Explore APIs" page](https://developer.ncrcloud.com/portals/dev-portal/api-explorer).

![Explore APIs](../../static/img/business-services-platform/explore-apis.png)

In the list of available APIs, visit the API that says [Business Services Platform](https://developer.ncrcloud.com/portals/dev-portal/api-explorer/details/8849/documentation).

![Business Services Platform](../../static/img/business-services-platform/click-bsp.png)

At the top of the page, there should be a green "Try It Out" button.

:::tip

Don't see the button? Make sure you're logged in and have confirmed your account by clicking the link in the confirmation email.

:::

![Try It Out](../../static/img/business-services-platform/try-it-out.png)

Click this button to get a sandbox environment provisioned for your account.

A modal will appear with instructions on how to download the Postman collection with examples of available APIs.

![Postman Modal](../../static/img/business-services-platform/postman-modal.png)

### Organization Key

To retreive the required Organization key, [visit your dashboard](https://developer.ncrcloud.com/dx/user-dashboard) by clicking on your username in the top right and then clicking on ["Dashboard"](https://developer.ncrcloud.com/dx/user-dashboard).

Visiting your dashboard will show all of your applications you have available, including the sandbox environment application you just provisioned.

:::tip

Don't see an application? **Log out and then log back in.**

:::

Click on your application and you'll be redirected to your application information.

In the middle of the screen there is a section called "Service User Name". The service username is your **Fully Qualified Username** which can be used for [accessing TDM data](/apis/tdm) and more.

![Fully Qualified Username](../../static/img/business-services-platform/fully-qualified-username.png)

The fully qualified username is made up of 2 pieces:

```
acct:[organization]@[username]
```

The organization you will use is what follows `acct:` and before the `@` sign.

### Shared and Secret Key

On the same application dashboard page, to the right of "Access Keys" is a plus button. Click that button to generate new Access Keys.

![Plus Button](../../static/img/business-services-platform/plus-button.png)

A modal will appear with a new Shared and Secret Key. Be sure to save those keys for future use as you'll have to create new ones if you forget or lose the current ones.

![Access Key](../../static/img/business-services-platform/access-keys.png)
