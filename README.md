# JavaJAM releases

# Basic Usage

```bash
❤ JavaJAM

Usage: ./bin/javajam <COMMAND> [OPTIONS]

Commands:
  gen-spec    Generate new chain spec from the spec config
  gen-keys    Generate a new secret key seed and print the derived session keys
  list-keys   List all session keys we have the secret key for
  run         Run a JavaJAM node
  help        Print this message or the help of the given subcommand(s)

Options:
  -d, --data-path <DATA_PATH>        Base data path
  -c, --config-path <CONFIG_PATH>    Base config path
  --chain <CHAIN>                    Chain to run. "dev", or the path of a chain spec file [default: dev]
  -p, --parameters <PARAMETERS>      Parameter override. If none is specified, the parameters are determined by the `chain` [possible values: full, tiny]
  -l, --log-level <LOG_LEVEL>       Change logging level [default: info] [possible values: trace, info, error]
  -h, --help                         Print help (see more with '--help')
  -V, --version                      Print version
```

# Run options


```bash
% ./javajam run --help

❤ JavaJAM

Usage: ./bin/javajam run [OPTIONS]

Options:
  -d, --data-path <DATA_PATH>        Base data path
  -c, --config-path <CONFIG_PATH>    Base config path
  --chain <CHAIN>                    Chain to run. "dev", or the path of a chain spec file [default: dev]
  -p, --parameters <PARAMETERS>      Parameter override. If none is specified, the parameters are determined by the `chain` [possible values: full, tiny]
  -l, --log-level <LOG_LEVEL>       Change logging level [default: info] [possible values: trace, info, error]
  --peer-id <PEER_ID>                Peer ID of this node.
                                     If not specified, a new peer ID will be generated.
  --external-ip <EXTERNAL_IP>        External IP of this node, as used by other nodes to connect.
  --listen-ip <LISTEN_IP>            IP address to listen on [default: 127.0.0.1]
  --port <PORT>                      UDP port to listen on [default: 0]
  --rpc-listen-ip <RPC_LISTEN_IP>    IP address for RPC server to listen on [default: 127.0.0.1]
  --rpc-port <RPC_PORT>              RPC port to listen on [default: 19800]
  --dev-validator <VALIDATOR>        Configure this node as the dev chain validator with the given index.
  -h, --help                         Print help (see more with '--help')

```

There is no source code available in this repository.