---
id: "structures_preProcessors.MessagePreProcessor"
title: "Type alias: MessagePreProcessor"
sidebar_label: "MessagePreProcessor"
custom_edit_url: null
---

[structures/preProcessors](/api/modules/structures_preProcessors.md).MessagePreProcessor

Ƭ **MessagePreProcessor**: (`message`: [`Message`](/api/interfaces/api_model_message.Message.md), `client?`: [`Client`](/api/classes/api_Client.Client.md), `alreadyProcessed?`: `boolean`, `source?`: ``"onMessage"`` \| ``"onAnyMessage"``) => `Promise`<[`Message`](/api/interfaces/api_model_message.Message.md)\>

#### Type declaration

▸ (`message`, `client?`, `alreadyProcessed?`, `source?`): `Promise`<[`Message`](/api/interfaces/api_model_message.Message.md)\>

A function that takes a message and returns a message.

##### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`Message`](/api/interfaces/api_model_message.Message.md) | The message to be processed |
| `client?` | [`Client`](/api/classes/api_Client.Client.md) | The client that received the message |
| `alreadyProcessed?` | `boolean` | Whether the message has already been processed by another preprocessor. (This is useful in cases where you want to mutate the message for both onMessage and onAnyMessage events but only want to do the actual process, like uploading to s3, once.) |
| `source?` | ``"onMessage"`` \| ``"onAnyMessage"`` | The source of the message. This is useful for knowing if the message is from onMessage or onAnyMessage. Only processing one source will prevent duplicate processing. |

##### Returns

`Promise`<[`Message`](/api/interfaces/api_model_message.Message.md)\>
