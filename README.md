# hubot-datadog-graph

A Hubot script to take graph snapshots using the [Datadog API](http://docs.datadoghq.com/api/).

## Installation

    $ npm install https://github.com/bouzuya/hubot-datadog-graph/archive/master.tar.gz

or

    $ npm install https://github.com/bouzuya/hubot-datadog-graph/archive/{VERSION}.tar.gz

## Example

    bouzuya> hubot help datadog-graph
      hubot> hubot datadog graph <graph>[ <range>] - take a graph snapshot using the Datadog API
             hubot datadog graph config - list datadog graphs (queries)
             hubot datadog graph config add <graph> <query> - add datadog graph (query)
             hubot datadog graph config remove <graph> - remove datadog graph (query)

    bouzuya> hubot datadog graph config add sushi system.load.1{*}
      hubot> OK
    bouzuya> hubot datadog graph config
      hubot> graph1
             graph2
             sushi

    bouzuya> hubot datadog graph config remove graph1
      hubot> OK
    bouzuya> hubot datadog graph config
      hubot> graph2
             sushi

    bouzuya> hubot datadog graph sushi
      hubot> take a graph snapshot (sushi) ...
      hubot> https://s3.amazonaws.com/dd-snapshots-prod/org_1499/2013-07-19/53fd79f024e7796f4ca399f1d90adf3cf95a9bb8.png

## Configuration

See [`src/scripts/datadog-graph.coffee`](src/scripts/datadog-graph.coffee).

## Development

See `npm run`

## License

[MIT](LICENSE)

## Author

[bouzuya][user] &lt;[m@bouzuya.net][mail]&gt; ([http://bouzuya.net][url])

## Badges

[![Build Status][travis-badge]][travis]
[![Dependencies status][david-dm-badge]][david-dm]
[![Coverage Status][coveralls-badge]][coveralls]

[travis]: https://travis-ci.org/bouzuya/hubot-datadog-graph
[travis-badge]: https://travis-ci.org/bouzuya/hubot-datadog-graph.svg?branch=master
[david-dm]: https://david-dm.org/bouzuya/hubot-datadog-graph
[david-dm-badge]: https://david-dm.org/bouzuya/hubot-datadog-graph.png
[coveralls]: https://coveralls.io/r/bouzuya/hubot-datadog-graph
[coveralls-badge]: https://img.shields.io/coveralls/bouzuya/hubot-datadog-graph.svg
[user]: https://github.com/bouzuya
[mail]: mailto:m@bouzuya.net
[url]: http://bouzuya.net

