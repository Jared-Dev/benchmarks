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
* __Machine:__ Linux fv-az115 5.0.0-1035-azure #37-Ubuntu SMP Wed Mar 18 11:21:35 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux | 2 vCPUs | 7GB.
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure).
* __Node:__ `v12.16.3`
* __Run:__ Fri May  1 00:55:04 UTC 2020

|                          | Router | Requests/s | Latency | Throughput/Mb |
| :--                      | --:    | :-:        | --:     | --:           |
| polkadot                 | ✗      | 66896.4    | 1.37    | 10.46         |
| fastify                  | ✓      | 65945.2    | 1.43    | 10.31         |
| foxify                   | ✓      | 61472.0    | 1.54    | 8.73          |
| bare                     | ✗      | 61244.0    | 1.54    | 9.58          |
| polka                    | ✓      | 59944.8    | 1.58    | 9.38          |
| connect                  | ✗      | 57870.4    | 1.64    | 9.05          |
| rayo                     | ✓      | 56700.8    | 1.68    | 8.87          |
| micro                    | ✗      | 54179.2    | 1.76    | 8.47          |
| yeps                     | ✗      | 54019.2    | 1.76    | 8.45          |
| server-base-router       | ✓      | 52872.8    | 1.80    | 8.27          |
| server-base              | ✗      | 52220.8    | 1.83    | 8.17          |
| micro-route              | ✓      | 50484.0    | 1.89    | 7.90          |
| connect-router           | ✓      | 50108.8    | 1.91    | 7.84          |
| trek-engine              | ✗      | 49357.6    | 1.94    | 7.01          |
| trek-router              | ✓      | 49293.6    | 1.95    | 7.00          |
| yeps-router              | ✓      | 45120.0    | 2.13    | 7.06          |
| vapr                     | ✓      | 44596.8    | 2.15    | 6.34          |
| koa                      | ✗      | 43778.4    | 2.20    | 6.85          |
| total.js                 | ✓      | 40713.6    | 2.36    | 11.57         |
| spirit                   | ✗      | 40428.8    | 1.94    | 6.32          |
| spirit-router            | ✓      | 40110.4    | 1.96    | 6.27          |
| koa-router               | ✓      | 37142.6    | 2.61    | 5.81          |
| restify                  | ✓      | 36437.0    | 2.66    | 5.77          |
| express-route-prefix     | ✓      | 32489.2    | 2.97    | 11.31         |
| express                  | ✓      | 30408.0    | 3.19    | 4.76          |
| microrouter              | ✓      | 29477.2    | 3.29    | 4.61          |
| hapi                     | ✓      | 24171.2    | 4.05    | 3.78          |
| express-with-middlewares | ✓      | 23633.2    | 4.12    | 8.54          |
| egg.js                   | ✓      | 19146.0    | 5.14    | 6.32          |
| fastify-big-json         | ✓      | 11197.6    | 8.81    | 128.57        |
| take-five                | ✓      | N/A        | N/A     | N/A           |
