---
title: "chatMessage: unsetReaction"
description: "Unset areaction to a single message or message reply in a channel or a chat."
author: "Sumana Chakrabarti"
ms.prod: "microsoft-teams"
doc_type: apiPageType
ms.localizationpriority: medium
---

# chatMessage: unsetReaction

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Unset a reaction to a single [message](../resources/chatmessage.md) or a [message reply](../resources/chatmessage.md) in a [channel](../resources/channel.md) or a [chat](../resources/chat.md).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

### Permissions for channel

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
|Delegated (work or school account)| ChannelMessage.Send,  |
|Delegated (personal Microsoft account)| Not supported. |
|Application| Not supported. |

### Permissions for chat

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
|Delegated (work or school account)| Chat.ReadWrite, ChatMessage.Send |
|Delegated (personal Microsoft account)| Not supported. |
|Application| Not supported. |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{userId}/chats/{chatsId}/messages/{chatMessageId}/unsetReaction
POST /teams/{teamsId}/channels/{channelId}/messages/{chatMessageId}/unsetReaction
POST /teams/{teamId}/channels/{channelId}/messages/{messageId}/replies/{replyId}/unsetReaction
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

In the request body, supply the **reactionType** as unicode.

## Response

If successful, this action returns a `204 No Content` response code.

## Examples

### Example 1: Unset a reaction to a chat message

#### Request

```http
POST https://graph.microsoft.com/beta/chats/chatId/messages/messageId/unsetReaction
{
  "reactionType": "💘"
}
```

#### Response

<!-- {
  "blockType": "response"
} -->

```http
HTTP/1.1 204 No Content
```

### Example 2: Unset a reaction to a message in a channel

#### Request
```http
POST https://graph.microsoft.com/beta/teams/teamsid/channels/channelId/messages/messageId/unsetReaction
{
  "reactionType": "💘"
}
```

#### Response

<!-- {
  "blockType": "response"
} -->

``` http
HTTP/1.1 204 No Content
```

### Example 3:  Unset a reaction to a message reply

#### Request

```http
POST https://graph.microsoft.com/beta/teams/teamsid/channels/channelId/messages/messageId/replies/replyId/unsetReaction
{
  "reactionType": "💘"
}
```

#### Response

<!-- {
  "blockType": "response"
} -->

```http
HTTP/1.1 204 No Content
```
