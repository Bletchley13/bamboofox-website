title: '[CSAW CTF 2016] warmup 50'
author: nae
tags:
  - CSAW CTF 2016
  - pwn
  - overflow
categories:
  - write-ups
date: 2016-09-19 23:31:00
---

> Category: pwn		
> Point: 50		
> Solver: nae @ BambooFox	

和藹可親的 warmup

64 bit ELF NX, Partial RELRO, no canary, no PIE

這題就簡單的 `stack overflow` 量一下 offset，他有一個 function 會直接 `system('cat flag.txt')`，在 ret address 的地方蓋成那個 function 就可以拿 flag。
