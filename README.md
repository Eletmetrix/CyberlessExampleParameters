## Parameters

| **Parameter Name** | **Type** | **Is Level Parameter**  | **Description**                                                                   | **Default Value** |
|--------------------|:--------:|:-----------------------:|-----------------------------------------------------------------------------------|:-----------------:|
| ServerPassword     |  string  |           ❌            | The password will be asked while login to server (empty value means no password). |     *(empty)*     |
| TimeLimit          | integer  |           ✔️            | Match maximum playable time without overtime (0 means infinite time).             |  15 *(minutes)*   |
| GoalScore          | integer  |           ✔️            | Goal score of player scores or team scores (0 means no goal score).               |        300        |
| NoKillcam          |   bool   |           ✔️            | Disables kill cam on server.                                                      |       false       |
| BalanceTeams       |   bool   |           ✔️            | If true it will balance teams on changing team                                    |       false       |
| IgnoreIdlePlayers  |   bool   |           ✔️            | If true, server will not kick idle players during traveling to next map           |       false       |
| Demorec            |  string  |           ✔️            | Custom demo file name (0 means no match recording).                               |  *(not passed)*   |
| LAN                |   bool   |           ❌            | Starts game server as local server.                                               |  *(not passed)*   |


## Example Usage (For Linux)
```shell
# Starts local server with password
./CyberlessIIIOnlineServer.sh /Game/Maps/Warehouse -LAN -ServerPassword=passwd123
# Starts server with custom time limit and goal score
./CyberlessIIIOnlineServer.sh /Game/Maps/Warehouse?TimeLimit=20?GoalScore=330
# Starts server without kill cam system, ignoring idle players and without recording match
./CyberlessIIIOnlineServer.sh /Game/Maps/Warehouse?NoKillcam=1?IgnoreIdlePlayers=1?Demorec=0
```

## Example Usage (For Windows)
```bash
# Starts local server with password
.\CyberlessIIIOnlineServer.exe /Game/Maps/Warehouse -LAN -ServerPassword=passwd123
# Starts server with custom time limit and goal score
.\CyberlessIIIOnlineServer.exe /Game/Maps/Warehouse?TimeLimit=20?GoalScore=330
# Starts server without kill cam system, ignoring idle players and without recording match
.\CyberlessIIIOnlineServer.exe /Game/Maps/Warehouse?NoKillcam=1?IgnoreIdlePlayers=1Demorec=0
```
