# angular-swagger-ui-material

![work: in progress](https://img.shields.io/badge/work-in%20progress-orange.svg?style=flat)

Material Design template for [angular-swagger-ui](https://github.com/Orange-OpenSource/angular-swagger-ui).

## Demo

### Main demos

| Demo  | Server | Notes |
| --- | --- | --- |
| [Pet Store](http://darosh.github.io/angular-swagger-ui-material) | [petstore.swagger.io](http://petstore.swagger.io) | Markdown in API info |
| [Hub](http://darosh.github.io/angular-swagger-ui-material/hub.html) | | powered by [APIs.guru](http://APIs.guru) |
| [Theming Demo](http://darosh.github.io/angular-swagger-ui-material/?primary=blue-grey&accent=grey&warn=pink) | [petstore.swagger.io](http://petstore.swagger.io) | *primary:* blue-grey, *accent:* grey, *warn:* pink |

### Development demos

| Demo  | Server | Notes |
| --- | --- | --- |
| [Uber](http://darosh.github.io/angular-swagger-ui-material/#?url=https://cdn.rawgit.com/OAI/OpenAPI-Specification/master/examples/v2.0/json/uber.json) | no | Markdown in operation info |
| [LoopBack Drupal](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-drupal.json) | no | [Drupal](https://www.drupal.org/) database discovered + [LoopBack](http://loopback.io/) default models, <br> large: 900+ operations |
| [Minimal Swagger 2.0](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-minimal.json) | no | |
| [GiHub Flavored Markdown](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-gfm.json) | no | generated from [github-flavored-markdown-test](https://github.com/suan/github-flavored-markdown-test) |
| [Swashbuckle](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-swashbuckle.json) | no | generated by [Swashbuckle](https://github.com/domaindrivendev/Swashbuckle) |
| [Swashbuckle.OData](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-swashbuckle-odata.json) | no | example from [Swashbuckle.OData](https://github.com/rbeauchamp/Swashbuckle.OData) |
| [YAML](http://darosh.github.io/angular-swagger-ui-material/#?url=https://cdn.rawgit.com/APIs-guru/api-models/master/APIs/bbc.com/1.0.0/swagger.yaml) | no | example for [swagger-yaml.js](./src/modules/swagger-yaml.js) module |

## Features

* [x] Compatible with [angular-swagger-ui](https://github.com/Orange-OpenSource/angular-swagger-ui) 0.3.0 (2016-02-22)
* [x] [Material Design](https://www.google.com/design/spec/material-design/introduction.html)
* [x] Responsible layout
* [x] Configurable [angular-material](https://material.angularjs.org) theme colors
* [x] Highlight deprecated methods
* [x] Search
* [x] YAML Swagger format support
* [x] Standard HTTP methods, status codes and headers reference thanks to [know-your-http-well](https://github.com/for-GET/know-your-http-well)
* [*] Grouped/Un-grouped view


## Search

| Filter | Matches | Notes |
| --- | --- | --- |
| log | POST /user/login <br> POST /user/login| path |
| get | GET /user <br> GET /pet | method |
| ge | N/A | single word, not full method |
| get pet | GET /pet | method + path |
| ge pet | GET /pet | method + path |

## Additional modules

### [sort](./src/modules/swagger-sort.js)

Standalone angular-swagger-ui plugin module for human readable sorting.

### [markdown](./src/modules/swagger-markdown.js)

Angular-swagger-ui plugin module for markdown.

**Dependencies**

```html
<script src="../bower_components/showdown/dist/showdown.js"></script>
<script src="../bower_components/angular-markdown-filter/markdown.js"></script>
```

### [split](./src/modules/swagger-split.js)

Angular-swagger-ui plugin module splitting creating and adding missing tags to operations based on path URL.

### [yaml](./src/modules/swagger-yaml.js)

Angular-swagger-ui plugin module for YAML.

**Dependencies**

```html
<script src="../bower_components/js-yaml/dist/js-yaml.js"></script>
```

## Reference

* [angular-swagger-ui](https://github.com/Orange-OpenSource/angular-swagger-ui)
* [Swagger RESTful API documentation specification](http://swagger.io/specification/)
* [OpenAPI specification](https://github.com/OAI/OpenAPI-Specification)

## Development

**Install**

```shell
npm install -g bower gulp
bower install
npm install
```

**Build dist**

```shell
gulp
```

**Build demo**

```shell
gulp demo
```

**Deploy demo**

```shell
gulp deploy
```

## TODOs

* [angular-swagger-ui-material](https://github.com/darosh/angular-swagger-ui-material/search?q=TODO&type=Code&utf8=%E2%9C%93)
* [angular-swagger-ui](https://github.com/Orange-OpenSource/angular-swagger-ui/search?q=TODO&type=Code&utf8=%E2%9C%93)
* [ ] Alternative layout in "documentation" style
* [ ] Operation permalinks
* [ ] Hot keys (search, submit)
* [ ] E2E tests
* [ ] Cross-browser compatibility (unknown, Chrome should be fine)
* [ ] Optimization (one-time binding, &hellip;)
