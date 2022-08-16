## Parameters

| **Parameter Name** | **Type** | **Is Level Parameter** | **Description**                                                                   | **Default Value** |
| ------------------ | :------: | :--------------------: | --------------------------------------------------------------------------------- | :---------------: |
| ServerPassword     |  string  |           ✔️           | The password will be asked while login to server (empty value means no password). |     *(empty)*     |
| LAN                |   bool   |           ❌           | Starts game server as local server.                                               |   *(not passed)*  |


## Example Usage
```shell
# Starts local server with password
./CyberlessIIIOnlineServer.sh /Game/Maps/DM-DeepForest?ServerPassword=passwd123 -LAN
```
