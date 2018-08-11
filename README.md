<p align="center"><img width=50% src="/imgs/logo-with-text.png"></img></p>
<p align="center">a simple, handy network addressing multitool with plenty of features</p>
<p align="center">
  <a href="ship.sh"><img src="https://img.shields.io/badge/version-2.6.2-blue.svg?style=flat-square&colorA=13818d&colorB=44c2c7"></a>
    &nbsp;
  <a href="LICENSE.md"><img src="https://img.shields.io/badge/license-GPL%20v3%2B-yellow.svg?style=flat-square&colorA=13818d&colorB=44c2c7"></a>
    &nbsp;
  <a href="http://tldp.org/LDP/abs/html/bashver3.html#AEN20987"><img src="https://img.shields.io/badge/bash-3.2+-lightgrey.svg?style=flat-square&colorA=13818d&colorB=44c2c7"></a>
    &nbsp;
</p>

---

### Features

* [x] Show all network **interfaces**
* [x] Show all active network **interfaces**
* [x] Show the **driver** used of each active network interface
	* [ ] link displayed **driver** to correct interface
* [x] Show the **gateway** of each online interface
* [x] Show the addresses of each active network interface with/without CIDR notation
  * [x] **IPv4**
  * [x] **IPv6** (*if possible*)
  * [x] **MAC**
* [x] Show the **public/external IP/s**
  * [x] of user
  * [x] of website / domain
* [x] Show **active hosts** on current network with/without MAC address
* [x] Show all valid addresses (IPv4, IPv6, MAC) extracted
  * [x] from **file** or multiple **files** at once
  * [x] from **website** or multiple **websites** at once
* [x] Show the **route** to a network host using three most common tools. `ship` checks which are installed and decides to run the fastest one for each case scenario
  * [x] **IPv4**
  * [x] **IPv6** (*if possible*)
* [x] Show the **broadcast** and **network** address, cisco **wildcard** mask, **class** and **host range** by giving the IP address and CIDR or netmask
  * [x] **IPv4**
  * [x] optionally suppress the bitwise output
  * [x] display results as HTML
  * [x] split into networks of size `n1, n2, n3` :construction:
  * [x] de-aggregate address range :construction:
* [x] Show list of **common ports** with description, **private** and **reserved** IPv4 and IPv6 addresses with or without CIDR notation
* [x] Compatible with most of the common linux distributions
* [x] Drag and drop URLs or file paths on console window
* [x] Cleaning temp files and handling remaining tasks on exit
* [x] Exiting on long running tasks needs confirmation

---      

### Usage

Read the [Guide]. Usage and some interactive examples are there for you :ship:

---

### (macOS)Requirements

 :wrench:    | (Homebrew)Package               | Severity       
:------------|:--------------------------------|:---------------------
 `awk`       | [✔] `Homebrew/coreutils`       | :small_red_triangle: 
 `gsed`      | [✔] `Homebrew/coreutils`       | :small_red_triangle: 
 `ggrep`     | [✔] `Homebrew/[tap]dupe/ggrep` | :small_red_triangle:
 `ip`        | [✔] `Homebrew/iproute2mac`     | :small_red_triangle: 
 `mtr`       | [✔] `Homebrew/mtr`             | :large_blue_circle:  
 `ping`      | [✔] `macOS/ Native`            | :small_red_triangle: 
 *`ss`*      | [✘] *`iproute2`*               | :small_red_triangle: 
 `tracepath` | [✔] `Homebrew/bwctl`           | :large_blue_circle:  
 `traceroute`| [✔] `macOS/ Native`            | :large_blue_circle:  
 `wget`      | [✔] `macOS/ Native`            | :small_red_triangle: 

 Symbol               | Meaning
:---------------------|:---------------------------------------------------------
 :small_red_triangle: | the script doesn't work without them                     
 :large_blue_circle:  | there should be installed at least one of those packages 

Of course, the script uses some of the tools included in **coreutils** and shell builtins

#### NOTE

`ship` utilizes the functionality of `ping` to check and validate LAN and WAN connections

* **CAP_NET_RAW** capability should be permitted
* Kernel must support non-raw ICMP sockets
* User must be allowed to create ICMP echo sockets
* macOS: `Homebrew` must be installed
* macOS: Homebrew formula: `coreutils` (for: `gawk, gcut, gmktemp, grm, gsort, gtail`) must be installed
* macOS: Homebrew formula: `ggrep` must be installed

---

### Compatibility

 :penguin: | Version             
:----------|:--------------------
 Arch      | 4.7.5-1 - 4.11.9-1  
 Debian    | 7 - 8               
 Kali      | 2016.2              
 Ubuntu    | 14.04.3 - 16.04.1
 **macOS** | **10.x - 10.14 (Beta) w/ Homebrew**   

---

### Getting Started

```bash
$ git clone --branch=master https://github.com/LaurentFough/ship.git
$ cd /path/to/ship
$ bash ship.sh
```

---

### Contribution

Pull requests, issues, suggestions, testing and feedback are all welcome

* Fork the repo
* Create a new branch
  * `$ git checkout -b my-new-feature`
* Make the appropriate changes in the files
* Add changes to reflect the changes made
* Commit your changes
  * `$ git commit -am 'Added some feature'`
* Push to the branch
  * `$ git push origin my-new-feature`
* Create a Pull Request on `contributors`

---

### Changelog

Read the [Changelog] file to review changes

---

### Contact

Send me an email at [laurent.fough@gmail.com]

----

### License

Copyright (c) **2017** by **Sotirios M. Roussis**. Some rights reserved


`ship` is under the terms of the GPLv3+ License, following all clarifications stated in the [license] file

<!-- Links -->

[Guide]: GUIDE.md
[Changelog]: CHANGELOG.md
[license]: LICENSE.md
