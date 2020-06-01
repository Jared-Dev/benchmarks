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
* __Machine:__ Linux fv-az148 5.3.0-1020-azure #21~18.04.1-Ubuntu SMP Wed Apr 15 09:35:56 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux | 2 vCPUs | 7GB.
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure).
* __Node:__ `v12.16.3`
* __Run:__ Mon Jun  1 01:08:34 UTC 2020

|                          | Router | Requests/s | Latency | Throughput/Mb |
| :--                      | --:    | :-:        | --:     | --:           |
| polkadot                 | ✗      | 66116.4    | 1.40    | 10.34         |
| fastify                  | ✓      | 64090.8    | 1.47    | 10.02         |
| bare                     | ✗      | 60239.2    | 1.57    | 9.42          |
| polka                    | ✓      | 60044.8    | 1.58    | 9.39          |
| rayo                     | ✓      | 59296.8    | 1.60    | 9.27          |
| foxify                   | ✓      | 57652.0    | 1.65    | 8.19          |
| connect                  | ✗      | 57578.4    | 1.65    | 9.01          |
| micro                    | ✗      | 56877.6    | 1.67    | 8.90          |
| yeps                     | ✗      | 54829.6    | 1.74    | 8.58          |
| server-base-router       | ✓      | 54134.4    | 1.76    | 8.47          |
| server-base              | ✗      | 53243.2    | 1.79    | 8.33          |
| micro-route              | ✓      | 51640.8    | 1.85    | 8.08          |
| connect-router           | ✓      | 51484.0    | 1.85    | 8.05          |
| trek-engine              | ✗      | 49141.6    | 1.95    | 6.98          |
| trek-router              | ✓      | 48105.6    | 1.99    | 6.84          |
| yeps-router              | ✓      | 45437.6    | 2.11    | 7.11          |
| vapr                     | ✓      | 45302.4    | 2.12    | 6.44          |
| koa                      | ✗      | 43342.4    | 2.22    | 6.78          |
| spirit                   | ✗      | 40904.0    | 1.94    | 6.40          |
| total.js                 | ✓      | 39976.0    | 2.41    | 11.36         |
| spirit-router            | ✓      | 39879.2    | 1.99    | 6.24          |
| koa-router               | ✓      | 38689.4    | 2.50    | 6.05          |
| restify                  | ✓      | 38598.6    | 2.51    | 6.11          |
| express-route-prefix     | ✓      | 31645.0    | 3.04    | 11.02         |
| microrouter              | ✓      | 29844.8    | 3.25    | 4.67          |
| express                  | ✓      | 29376.8    | 3.31    | 4.59          |
| hapi                     | ✓      | 23543.2    | 4.16    | 3.68          |
| express-with-middlewares | ✓      | 22530.8    | 4.33    | 8.14          |
| egg.js                   | ✓      | 19075.1    | 5.16    | 6.29          |
| fastify-big-json         | ✓      | 10684.0    | 9.24    | 122.68        |
| take-five                | ✓      | N/A        | N/A     | N/A           |
