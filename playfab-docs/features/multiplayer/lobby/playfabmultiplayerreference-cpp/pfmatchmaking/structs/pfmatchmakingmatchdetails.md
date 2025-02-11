---
author: tomcoMSFT
title: "PFMatchmakingMatchDetails"
description: "The resulting match information found by a completed ticket."
ms.author: tomco
ms.topic: reference
ms.prod: playfab
ms.date: 11/09/2021
---

# PFMatchmakingMatchDetails  

The resulting match information found by a completed ticket.  

## Syntax  
  
```cpp
typedef struct PFMatchmakingMatchDetails {  
    const char* matchId;  
    const PFMatchmakingMatchMember* members;  
    uint32_t memberCount;  
    const char* regionPreferences;  
    uint32_t regionPreferenceCount;  
    const char* lobbyArrangementString;  
} PFMatchmakingMatchDetails  
```
  
### Members  
  
**`matchId`** &nbsp; const char*  
*_Null_terminated_*  
  
The ID of the match.
  
**`members`** &nbsp; const [PFMatchmakingMatchMember](pfmatchmakingmatchmember.md)*  
  
The users that have been matched together.
  
**`memberCount`** &nbsp; uint32_t  
  
The count of members that have been matched together.
  
**`regionPreferences`** &nbsp; const char*  
  
Preferred regions for the match, sorted from most to least preferred.
  
**`regionPreferenceCount`** &nbsp; uint32_t  
  
The count of preferred regions for the match.
  
**`lobbyArrangementString`** &nbsp; const char*  
*_Null_terminated_*  
  
The lobby arrangement string associated with the match.
  
This connection string can optionally be used with [PFMultiplayerJoinArrangedLobby()](../../pflobby/functions/pfmultiplayerjoinarrangedlobby.md) to join a lobby associated with this match result. The lobby is not created until a user attempts to join it.
  
  
## Requirements  
  
**Header:** PFMatchmaking.h
  
## See also  
[PFMatchmaking members](../pfmatchmaking_members.md)  

  
  
