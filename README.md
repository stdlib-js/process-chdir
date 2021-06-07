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

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/process-chdir/main/LICENSE

[chdir]: http://man7.org/linux/man-pages/man2/chdir.2.html

</section>

<!-- /.links -->
