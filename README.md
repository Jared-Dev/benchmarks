<div align="center">
<img src="https://github.com/fastify/graphics/raw/master/full-logo.png" width="650" height="auto"/>
</div>

<div align="center">

[![Build Status](https://travis-ci.org/fastify/fastify.svg?branch=master)](https://travis-ci.org/fastify/fastify)
[![Coverage Status](https://coveralls.io/repos/github/fastify/fastify/badge.svg?branch=master)](https://coveralls.io/github/fastify/fastify?branch=master)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](http://standardjs.com/)
[![NPM version](https://img.shields.io/npm/v/fastify.svg?style=flat)](https://www.npmjs.com/package/fastify)
[![NPM downloads](https://img.shields.io/npm/dm/fastify.svg?style=flat)](https://www.npmjs.com/package/fastify) [![Gitter](https://badges.gitter.im/gitterHQ/gitter.svg)](https://gitter.im/fastify)
</div>
<br />

# TL;DR

* [Fastify](https://github.com/fastify/fastify) is, fast and low overhead web framework for Node.js
* This package shows how fast it is comparatively.

# Installing

```
npm i -g fastify-benchmarks
```

# Usage

```
benchmark [arguments (optional)]
```

#### Arguments

* `-h`: Help on how to use the tool.
* `compare`: Get comparative data for your benchmarks.

> You may also compare all test results, at once, in a single table; `benchmark compare -t`

> You can also extend the comparison table with percentage values based on fastest result; `benchmark compare -p`
# Benchmarks
* __Machine:__ Linux fv-az86 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux | 2 vCPUs | 7GB.
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure).
* __Node:__ `v12.18.3`
* __Run:__ Sat Aug  1 01:23:35 UTC 2020

|                          | Router | Requests/s | Latency | Throughput/Mb |
| :--                      | --:    | :-:        | --:     | --:           |
| polkadot                 | ✗      | 57688.0    | 1.59    | 9.02          |
| fastify                  | ✓      | 53945.6    | 1.76    | 8.44          |
| bare                     | ✗      | 51928.8    | 1.83    | 8.12          |
| foxify                   | ✓      | 51147.2    | 1.86    | 7.27          |
| polka                    | ✓      | 51145.6    | 1.86    | 8.00          |
| connect                  | ✗      | 49164.8    | 1.94    | 7.69          |
| micro                    | ✗      | 48262.4    | 1.98    | 7.55          |
| rayo                     | ✓      | 48256.8    | 1.98    | 7.55          |
| connect-router           | ✓      | 45750.4    | 2.10    | 7.16          |
| yeps                     | ✗      | 44851.2    | 2.14    | 7.01          |
| server-base-router       | ✓      | 44226.4    | 2.17    | 6.92          |
| server-base              | ✗      | 44092.0    | 2.18    | 6.90          |
| trek-engine              | ✗      | 44053.6    | 2.18    | 6.26          |
| micro-route              | ✓      | 43556.8    | 2.20    | 6.81          |
| trek-router              | ✓      | 42480.0    | 2.27    | 6.04          |
| koa                      | ✗      | 38510.2    | 2.51    | 6.02          |
| yeps-router              | ✓      | 38113.6    | 2.53    | 5.96          |
| vapr                     | ✓      | 37264.0    | 2.59    | 5.30          |
| spirit                   | ✗      | 36136.6    | 2.19    | 5.65          |
| spirit-router            | ✓      | 35743.8    | 2.24    | 5.59          |
| total.js                 | ✓      | 34446.4    | 2.81    | 9.79          |
| koa-router               | ✓      | 33245.6    | 2.92    | 5.20          |
| restify                  | ✓      | 32102.6    | 3.03    | 5.08          |
| microrouter              | ✓      | 25596.4    | 3.80    | 4.00          |
| hapi                     | ✓      | 22076.4    | 4.44    | 3.45          |
| egg.js                   | ✓      | 18862.7    | 5.23    | 6.22          |
| express                  | ✓      | 10669.0    | 9.24    | 1.67          |
| express-route-prefix     | ✓      | 9634.5     | 10.29   | 3.35          |
| express-with-middlewares | ✓      | 9235.8     | 10.68   | 3.34          |
| fastify-big-json         | ✓      | 9018.6     | 10.95   | 103.56        |
| take-five                | ✓      | N/A        | N/A     | N/A           |
