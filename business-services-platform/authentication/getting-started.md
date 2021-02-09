---
id: getting-started
title: Getting Started with Authentication
sidebar_label: Getting Started
slug: /authentication/getting-started
---

Authentication will be required in order to access any of the Business Services Platform APIs. Authentication of requests requires a valid user account on [developer.ncrcloud.com](https://developer.ncrcloud.com) and valid credentials for the user account.

Authentication of requests is handled by the `Authorization` HTTP header. The platform currently supports two types of authentication schemes:

### Access Key Authentication

:::note

Access Key Authentication is the preferred authentication format for production applications

:::

The Access Key authentication scheme uses hash-based message authentication (HMAC) code to uniquely sign an individual HTTP request.

This type of scheme is used specifically for system-to-system authentication between applications. Your server generates a valid HMAC code to sign API requests to send to the NCR APIs with the `Authorization` header.

Visit [HMAC Documentation](/docs/authentication/hmac) to learn how to implement.

### Basic Authentication

Basic authentication utilizes a username and password to authenticate a request. HTTP Basic authentication follows the HTTP specification for the Basic scheme of the Authorization header in a request. The username/password are separated by a `:` character, and the credentials are encoded in Base64. The scheme used in the `Authorization` header is `Basic`.

Visit [Basic Authentication Documentation](/docs/authentication/basic-auth) to learn how to implement.
