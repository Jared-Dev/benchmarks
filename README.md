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
* __Machine:__ Linux fv-az50 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux | 2 vCPUs | 7GB.
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure).
* __Node:__ `v12.18.4`
* __Run:__ Thu Oct  1 01:40:05 UTC 2020

|                          | Router | Requests/s | Latency | Throughput/Mb |
| :--                      | --:    | :-:        | --:     | --:           |
| polkadot                 | ✗      | 73970.8    | 1.23    | 11.57         |
| fastify                  | ✓      | 70193.6    | 1.34    | 10.98         |
| bare                     | ✗      | 67514.8    | 1.40    | 10.56         |
| foxify                   | ✓      | 66092.8    | 1.43    | 9.39          |
| polka                    | ✓      | 65578.8    | 1.44    | 10.26         |
| rayo                     | ✓      | 64842.0    | 1.46    | 10.14         |
| connect                  | ✗      | 64708.4    | 1.46    | 10.12         |
| micro                    | ✗      | 63415.2    | 1.49    | 9.92          |
| yeps                     | ✗      | 60244.8    | 1.57    | 9.42          |
| server-base-router       | ✓      | 58641.6    | 1.62    | 9.17          |
| connect-router           | ✓      | 58195.2    | 1.63    | 9.10          |
| server-base              | ✗      | 57845.6    | 1.65    | 9.05          |
| micro-route              | ✓      | 57290.4    | 1.66    | 8.96          |
| trek-engine              | ✗      | 55827.2    | 1.71    | 7.93          |
| trek-router              | ✓      | 54047.2    | 1.77    | 7.68          |
| yeps-router              | ✓      | 51400.8    | 1.86    | 8.04          |
| vapr                     | ✓      | 48771.2    | 1.96    | 6.93          |
| koa                      | ✗      | 47912.8    | 2.01    | 7.49          |
| spirit                   | ✗      | 47200.0    | 1.66    | 7.38          |
| total.js                 | ✓      | 46450.4    | 2.06    | 13.20         |
| spirit-router            | ✓      | 46061.6    | 1.72    | 7.20          |
| koa-router               | ✓      | 43699.2    | 2.21    | 6.83          |
| restify                  | ✓      | 43314.4    | 2.23    | 6.86          |
| microrouter              | ✓      | 33956.4    | 2.85    | 5.31          |
| hapi                     | ✓      | 28715.2    | 3.40    | 4.49          |
| egg.js                   | ✓      | 21538.8    | 4.56    | 7.11          |
| express                  | ✓      | 13855.4    | 7.11    | 2.17          |
| express-with-middlewares | ✓      | 11862.6    | 8.31    | 4.29          |
| fastify-big-json         | ✓      | 11749.4    | 8.39    | 134.91        |
| express-route-prefix     | ✓      | 11704.2    | 8.46    | 4.07          |
| take-five                | ✓      | N/A        | N/A     | N/A           |
