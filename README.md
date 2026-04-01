# JavaJAM releases

There is no source code available in this repository.

# Prerequisites

- JDK 25+

```bash
# install Java 25+ (if needed)
sudo apt install openjdk-25-jdk
```
# Installation

```bash
# Download latest release (additional OS versions are available as well)
curl -O -L https://github.com/javajamio/javajam-releases/releases/latest/download/javajam-linux-x86_64.zip
   
unzip javajam-linux-x86_64.zip
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
  -l, --log-level <LOG_LEVEL>        Logging level [default: info]
  --log-file <LOG_FILE>              Log file [default: logs/javajam.log]
  -h, --help                         Print help
  -V, --version                      Print version
```

# Run options


```bash
% ./bin/avajam run --help

❤ JavaJAM

Usage: ./bin/javajam run [OPTIONS]

Options:
  -d, --data-path <DATA_PATH>        Base data path
  -c, --config-path <CONFIG_PATH>    Base config path
  --chain <CHAIN>                    Chain to run. "dev", or the path of a chain spec file [default: dev]
  -l, --log-level <LOG_LEVEL>        Change logging level [default: info] [possible values: trace, info, error]
  --peer-id <PEER_ID>                Peer ID of this node.
  --external-ip <EXTERNAL_IP>        External IP address
  --telemetry <TELEMETRY>            IP and port of JAM Tart [format: HOST:PORT]
  --pvm-backend <PVM_BACKEND>        PVM override [values: interpreter, recompiler]
  --listen-ip <LISTEN_IP>            IP to listen on [default: 0.0.0.0]
  --port <PORT>                      UDP port [default: 0]
  --rpc-listen-ip <RPC_LISTEN_IP>    RPC IP [default: 127.0.0.1]
  --rpc-port <RPC_PORT>              RPC port [default: 19800]
  --dev-validator <VALIDATOR_NUM>    Configure this node as a dev validator
  -h, --help                         Print help
   ```

# Run Example
```bash
% ./bin/javajam run --chain conf/polkajam-spec.json --dev-validator 0 --port 40001 --rpc-port 19800

21:07:16.964 INFO  ❤️ JavaJAM
21:07:16.968 INFO  📝 Parameters: Custom
21:07:16.969 INFO  🧬 Genesis (Header Hash: 0x2bf1...5716)
21:07:16.969 INFO  ℹ️ Peer ID: 0x4418...9ace
21:07:18.828 INFO  🗄️ RocksDB initialized (Location: node0/datastore)
```

# Fuzzer target options


```bash
% ./bin/javajam fuzz --help

❤ JavaJAM

Usage: ./bin/javajam fuzz <FUZZ_SOCKET>

Arguments:
  <FUZZ_SOCKET>  Named unix socket for fuzzer to connect too. Ex: /tmp/jam_target.sock
  -h, --help                         Print help


```