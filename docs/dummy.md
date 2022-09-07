# Dummy example with all spec features included 0.0.1 documentation

* License: [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0)
* Default content type: [application/json](https://www.iana.org/assignments/media-types/application/json)
* Support: [API Support](http://www.asyncapi.com/support)
* Email support: [info@asyncapi.io](mailto:info@asyncapi.io)

[Find more info here](https://www.asyncapi.com)

This is an example of AsyncAPI specification file that is suppose to include all possible features of the AsyncAPI specification. Do not use it on production.

It's goal is to support development of documentation and code generation with the [AsyncAPI Generator](https://github.com/asyncapi/generator/) and [Template projects](https://github.com/search?q=topic%3Aasyncapi+topic%3Agenerator+topic%3Atemplate)

##### Specification tags

| Name | Description | Documentation |
|---|---|---|
| root-tag1 | - | [External docs description 1](https://www.asyncapi.com/) |
| root-tag2 | Description 2 | [Find more info here](https://www.asyncapi.com/) |
| root-tag3 | - | - |
| root-tag4 | Description 4 | - |
| root-tag5 | - | [Find more info here](https://www.asyncapi.com/) |


## Table of Contents

* [Servers](#servers)
  * [dummy-mqtt](#dummy-mqtt-server)
  * [dummy-amqp](#dummy-amqp-server)
  * [dommy-kafka](#dommy-kafka-server)
* [Operations](#operations)
  * [PUB dummy/channel/with/{dummy}/parameter/create](#pub-dummychannelwithdummyparametercreate-operation)
  * [SUB dummy/channel/without/parameter](#sub-dummychannelwithoutparameter-operation)

## Servers

### `dummy-mqtt` Server

* URL: `mqtt://localhost`
* Protocol: `mqtt`

dummy MQTT broker

#### `mqtt` Server specific information

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| clientId | - | - | `"guest"` | - | - |
| cleanSession | - | - | `"true"` | - | - |


### `dummy-amqp` Server

* URL: `amqp://localhost:{port}`
* Protocol: `amqp 0.9.1`

dummy AMQP broker

#### URL Variables

| Name | Description | Default value | Allowed values |
|---|---|---|---|
| port | - | _None_ | `15672`, `5672` |

#### Security

##### Security Requirement 1

* Type: `User/Password`






### `dommy-kafka` Server

* URL: `http://localhost:{port}`
* Protocol: `kafka`

dummy Kafka broker

#### URL Variables

| Name | Description | Default value | Allowed values |
|---|---|---|---|
| port | - | `9092` | _Any_ |

#### Security

##### Security Requirement 1

  * security.protocol: PLAINTEXT







## Operations

### PUB `dummy/channel/with/{dummy}/parameter/create` Operation

*Inform whenever something dummy is created.*

* Operation ID: `receiveNewDummyInfo`

Dummy channel description.

Longer description.

Still dummy though.


##### Operation tags

| Name | Description | Documentation |
|---|---|---|
| oparation-tag1 | - | [External docs description 1](https://www.asyncapi.com/) |
| oparation-tag2 | Description 2 | [Find more info here](https://www.asyncapi.com/) |
| oparation-tag3 | - | - |
| oparation-tag4 | Description 4 | - |
| oparation-tag5 | - | [Find more info here](https://www.asyncapi.com/) |

#### Parameters

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| dummy | string | The ID of the new dummy message. | - | - | **required** |


#### `kafka` Operation specific information

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| clientId | - | - | `"my-app-id"` | - | - |

#### Message Dummy created message `dummyCreated`

*This is just a dummy create message*

##### Headers

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| (root) | object | - | - | - | **additional properties are allowed** |
| my-custom-app-header | string | - | - | - | - |
| correlationId | string | - | - | - | - |

> Examples of headers _(generated)_

```json
{
  "my-custom-app-header": "string",
  "correlationId": "string"
}
```


##### Payload

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| (root) | object | - | - | - | **additional properties are allowed** |
| prop1 | integer | Dummy prop1 | - | >= 0 | - |
| prop2 | string | Dummy prop2 | - | - | **required** |
| sentAt | string | Date and time when the message was sent. | - | format (`date-time`) | - |
| dummyArrayWithObject | array<object> | - | - | - | - |
| dummyArrayWithObject.prop1 | string | Dummy prop1 | allowed (`"option1"`, `"option2"`) | - | **required** |
| dummyArrayWithObject.sentAt | string | Date and time when the message was sent. | - | format (`date-time`) | - |
| dummyArrayWithArray | tuple<object, string, number, ...optional<any>> | - | - | - | **additional items are allowed** |
| dummyArrayWithArray.0 (index) | object | - | - | - | **additional properties are allowed** |
| dummyArrayWithArray.0.prop1 | string | Dummy prop1 | allowed (`"option1"`, `"option2"`) | - | **required** |
| dummyArrayWithArray.0.sentAt | string | Date and time when the message was sent. | - | format (`date-time`) | - |
| dummyArrayWithArray.1 (index) | string | - | - | - | - |
| dummyArrayWithArray.2 (index) | number | - | - | - | - |
| dummyObject | object | - | - | - | **additional properties are allowed** |
| dummyObject.dummyObjectProp1 | string | Date and time when the message was sent. | - | format (`date-time`) | - |
| dummyObject.dummyObjectProp2 | object | - | - | - | **additional properties are allowed** |
| dummyObject.dummyObjectProp2.dummyRecursiveProp1 | object | - | - | - | **circular**, **additional properties are allowed** |
| dummyObject.dummyObjectProp2.dummyRecursiveProp2 | string | - | - | - | - |

> Examples of payload _(generated)_

```json
{
  "prop1": 0,
  "prop2": "string",
  "sentAt": "2019-08-24T14:15:22Z",
  "dummyArrayWithObject": [
    {
      "prop1": "option1",
      "sentAt": "2019-08-24T14:15:22Z"
    }
  ],
  "dummyArrayWithArray": [
    {
      "prop1": "option1",
      "sentAt": "2019-08-24T14:15:22Z"
    },
    "string",
    0
  ],
  "dummyObject": {
    "dummyObjectProp1": "2019-08-24T14:15:22Z",
    "dummyObjectProp2": {
      "dummyRecursiveProp1": {},
      "dummyRecursiveProp2": "string"
    }
  }
}
```


##### Message tags

| Name | Description | Documentation |
|---|---|---|
| message-tag1 | - | [External docs description 1](https://www.asyncapi.com/) |
| message-tag2 | Description 2 | [Find more info here](https://www.asyncapi.com/) |
| message-tag3 | - | - |
| message-tag4 | Description 4 | - |
| message-tag5 | - | [Find more info here](https://www.asyncapi.com/) |


### SUB `dummy/channel/without/parameter` Operation

* Operation ID: `receiveSystemInfo`

#### `amqp` Channel specific information

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| is | - | - | `"routingKey"` | - | - |

#### Message Dummy system info `dummyInfo`

*This is just a dummy info message*

More description for a dummy message.

It is a dummy system info message.


##### Headers

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| (root) | object | - | - | - | **additional properties are allowed** |
| my-app-header | integer | - | - | [ 0 .. 100 ] | - |
| correlationId | string | - | - | - | - |

> Examples of headers

```json
{
  "my-app-header": 12
}
```


```json
{
  "my-app-header": 13
}
```


##### Payload

| Name | Type | Description | Value | Constraints | Notes |
|---|---|---|---|---|---|
| (root) | object | - | - | - | **additional properties are allowed** |
| prop1 | string | Dummy prop1 | allowed (`"option1"`, `"option2"`) | - | **required** |
| sentAt | string | Date and time when the message was sent. | - | format (`date-time`) | - |

> Examples of payload

```json
{
  "prop1": "option1",
  "sentAt": "2020-01-31T13:24:53.000Z"
}
```


```json
{
  "prop1": "option2",
  "sentAt": "2020-01-31T13:24:53.000Z"
}
```



