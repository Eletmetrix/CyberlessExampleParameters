## Parameters

| **Parameter Name** | **Type** | **Is Level Parameter**  | **Description**                                                                                                                                                                                  | **Default Value** |
|--------------------|:--------:|:-----------------------:|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------:|
| ServerPassword     |  string  |           ❌            | The password will be asked while login to server (empty value means no password).                                                                                                               |     *(empty)*     |
| TimeLimit          | integer  |           ✔️            | Match maximum playable time without overtime (0 means infinite time).                                                                                                                           |  15 *(minutes)*   |
| GoalScore          | integer  |           ✔️            | Goal score of player scores or team scores (0 means no goal score).                                                                                                                             |        300        |
| NoKillcam          |   bool   |           ✔️            | Disables kill cam on server.                                                                                                                                                                    |       false       |
| BalanceTeams       |   bool   |           ✔️            | If true it will balance teams on changing team.                                                                                                                                                 |       false       |
| IgnoreIdlePlayers  |   bool   |           ✔️            | If true, server will not kick idle players during traveling to next map.                                                                                                                        |       false       |
| Demorec            |  string  |           ✔️            | Custom demo file name (0 means no match recording, and ExternalServer means livestream through service).                                                                                        |  *(not passed)*   |
| ReplayServerURL    |  string  |           ❌            | Used when ExternalServer value passed to Demorec parameter. Determines livestream service service. See extra details [here](https://github.com/Eletmetrix/UnrealReplayServer/tree/dev)          |  *(not passed)*   |
| LAN                |   bool   |           ❌            | Starts game server as local server.                                                                                                                                                             |  *(not passed)*   |
| SteamServerName    |  string  |           ❌            | Changes visible server name on Steam's server list widget                                                                                                                                       |  *(not passed)*   |


## Example Usage (For Linux)
```shell
# Starts a local server with password and custom server name
./CyberlessOnlineServer.sh /Game/Maps/Warehouse -LAN -ServerPassword=passwd123 -SteamServerName="My Cool Server"
# Starts a server with custom time limit and goal score
./CyberlessOnlineServer.sh /Game/Maps/Warehouse?TimeLimit=20?GoalScore=330
# Starts a server without kill cam system, ignoring idle players and without recording match
./CyberlessOnlineServer.sh /Game/Maps/Warehouse?NoKillcam=1?IgnoreIdlePlayers=1?Demorec=0
# Starts a server with connected to a livestream service
./CyberlessOnlineServer.sh /Game/Maps/Warehouse?Demorec=ExternalServer -ReplayServerURL="https://localhost:8080/"
```

## Example Usage (For Windows)
```bash
# Starts local server with password and custom server name
.\CyberlessOnlineServer.exe /Game/Maps/Warehouse -LAN -ServerPassword=passwd123 -SteamServerName="My Cool Server"
# Starts server with custom time limit and goal score
.\CyberlessOnlineServer.exe /Game/Maps/Warehouse?TimeLimit=20?GoalScore=330
# Starts server without kill cam system, ignoring idle players and without recording match
.\CyberlessOnlineServer.exe /Game/Maps/Warehouse?NoKillcam=1?IgnoreIdlePlayers=1?Demorec=0
# Starts a server with connected to a livestream service
.\CyberlessOnlineServer.exe /Game/Maps/Warehouse?Demorec=ExternalServer -ReplayServerURL="https://localhost:8080/"
```
