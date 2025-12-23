# XMRig Proxy
[![Github All Releases](https://img.shields.io/github/downloads/bendr0id/xmrigcc-proxy/total.svg)](https://github.com/bendr0id/xmrigcc-proxy/releases)
[![Github Latest](https://img.shields.io/github/downloads/bendr0id/xmrigCC-proxy/latest/total.svg)](https://github.com/bendr0id/xmrigcc-proxy/releases)
[![GitHub release](https://img.shields.io/github/release/bendr0id/xmrigcc-proxy/all.svg)](https://github.com/bendr0id/xmrigcc-proxy/releases)
[![GitHub Release Date](https://img.shields.io/github/release-date-pre/bendr0id/xmrigcc-proxy.svg)](https://github.com/bendr0id/xmrigcc-proxy/releases)
[![GitHub license](https://img.shields.io/github/license/bendr0id/xmrigcc-proxy.svg)](https://github.com/bendr0id/xmrigcc-proxy/blob/master/LICENSE)

Extremely high performance Monero (XMR) Stratum protocol proxy, can easily handle over 100K connections on cheap $5 (1024 MB) virtual machine. Reduce number of pool connections up to 256 times, 100K workers become just 391 worker on pool side. Written on C++/libuv same as [XMRigCC](https://github.com/bendr0id/xmrigCC) miner.

**This proxy is compatible with XMRigCC**

## Compatibility

:warning: :warning: :warning: **This proxy is compatible with all algos supported by the latest version of XMRigCC** :warning: :warning: :warning:

**Nicehash support must be enabled on miner side, it mandatory.**

* Compatible with any Monero, Electroneum, Sumokoin and AEON pools, except **nicehash.com**.
* Any miner with nicehash support, `--nicehash` option for [XMRig(CC)](https://github.com/bendr0id/xmrigCC), `"nicehash_nonce": true,` for xmr-stak-cpu.
* [Comparison](https://github.com/xmrig/xmrig-proxy/wiki/Comparison) with other proxies.

## Why?
This proxy is designed to handle donation traffic from XMRig. No other solution works well with high connection and disconnection rates.

## Download
* Binary releases: https://github.com/bendr0id/xmrigcc-proxy/releases
* Git tree: https://github.com/bendr0id/xmrigcc-proxy.git
  * Clone with `git clone https://github.com/bendr0id/xmrigcc-proxy.git` :hammer: [Build instructions](https://github.com/xmrig/xmrig-proxy/wiki/Build).
  
## Usage
:boom: If you are using Linux and need to manage over **1000 connections**, you must [increase the limits on open files](https://github.com/xmrig/xmrig-proxy/wiki/Ubuntu-setup).
  
### Options
```
  -b, --bind=ADDR          bind to specified address, example "0.0.0.0:3333"
  -a, --algo=ALGO          mining algorithm (--algorithms to print supported)
      --coin=COIN          specify coin instead of algorithm
  -m, --mode=MODE          proxy mode, nicehash (default) or simple
  -o, --url=URL            URL of mining server
  -O, --userpass=U:P       username:password pair for mining server
  -u, --user=USERNAME      username for mining server
  -p, --pass=PASSWORD      password for mining server
  -r, --retries=N          number of times to retry before switch to backup server (default: 1)
  -R, --retry-pause=N      time to pause between retries (default: 1 second)
      --custom-diff=N      override pool diff
      --reuse-timeout=N    timeout in seconds for reuse pool connections in simple mode
      --verbose            verbose output
      --user-agent=AGENT   set custom user-agent string for pool
      --no-color           disable colored output
      --no-workers         disable per worker statistics
      --variant            algorithm PoW variant
      --donate-level=N     donate level, default 2%
  -B, --background         run the miner in the background
  -c, --config=FILE        load a JSON-format configuration file
      --no-watch           disable configuration file watching
  -l, --log-file=FILE      log all output to a file
  -S, --syslog             use system log for output messages
  -A  --access-log-file=N  log all workers access to a file
      --api-port=N         port for the miner API
      --api-access-token=T use Bearer access token for API
      --api-worker-id=ID   custom worker-id for API
      --api-no-ipv6        disable IPv6 support for API
      --api-no-restricted  enable full remote access (only if API token set)
      --tls                enable SSL/TLS support for pool connection (needs pool support)
      --tls-bind=ADDR      bind to specified address with enabled TLS
      --tls-cert=FILE      load TLS certificate chain from a file in the PEM format
      --tls-cert-key=FILE  load TLS certificate private key from a file in the PEM format
      --tls-dhparam=FILE   load DH parameters for DHE ciphers from a file in the PEM format
      --tls-protocols=N    enable specified TLS protocols, example: "TLSv1 TLSv1.1 TLSv1.2 TLSv1.3"
      --tls-ciphers=S      set list of available ciphers (TLSv1.2 and below)
      --tls-ciphersuites=S set list of available TLSv1.3 ciphersuites 
  -h, --help               display this help and exit
  -V, --version            output version information and exit
      --algorithms         prints out a list of supported algos
```

## Contact
* ben [at] graef.in
* [telegram](https://telegram.me/bendr0id)
* [discord](https://discord.gg/r3rCKTB)
* [reddit](https://www.reddit.com/user/BenDr0id/)
