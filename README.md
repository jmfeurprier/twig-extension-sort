Twig extension : sort
=====================

## Installation & Requirements

Install with [Composer](https://getcomposer.org):

```shell script
composer require jmf/twig-sort
```

## Usage in Twig templates

### sort() filter

Sorts provided array by value, losing key-value association.

```html
{% set sorted = values|sort %}
```

### rsort() filter

Reverse-sorts provided array by value, losing key-value association.

```html
{% set sorted = values|rsort %}
```

### asort() filter

Sorts provided array by value, preserving key-value association.

```html
{% set sorted = values|asort %}
```

### arsort() filter

Reverse-sorts provided array by value, preserving key-value association.

```html
{% set sorted = values|arsort %}
```

### ksort() filter

Sorts provided array by key.

```html
{% set sorted = values|ksort %}
```

### krsort() filter

Reverse-sorts provided array by key.

```html
{% set sorted = values|krsort %}
```

### psort() filter

Sorts provided array of arrays or array of objects by properties.

```html
{% set sorted = articles|psort('title') %}
{% set sorted = articles|psort(['title', 'author.name']) %}
{% set sorted = articles|psort({'publication_date': 'desc', 'author': 'asc'}) %}
