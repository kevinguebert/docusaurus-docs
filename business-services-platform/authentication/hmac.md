---
id: hmac
title: HMAC Authentication
sidebar_label: HMAC Authentication
slug: /authentication/hmac
---

Access Key authentication uses a hash-based message authentication code (HMAC) to uniquely sign a single HTTP request.

Access keys are comprised of two parts: a **secret key** and a **shared key**.

Below is an example of access key authentication in an HTTP request:

```
GET /provisioning/user-profiles HTTP/1.1
Accept: application/json
Authorization: AccessKey e63ca6a9ca2e4db2bc13b741e7488437:Ysvt4LcqSnmIjvPbolVm2bS/zDXdqnYBtgtG+lWMlLI6uJp1MJiW34OVNtYrYA/B+6T/NDqhqFxbtlvuIFBliw==
Date: Wed, 26 Jun 2019 17:38:30 GMT
Host: gateway.ncrplatform.com
```

The scheme used in the `Authorization` header is `AccessKey <shared-key>:<hmac>`.

## Advantages

There are some advantages to HMAC authentication, such as:

- It allows maintenance of a single platform identity with multiple credentials expressed in the form of access keys.
- Individual access keys can be disabled or deleted without affecting other keys or the identity itself.
- The secret key never expires, which simplifies interaction with the platform as compared to using temporary access tokens.
- This method guarantees authenticity of the full request instead of a specific part of the request (such as the Authorization header).
- Actual user secrets are never transmitted over the wire as each request has a unique HMAC.

## Implementation

The credentials for `Authorization` request contain a user's shared key and HMAC generated from their shared key. The general algorithm for generating HMAC goes as follows:

1. Get the native `date` value from the request's HTTP headers (passed in)
2. Convert the native `date` to `ISO-8601` string format
3. Generate a unique key from the following concatenate string: `{secretKey + ':' + date}`
4. Generate a signature from the HTTP request data to use in HMAC calculation. The HTTP request data consists of the following parts:
   - HTTP method from the request (Required)
   - Relaite URI from the HTTP request, path, and query string (Required)
   - Content-Type header value (optional)
   - Content-MD5 header value (optional)
   - `nep-application-key` header value (optional)
   - `nep-correlation-id` header value (optional)
   - `nep-organization` header value (optional)
   - `nep-service-version` header value (optional)

## Examples

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs
defaultValue="js"
values={[
{ label: 'JavaScript', value: 'js', },
{ label: 'Python', value: 'py', },
{ label: 'Java', value: 'java', },
]
}>
<TabItem value="js">

```js
function helloWorld() {
  console.log("Hello, world!");
}
```

</TabItem>
<TabItem value="py">

```py
def hello_world():
  print 'Hello, world!'
```

</TabItem>
<TabItem value="java">

```java
class HelloWorld {
  public static void main(String args[]) {
    System.out.println("Hello, World");
  }
}
```

</TabItem>
</Tabs>

## Helper Functions
