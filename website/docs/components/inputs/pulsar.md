---
title: pulsar
type: input
status: experimental
categories: ["Services"]
---

<!--
     THIS FILE IS AUTOGENERATED!

     To make changes please edit the contents of:
     lib/input/pulsar.go
-->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

EXPERIMENTAL: This component is experimental and therefore subject to change or removal outside of major version releases.

Reads messages from an Apache Pulsar server.

```yaml
# Config fields, showing default values
input:
  pulsar:
    url: ""
    topics: []
    subscription_name: ""
```

### Metadata

This input adds the following metadata fields to each message:

```text
- pulsar_key
- pulsar_topic
- All properties of the message
```

You can access these metadata fields using
[function interpolation](/docs/configuration/interpolation#metadata).

## Fields

### `url`

A URL to connect to.


Type: `string`  
Default: `""`  

```yaml
# Examples

url: pulsar://localhost:6650

url: pulsar://pulsar.us-west.example.com:6650

url: pulsar+ssl://pulsar.us-west.example.com:6651
```

### `topics`

A list of topics to subscribe to.


Type: `array`  
Default: `[]`  

### `subscription_name`

Specify the subscription name for this consumer.


Type: `string`  
Default: `""`  


