<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# isSameKindCast

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Determine whether an ndarray [data type][@stdlib/ndarray/dtypes] can be safely cast to, or is of the same "kind" as, another ndarray [data type][@stdlib/ndarray/dtypes].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import isSameKindCast from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast@esm/index.mjs';
```

#### isSameKindCast( from, to )

Returns a `boolean` indicating whether an ndarray [data type][@stdlib/ndarray/dtypes] can be safely cast to, or is of the same "kind" as, another ndarray [data type][@stdlib/ndarray/dtypes] (e.g., casting between signed integers or between floats).

```javascript
var bool = isSameKindCast( 'float32', 'float64' );
// returns true

bool = isSameKindCast( 'uint16', 'int16' );
// returns false
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import dtypes from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-dtypes@esm/index.mjs';
import isSameKindCast from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast@esm/index.mjs';

var DTYPES;
var bool;
var dt;
var i;
var j;

// Get a list of supported ndarray data types:
DTYPES = dtypes();

// For each data type, determine whether one can cast to another data type...
for ( i = 0; i < DTYPES.length; i++ ) {
    dt = DTYPES[ i ];
    for ( j = 0; j < DTYPES.length; j++ ) {
        bool = isSameKindCast( dt, DTYPES[ j ] );
        console.log( '%s => %s. Allowed cast? %s.', dt, DTYPES[ j ], bool );
    }
}

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/ndarray-base-assert-is-same-kind-data-type-cast.svg
[npm-url]: https://npmjs.org/package/@stdlib/ndarray-base-assert-is-same-kind-data-type-cast

[test-image]: https://github.com/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast.svg
[dependencies-url]: https://david-dm.org/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/tree/deno
[umd-url]: https://github.com/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/tree/umd
[esm-url]: https://github.com/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/tree/esm
[branches-url]: https://github.com/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/ndarray-base-assert-is-same-kind-data-type-cast/main/LICENSE

[@stdlib/ndarray/dtypes]: https://github.com/stdlib-js/ndarray-dtypes/tree/esm

</section>

<!-- /.links -->
