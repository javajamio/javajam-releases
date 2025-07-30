# JavaJAM releases

There is no source code available in this repository.

# Prerequisites

- JDK 21+

```bash
# install Java 21+ (if needed)
sudo apt install openjdk-21-jdk
```
   
# Basic Usage

```bash
❤ JavaJAM

Usage: ./bin/javajam <COMMAND> [OPTIONS]

Commands:
  gen-spec    Generate new chain spec from the spec config
  gen-keys    Generate a new secret key seed and print the derived session keys
  list-keys   List all session keys we have the secret key for
  fuzz        Listen for connection from JAM conformance fuzzer
  run         Run a JAM node
  help        Print this message or the help of the given subcommand(s)

Options:
  -d, --data-path <DATA_PATH>        Base data path
  -c, --config-path <CONFIG_PATH>    Base config path
  --chain <CHAIN>                    Chain to run [default: tiny]
  -p, --parameters <PARAMETERS>      Parameter override [values: tiny, full]
  -l, --log-level <LOG_LEVEL>        Logging level [default: info]
  --log-file <LOG_FILE>              Log file [default: logs/javajam.log]
  -h, --help                         Print help
  -V, --version                      Print version
```

# Run options


```bash
% ./bin/javajam run --help

❤ JavaJAM

Usage: ./bin/javajam run [OPTIONS]

Options:
  -d, --data-path <DATA_PATH>        Base data path
  -c, --config-path <CONFIG_PATH>    Base config path
  --chain <CHAIN>                    Chain to run [default: tiny]
  -p, --parameters <PARAMETERS>      Parameter override [values: tiny, full]
  -l, --log-level <LOG_LEVEL>        Logging level [default: info]
  --log-file <LOG_FILE>              Log file [default: logs/javajam.log]
  --peer-id <PEER_ID>                Peer ID of this node
  --external-ip <EXTERNAL_IP>        External IP address
  --listen-ip <LISTEN_IP>            IP to listen on [default: 127.0.0.1]
  --port <PORT>                      UDP port [default: 0]
  --rpc-listen-ip <RPC_LISTEN_IP>    RPC IP [default: 127.0.0.1]
  --rpc-port <RPC_PORT>              RPC port [default: 19800]
  --dev-validator <VALIDATOR>        Configure this node as a dev validator
  -h, --help                         Print help

```