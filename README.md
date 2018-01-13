# ccminer-dace-cryptonight, a ccminer mod by tsiv, KlausT and Dace 
Modified by Dace for uninterrupted CUDA 9.1 CPU mining with no automatic donation pool redirections.

If you find this tool useful and like to support its continued development, then consider a donation to any of the relevant developers below.

## Dace's donation addresses:
* ETN donation address: etnjwVuF4zuC8q2zfxCX4RgdV7jNcM5pkZdDdC6GaTy68Qb4Wu9vfJwPd3ctp6mGFgfiYyoKn14BhPErDpFy8obD39rN9zHUPe
* FTC donation address: 6s1mzQ21zxD8DSF3Gnyj73dN25XUdJMjQa

## KlausT's donation addresses:
* BTC: 1QHH2dibyYL5iyMDk3UN4PVvFVtrWD8QKp
* BCH: 1AH1u7B4KtDTUBgmT6NrXyahNEgTac3fL7

## tsiv's donation adresseses:
* BTC: 1JHDKp59t1RhHFXsTw2UQpR3F9BBz3R3cs
* XMR: 42uasNqYPnSaG3TwRtTeVbQ4aRY3n9jY6VXX3mfgerWt4ohDQLVaBPv3cYGKDXasTUVuLvhxetcuS16ynt85czQ48mbSrWX

## Introduction

This is an optimized CUDA 9.1 CPU mining application for use with Monero, Electronium and other coins based on the Cryptonight algorithm with no donation pool mining.

THIS PROGRAM IS PROVIDED "AS-IS", USE IT AT YOUR OWN RISK!

## Command Line Options
```
 -d, --devices         gives a comma separated list of CUDA device IDs
                       to operate on. Device IDs start counting from 0!
                       Alternatively give string names of your card like
                       gtx780ti or gt640#2 (matching 2nd gt640 in the PC).
 -l, --launch=CONFIG   launch config for the Cryptonight kernel.
                       a comma separated list of values in form of
                       AxB where A is the number of threads to run in
                       each thread block and B is the number of thread
                       blocks to launch. If less values than devices in use
                       are provided, the last value will be used for
                       the remaining devices. If you don't need to vary the
                       value between devices, you can just enter a single
                       value and it will be used for all devices.
     --bfactor=X       Enables running the Cryptonight kernel in smaller pieces.\n\
                       The kernel will be run in 2^X parts according to bfactor,\n\
                       with a small pause between parts, specified by --bsleep.\n\
                       This is a per-device setting like the launch config.\n\
                       (default: 0 (no splitting) on Linux, 6 (64 parts) on Windows)\n\
     --bsleep=X        Insert a delay of X microseconds between kernel launches.\n\
                       Use in combination with --bfactor to mitigate the lag\n\
                       when running on your primary GPU.\n\
                       This is a per-device setting like the launch config.\n\
 -f, --diff            Divide difficulty by this factor (std is 1) 
 -o, --url=URL         URL of mining server (default: " DEF_RPC_URL ")
 -O, --userpass=U:P    username:password pair for mining server
 -u, --user=USERNAME   username for mining server
 -p, --pass=PASSWORD   password for mining server
     --cert=FILE       certificate for mining server using SSL
 -x, --proxy=[PROTOCOL://]HOST[:PORT]  connect through a proxy
 -t, --threads=N       number of miner threads
                       (default: number of nVidia GPUs in your system)
 -r, --retries=N       number of times to retry if a network call fails
                         (default: retry indefinitely)
 -R, --retry-pause=N   time to pause between retries, in seconds (default: 15)
 -T, --timeout=N       network timeout, in seconds (default: 270)
 -k, --keepalive       send keepalive requests to avoid a stratum timeout
 -s, --scantime=N      upper bound on time spent scanning current work when
                       long polling is unavailable, in seconds (default: 5)
     --no-longpoll     disable X-Long-Polling support
     --no-stratum      disable X-Stratum support
 -q, --quiet           disable per-thread hashmeter output
 -D, --debug           enable debug output
     --color           enable color output
 -P, --protocol-dump   verbose dump of protocol-level activities
 -B, --background      run the miner in the background (Linux only)
     --benchmark       run in offline benchmark mode
 -c, --config=FILE     load a JSON-format configuration file
 -V, --version         display version information and exit
 -h, --help            display this help text and exit
```

## AUTHORS

Notable contributors to this application are:

Dace: 
- some minor performance improvements to retry times and removal of automated pool donations.
- updated readme.md for optional manual donations by address if user chooses to do so and wants to further support development.
- Updated code to support Cuda 9.1 from Cuda 9.0

KlausT:
- various fixes and optimizations

tsiv: 
- CUDA 9.0 implementation for the Cryptonight algorithm.

Christian Buchner, Christian H. (Germany): 
- modifying the original pooler-cpuminer for use with CUDA.

Jeff Garzik, pooler + contributors:
- The original pooler-cpuminer project

LucasJones:
 - JSON-RPC 2.0 handling and the Cryptonight C-code comes
   from his cpuminer fork, cpuminer-multi

* Don't forget to support the original ccminer authors
Christian Buchner and Christian H. This mod would not be
here without their work on ccminer:

* LTC donation address: LKS1WDKGED647msBQfLBHV3Ls8sveGncnm
* BTC donation address: 16hJF5mceSojnTD3ZTUDqdRhDyPJzoRakM
* YAC donation address: Y87sptDEcpLkLeAuex6qZioDbvy1qXZEj4
* VTC donation address: VrjeFzMgvteCGarLw85KivBzmsiH9fqp4a
* MAX donation address: mHrhQP9EFArechWxTFJ97s9D3jvcCvEEnt
* DOGE donation address: DT9ghsGmez6ojVdEZgvaZbT2Z3TruXG6yP
* HVC donation address: HNN3PyyTMkDo4RkEjkWSGMwqia1yD8mwJN
* GRS donation address: FmJKJAhvyHWPeEVeLQHefr2naqgWc9ABTM
* MYR donation address: MNHM7Q7HVfGpKDJgVJrY8ofwvmeugNewyf
* JPC donation address: JYFBypVDkk583yKWY4M46TG5vXG8hfgD2U
* SFR donation address: SR4b87aEnPfTs77bo9NnnaV21fiF6jQpAp
* MNC donation address: MShgNUSYwybEbXLvJUtdNg1a7rUeiNgooK
* BTQ donation address: 13GFwLiZL2DaA9XeE733PNrQX5QYLFsonS

Source code is included to satisfy GNU GPL V3 requirements.