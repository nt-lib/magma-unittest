# magma-unittest

A minimal unit testing framework for [Magma](http://magma.maths.usyd.edu.au/magma/).

## Usage

Add this repository as a git submodule, then load `tst.m` from your test entry point:

    load "path/to/magma-unittest/tst.m";

## API

- `TSTAssertEQ(computed, expected)` -- asserts `computed eq expected`, aborts on failure
- `TSTAssertNE(computed, expected)` -- asserts `computed ne expected`, aborts on failure
- `TSTAssertRaises(f, message, args)` -- asserts that calling `f(args...)` raises an error whose message contains `message`

## Example

    load "magma-unittest/tst.m";

    procedure test_addition()
        TSTAssertEQ(1 + 1, 2);
    end procedure;

    test_addition();
    print "All tests passed!";

## Adding as a submodule

    git submodule add git@github.com:nt-lib/magma-unittest.git tests/magma-unittest

Then in your test entry point:

    load "magma-unittest/tst.m";

## Licence

Copyright (C) 2025 Maarten Derickx.
Licensed under the GNU General Public Licence v3. See LICENSE.
