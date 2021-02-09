---
id: retrieving-data
title: Retrieving Data
sidebar_label: Retrieving Data
slug: /authentication/retrieving-data
---

Retrieving data from the NCR BSP APIs is like any GET request to an API. This document outlines how to integrate a GET request with NCR's authentication methods.

## With HMAC

:::important
These functions use the example code from [HMAC Authentication](/authentication/hmac) as helper functions to generate the HMAC code.
:::

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

## With Basic Auth

:::important
These functions use the example code from [Basic Authentication](/authentication/basic-authentication) as helper functions to generate the HMAC code.
:::
