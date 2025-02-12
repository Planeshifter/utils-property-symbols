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

# propertySymbols

> Return an array of an object's own symbol properties.

<section class="installation">

## Installation

```bash
npm install @stdlib/utils-property-symbols
```

</section>

<section class="usage">

## Usage

```javascript
var propertySymbols = require( '@stdlib/utils-property-symbols' );
```

#### propertySymbols( obj )

Returns an `array` of an object's own symbol.

```javascript
var symbols = propertySymbols( {} );
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   In contrast to the built-in `Object.getOwnPropertySymbols()`, if provided `null` or `undefined`, the function returns an empty `array`, rather than throwing an error.

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var hasSymbolSupport = require( '@stdlib/assert-has-symbol-support' );
var Symbol = require( '@stdlib/symbol-ctor' );
var propertySymbols = require( '@stdlib/utils-property-symbols' );

function Foo() {
    if ( hasSymbolSupport() ) {
        this[ Symbol( 'beep' ) ] = 'boop';
    }
    return this;
}

Foo.prototype.foo = 'bar';

var obj = new Foo();
var symbols = propertySymbols( obj );

console.log( symbols );
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-property-symbols/main/LICENSE

[@stdlib/symbol/ctor]: https://github.com/stdlib-js/symbol-ctor

</section>

<!-- /.links -->
