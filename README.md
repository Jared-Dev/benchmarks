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
* __Machine:__ Linux fv-az54 5.3.0-1028-azure #29~18.04.1-Ubuntu SMP Fri Jun 5 14:32:34 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux | 2 vCPUs | 7GB.
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure).
* __Node:__ `v12.18.1`
* __Run:__ Wed Jul  1 01:17:27 UTC 2020

|                          | Router | Requests/s | Latency | Throughput/Mb |
| :--                      | --:    | :-:        | --:     | --:           |
| polkadot                 | ✗      | 36505.2    | 2.63    | 5.71          |
| fastify                  | ✓      | 33607.0    | 2.88    | 5.26          |
| polka                    | ✓      | 33133.8    | 2.92    | 5.18          |
| micro                    | ✗      | 32477.2    | 2.98    | 5.08          |
| foxify                   | ✓      | 32429.4    | 2.99    | 4.61          |
| connect                  | ✗      | 31554.4    | 3.07    | 4.94          |
| bare                     | ✗      | 31020.0    | 3.13    | 4.85          |
| rayo                     | ✓      | 30237.0    | 3.21    | 4.73          |
| yeps                     | ✗      | 27482.0    | 3.54    | 4.30          |
| spirit-router            | ✓      | 27236.0    | 3.29    | 4.26          |
| server-base              | ✗      | 26898.8    | 3.62    | 4.21          |
| spirit                   | ✗      | 26183.6    | 3.43    | 4.09          |
| connect-router           | ✓      | 26182.0    | 3.72    | 4.09          |
| server-base-router       | ✓      | 26157.2    | 3.72    | 4.09          |
| micro-route              | ✓      | 25980.8    | 3.75    | 4.06          |
| trek-router              | ✓      | 25758.4    | 3.79    | 3.66          |
| trek-engine              | ✗      | 25605.6    | 3.82    | 3.64          |
| yeps-router              | ✓      | 23756.0    | 4.11    | 3.72          |
| koa                      | ✗      | 23510.8    | 4.16    | 3.68          |
| vapr                     | ✓      | 21925.6    | 4.45    | 3.12          |
| restify                  | ✓      | 21370.0    | 4.59    | 3.38          |
| total.js                 | ✓      | 21231.2    | 4.60    | 6.03          |
| koa-router               | ✓      | 20557.2    | 4.77    | 3.22          |
| microrouter              | ✓      | 18734.0    | 5.24    | 2.93          |
| hapi                     | ✓      | 16723.2    | 5.91    | 2.62          |
| egg.js                   | ✓      | 12272.6    | 8.07    | 4.05          |
| fastify-big-json         | ✓      | 7660.4     | 12.90   | 87.96         |
| express                  | ✓      | 7081.3     | 13.96   | 1.11          |
| express-route-prefix     | ✓      | 6903.9     | 14.37   | 2.40          |
| express-with-middlewares | ✓      | 6093.7     | 16.28   | 2.20          |
| take-five                | ✓      | N/A        | N/A     | N/A           |
