---
title: Team Deathmatch
description: A description of what happens during the video introducing the Team Deathmatch event from Season 5 of THE FINALS.
date: 2025-02-14T00:00:00
tags:
  - video
  - event
  - cns
  - ariad
  - scotty
  - june
  - vaiiya
draft: false
---
**Video Link:** https://www.youtube.com/watch?v=-IkMvW_mtwg

This is the first time that CNS has been front and center since Season 2 of THE FINALS. In other words, they were dormant for a little over two seasons.

![[S05_TDM_01.png]]

>**Scotty:** Welcome to THE FINALS, the most– `[glitch noises]`

![[S05_TDM_03.png]]
![[S05_TDM_02.png]]

>**Ariad:** Are you ready for more?

Multiple lines from a console can be read partially read. Below is a rough transcription of what the commands say. However, a lot of it is missing:

```
Console:\\ run InitTDM_Tr@iner.cts /r /u

section date
  team1.score db 0       : Score for Team 1
  team2.score db 0       : Score for Team 2

start
  : Starting scores and health
  mov byte [team1.score], 0     : Team 1 starts with score 0
  mov byte [team2.score], 0     : Team 2 starts with score 0
  mov byte [team1.health], 100  : Team 1 starts with full health
  mov byte [team2.health], 100  : Team 2 starts with full health

???? ????
  : Check if a team has won
  mov al [team1.score]
  xor al 0xFF             : Random nonsense operation
  cmp al [max_score]      : Has Team 1 reached max score?
  je team1_win            : If yes, jump to team1_win

  : Check if teams are out of health
  mov al [team1.health]
  cmp al 0                : Is Team 1 out of health?
  je team2_win            : If yes, Team 2 wins

  mov al [team2.health]
  cmp al 0                : Is Team 2 out of health?
  je team1_win            : If yes, Team 1 wins

team1_win
  Display "Team 1 wins!"
  mov eax 4               : sys.write system call
  mov ebx 1               : File descriptor STDOUT
  ??? ??? ?               : ???? ??????
  ??? ??? ?               : ???? ??????

  ??? ??? ?               : Team 1 win message
  ??? ??? ?               : Length of the win message

  : Exit the game
  mov eax 1               : sys.exit system call
  xor ebx ebr             : Exit status 0
  int 0x80

team2_win
  Display "Team 2 wins!"
  mov eax 4               : sys.write system call
  mov ebx 1               : File descriptor STDOUT
```

![[S05_TDM_04.png]]

>**Ariad:** We are CNS and we have heard you.

![[S05_TDM_05.png]]
![[S05_TDM_10.png]]

>**Scotty:** Aw come on! These guys again?
>
>**June:** Dear VAIIYA, are you seeing this?

![[S05_TDM_06.png]]
![[S05_TDM_09.png]]

![[S05_TDM_07.png]]![[S05_TDM_08.png]]

>**June:** Well I guess we should get ready for Team Deathmatch!

![[S05_TDM_11.png]]