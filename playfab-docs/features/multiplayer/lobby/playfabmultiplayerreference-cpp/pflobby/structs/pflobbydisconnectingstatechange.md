---
author: tomcoMSFT
title: "PFLobbyDisconnectingStateChange"
description: "Information specific to the *Disconnecting* type of state change."
ms.author: tomco
ms.topic: reference
ms.prod: playfab
ms.date: 11/23/2021
---

# PFLobbyDisconnectingStateChange  

Information specific to the *Disconnecting* type of state change.  

## Syntax  
  
```cpp
typedef struct PFLobbyDisconnectingStateChange {  
    _Notnull_ lobby;  
    PFLobbyDisconnectingReason reason;  
} PFLobbyDisconnectingStateChange  
```
  
### Members  
  
**`lobby`** &nbsp; _Notnull_  
  
The lobby that has started disconnecting.
  
**`reason`** &nbsp; [PFLobbyDisconnectingReason](../enums/pflobbydisconnectingreason.md)  
  
The reason the lobby started disconnecting.
  
## Remarks  
  
This state change signals that the lobby is in the process of disconnecting because there are no local members actively connected or attempting to reconnect to the lobby. At the point when this state change is provided by [PFMultiplayerStartProcessingLobbyStateChanges()](../functions/pfmultiplayerstartprocessinglobbystatechanges.md), some operations which require a connected lobby object will begin to fail such as [PFLobbyAddMember](../functions/pflobbyaddmember.md).
  
## Requirements  
  
**Header:** PFLobby.h
  
## See also  
[PFLobby members](../pflobby_members.md)  

  
  
