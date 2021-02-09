---
id: basic-authentication
title: Basic Authentication
sidebar_label: Basic Authentication
slug: /authentication/basic-authentication
---

Basic Authentication utilizes a username and password for `Authorization`. HMAC is preferred for production applications but Basic Authentication can be used for sandbox environments.

:::note
Basic Authentication is not set up by default for applications and requires an API request.
:::

## Setup

:::important
In order to setup Basic Auth you'll need:

- A [developer.ncrcloud.com](https://developer.ncrcloud.com) account
- A sandbox environment with an organization, a shared key, and a secret key. Don't have an environment? Visit the [Introduction](/introduction) to learn how to setup.

Follow the instructions below to learn how to get setup.
:::

Your organization, shared key, and secret key all come from the application you've created from the "Try It Out" button.

To find your username, visit [developer.ncrcloud.com](https://developer.ncrcloud.com), and click on the dropdown menu next to your name to visit your [Dashboard](https://developer.ncrcloud.com/dx/user-dashboard/myapplications).

Click on the application in the dashboard to view your application details.

There is a section called Service User Name.

![Fully Qualified Username](../../../static/img/business-services-platform/fully-qualified-username.png)

The fully qualified username is made up of 2 pieces:

```
acct:[organization]@[username]
```

Your username is everything after the @ sign.

```
<form>
<input />
```

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
