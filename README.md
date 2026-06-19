# Arctium Game Launcher (Public version)
A game launcher for World of Warcraft that allows you to connect to custom servers with a valid tls certificate attached.

**NOTE**: This is not the full-featured launcher. For mod loading, developer mode, extended tooling, and binary releases, use the official launcher at https://arctium.io

### License, Copyright & Contributions

Please see our Open Source project [Documentation Repo](https://github.com/Arctium/Documentation)

## Important Scope & Limitations

This public launcher has a very strict and intentionally limited feature set.

### What was removed
- No developer mode
- No Arctium server connection  
  (Names remain unchanged by design)
- No mod loading
- No experimental or legacy features
- No binary releases
- No support for deprecated client branches

If you need any of the above, please use the full-featured launcher

### What This Launcher Can Do

- Launch modern World of Warcraft clients
- Connect to custom servers with a valid TLS certificate attached
- Allow custom client version & cdn urls  
  Useful for launching older clients or serving data from your own CDN

## Supported Clients
| Client Branch | Min Supported Version | Max Supported Version |
|-------------------------|------------|------------|
| Mainline                | 10.1.5     | **12.0.5** |
| Classic Era             | 1.14.4     | **\*** |
| Classic                 | 3.4.2      | **5.5.3** |
| Classic Anniversary     | 2.5.5      | **\*** |
| Classic Titan           | 3.80.0     | **\*** |

**\* = all future versions in that branch (unless otherwise stated)**

## Special Request <3
Please do NOT remove the name `arctium` from the final binary.
Blizzard filters their crash logs based on localhost and the string `arctium` in the binary name. 

### NOTE FOR SERVER CONNECTIONS
* A valid certificate matching your authentication/bnet server host name.
  That certificate needs to be loaded by the authentication/bnet server too

### Binary Releases
There are no binary releases of this version. Our **full-featured** launcher has binary releases at https://arctium.io

## Building

### Build Prerequisites
* [.NET Core SDK 10.0.0 or later](https://dotnet.microsoft.com/download/dotnet/10.0)
* Optional for native builds: C++ workload through Visual Studio 2026 or latest C++ build tools

### Build Instructions Windows (native)
* Execute `dotnet publish -r win-x64 -c Configuration -p:platform="x64" -p:PublishAot=true`
* Native output is placed in the `build` folder.

## Usage

### Windows Usage
1. Copy `Actium Game Launcher.exe` to your World of Warcraft folder.
2. Edit the `WTF/Config.wtf` to set your portal or use a different config file with the `-config Config2.wtf` launch arg.
3. Run the `Actium Game Launcher.exe`

### Launch Parameters
Use `--help`
