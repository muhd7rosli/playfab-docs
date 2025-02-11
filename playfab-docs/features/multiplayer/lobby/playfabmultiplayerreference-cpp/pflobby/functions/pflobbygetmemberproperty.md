---
author: tomcoMSFT
title: "PFLobbyGetMemberProperty"
description: "Get the member property's value from its key."
ms.author: tomco
ms.topic: reference
ms.prod: playfab
ms.date: 11/23/2021
---

# PFLobbyGetMemberProperty  

Get the member property's value from its key.  

## Syntax  
  
```cpp
HRESULT PFLobbyGetMemberProperty(  
    PFLobbyHandle lobby,  
    const PFEntityKey* member,  
    const char* key,  
    const char** value  
)  
```  
  
### Parameters  
  
**`lobby`** &nbsp; PFLobbyHandle  
  
The handle of the lobby.  
  
**`member`** &nbsp; PFEntityKey*  
  
The member whose property bag we want to query.  
  
**`key`** &nbsp; char*  
*_Null_terminated_*  
  
The key of the property.  
  
**`value`** &nbsp; char**  
*library-allocated output, may return nullptr*  
  
The output value associated with the key. An output null value signifies the property wasn't present.  
  
  
### Return value
Type: HRESULT
  
```S_OK``` if the call succeeded or an error code otherwise. The human-readable form of the error code can be retrieved via [PFMultiplayerGetErrorMessage()](../../pfmultiplayer/functions/pfmultiplayergeterrormessage.md).
  
## Remarks  
  
Per-member properties are only visible to members of the lobby. <br /><br /> If the member is still in the process of asynchronously joining this lobby either via [PFMultiplayerCreateAndJoinLobby()](pfmultiplayercreateandjoinlobby.md), [PFMultiplayerJoinLobby()](pfmultiplayerjoinlobby.md), or [PFLobbyAddMember()](pflobbyaddmember.md), this method will return no properties.
  
## Requirements  
  
**Header:** PFLobby.h
  
## See also  
[PFLobby members](../pflobby_members.md)  

  
  
