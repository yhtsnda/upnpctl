# upnpctl

Usage:

```
           _________   _...._         _..._   _________   _...._        .' .'      '.\      |   |
           \        |.'      '-.    .'     '. \        |.'      '-.    / .'                 |   |
            \        .'''''.    '. .   .-.   . \        .'''''.    '. . '               .|  |   |
             \      |       \     \|  '   '  |  \      |       \     \| |             .' |_ |   |
   _    _     |     |        |    ||  |   |  |   |     |        |    || |           .'     ||   |
  | '  / |    |      \      /    . |  |   |  |   |      \      /    . . '          '--.  .-'|   |
 .' | .' |    |     |\''-.-'   .'  |  |   |  |   |     |\''-.-'   .'   \ '.          .|  |  |   |
 /  | /  |    |     | '-....-''    |  |   |  |   |     | '-....-''      '. '._____.-'/|  |  |   |
|   ''.  |   .'     '.             |  |   |  |  .'     '.                 '-.______ / |  '.''---'
'   .'|  '/'-----------'           |  |   |  |'-----------'                        '  |   /
 '-'  '--'                         '--'   '--'                                        ''-'

Usage:
  upnpctl [flags]
  upnpctl [command]

Available Commands:
  help        Help about any command
  scan        Scan the network for possible Devices and persist them
  serve       Serve a UPNP honeypot that receives all the events and eventually persists them

Flags:
  -h, --help   help for upnpctl

Use "upnpctl [command] --help" for more information about a command.
```

## Example Usages

### Scanning

Save a scan of your local network to a json file:

```
upnpctl scan > /tmp/scan.json
```

#### Usage:

``` 
Scan the network for possible Devices and persist them

Usage:
  upnpctl scan [flags]

Flags:
  -h, --help       help for scan
  -j, --json       --json (default true)
  -n, --num int    --num <num> (default 10)
  -w, --wait int   --wait <num> (default 30)
```

### Monitor


Monitor the device discovery (or other httpu packages):

```
upnpctl serve
```

#### Usage:
``` 
Serve a UPNP honeypot that receives all the events and eventually persists them

Usage:
  upnpctl serve [flags]

Flags:
  -a, --addr string    --addr <hostname>:<port> (default "239.255.255.250:1900")
  -h, --help           help for serve
  -i, --iface string   --iface <interfacename>
  -m, --multicast      --multicast <true|false> (default true)
```