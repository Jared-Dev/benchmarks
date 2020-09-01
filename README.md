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
* __Machine:__ Linux fv-az60 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux | 2 vCPUs | 7GB.
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure).
* __Node:__ `v12.18.3`
* __Run:__ Tue Sep  1 01:33:38 UTC 2020

|                          | Router | Requests/s | Latency | Throughput/Mb |
| :--                      | --:    | :-:        | --:     | --:           |
| polkadot                 | ✗      | 57993.6    | 1.61    | 9.07          |
| fastify                  | ✓      | 54228.8    | 1.76    | 8.48          |
| bare                     | ✗      | 52162.4    | 1.83    | 8.16          |
| connect                  | ✗      | 50264.8    | 1.90    | 7.86          |
| foxify                   | ✓      | 50254.4    | 1.90    | 7.14          |
| polka                    | ✓      | 50079.2    | 1.91    | 7.83          |
| rayo                     | ✓      | 48841.6    | 1.96    | 7.64          |
| micro                    | ✗      | 47891.2    | 2.00    | 7.49          |
| connect-router           | ✓      | 45999.2    | 2.08    | 7.19          |
| server-base              | ✗      | 45260.8    | 2.12    | 7.08          |
| yeps                     | ✗      | 45165.6    | 2.12    | 7.06          |
| server-base-router       | ✓      | 44967.2    | 2.14    | 7.03          |
| micro-route              | ✓      | 44056.0    | 2.18    | 6.89          |
| trek-router              | ✓      | 42486.4    | 2.27    | 6.04          |
| trek-engine              | ✗      | 41444.0    | 2.33    | 5.89          |
| vapr                     | ✓      | 38411.2    | 2.51    | 5.46          |
| yeps-router              | ✓      | 38304.8    | 2.52    | 5.99          |
| koa                      | ✗      | 37592.6    | 2.58    | 5.88          |
| spirit                   | ✗      | 35927.0    | 2.17    | 5.62          |
| spirit-router            | ✓      | 35674.2    | 2.21    | 5.58          |
| total.js                 | ✓      | 34775.8    | 2.78    | 9.88          |
| koa-router               | ✓      | 33721.0    | 2.88    | 5.27          |
| restify                  | ✓      | 33357.6    | 2.91    | 5.28          |
| microrouter              | ✓      | 26451.2    | 3.68    | 4.14          |
| hapi                     | ✓      | 22140.0    | 4.43    | 3.46          |
| egg.js                   | ✓      | 18995.5    | 5.19    | 6.27          |
| express                  | ✓      | 10807.4    | 9.12    | 1.69          |
| express-route-prefix     | ✓      | 9657.4     | 10.27   | 3.36          |
| express-with-middlewares | ✓      | 9294.0     | 10.62   | 3.36          |
| fastify-big-json         | ✓      | 8999.3     | 10.97   | 103.33        |
| take-five                | ✓      | N/A        | N/A     | N/A           |
