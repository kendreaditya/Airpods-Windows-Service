# The project is being developed and has not release yet.

# Airpods Windows Service

A Windows Service for reading Airpods Battery and some other informations.
Using this service, you can get your Airpods data as JSON over the UDP socket.

## Requirements
- Windows 10, version 16299 (Fall Creators Update) or greater
- Bluetooth 4.0+

## Installation
1. Download/clone project
2. Run "python service.py install" in cmd as Administrator or simply click "register-service.bat" two times
3. Run Service on Windows Services
4. After first run, config file automatically created on your userpath as ".airpods-config.json".
You can change the UDP port using this config.

## Usage
While the service is running, it will automatically send JSON data over the UDP port you set in the config file.
The data looks like the following. You can use this JSON data in any application you create.

```
{
   "status":0, //IF AIRPODS FOUND IT RETURNS 1
   "error":"", //IF ANY ERROR OCCURED, IT IS HERE
   "rssi":-670, //RECEIVED SIGNAL STRENGTH INDICATION
   "addr":"" //MAC ADDRESS FROM WHICH DATA IS TAKEN
}
```

## Referances
- [tzY15368](https://github.com/tzY15368)/**[WinPods](https://github.com/tzY15368/WinPods)**
- [adolfintel](https://github.com/adolfintel)/**[OpenPods](https://github.com/adolfintel/OpenPods)**

## Copyright and License
**Airpods Windows Service** is licensed under the GNU General Public License v3.0.