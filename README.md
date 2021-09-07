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

# chdir

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Change the current working directory.

<section class="installation">

## Installation

```bash
npm install @stdlib/process-chdir
```

</section>

<section class="usage">

## Usage

```javascript
var chdir = require( '@stdlib/process-chdir' );
```

#### chdir( path )

Changes the current working directory to the specified `path`.

<!-- run-disable -->

```javascript
var err = chdir( '/foo/bar' );
```

If the function encounters an error when attempting to change the working directory, the function returns an `error`; otherwise, the function returns `null`.

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   See [chdir(2)][chdir].

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var cwd = require( '@stdlib/process-cwd' );
var chdir = require( '@stdlib/process-chdir' );

// Print the current working directory:
var dir = cwd();
console.log( dir );

// Change the current working directory to the directory of this file:
var err = chdir( __dirname );
if ( err ) {
    console.error( err.message );
}

// Print the current working directory:
console.log( cwd() );

// Change the current working directory back to the original directory:
err = chdir( dir );
if ( err ) {
    console.error( err.message );
}

// Print the current working directory:
console.log( cwd() );
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   [`@stdlib/process/cwd`][@stdlib/process/cwd]: return the current working directory.

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/process-chdir.svg
[npm-url]: https://npmjs.org/package/@stdlib/process-chdir

[test-image]: https://github.com/stdlib-js/process-chdir/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/process-chdir/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/process-chdir/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/process-chdir?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/process-chdir.svg
[dependencies-url]: https://david-dm.org/stdlib-js/process-chdir/main

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/process-chdir/main/LICENSE

[chdir]: http://man7.org/linux/man-pages/man2/chdir.2.html

<!-- <related-links> -->

[@stdlib/process/cwd]: https://github.com/stdlib-js/process-cwd

<!-- </related-links> -->

</section>

<!-- /.links -->
