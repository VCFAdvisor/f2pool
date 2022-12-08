# Aleo manual

## System

Install Ubuntu 18.04-20.04, server version, without GUI components

## GPU

- NVIDIA: Driver version 515 and above (Example: 515.78)

## Start-up command

Download the ‘aleo.sh’ and ‘aleo-prover-cuda’ files, configure the mining parameters in aleo.sh file and start mining.
- Modify `ACCOUNT_NAME=accountname` in the aleo.sh file to set `accountname` to your f2pool account name
- Modify `POOL="xxx.xxx.xxx.xxx:xxxx"` in the aleo.sh file. If you choose to connect to the non-SSL server,  `POOL="aleo-asia.f2pool.com:4400"` . If you you choose to connect to the SSL server, set `xxx.xxx.xxx.xxx:xxxx` to the proxy address of your [stunnel](#stunnel installation). [Related guide](https://f2pool.io/mining/guides/how-to-mine-aleo/?_ga=2.261973965.1760295878.1670166632-1277269998.1658672539).
- Start the software `chmod +x aleo.sh && . /aleo.sh`

## View log

- Hashrate
  - 1m: the average number of prover_solutions produced per second in the last 1 minute
  - 5m: the average number of prover_solutions generated per second in the last 5 minutes
  - perf: followed by a number indicating the total number of prover_solutions generated