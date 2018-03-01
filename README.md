# Python Equation Calculation Research

# Packages

## Sympy

http://docs.sympy.org/

- More suited for equation solving, not string based

## Equation

https://github.com/alphaomega-technology/Equation
https://pypi.python.org/pypi/Equation/1.0

Exceptions are pretty unhelpful.

Requires pre-parsing of parameter tokens into simple variables (chokes on `<Production capacity>`, needs `x` instead).

Has some latex output support, would still need to figure out how to interpolate meaningful variables names.

Operators & functions

- +
- -
- *
- /
- %
- ^
- **
- &&
- ||
- &
- |
- </>
- &|
- |&
- ==
- =
- ~
- !~
- !=
- <>
- ><
- <
- >
- <=
- >=
- =<
- =>
- <~
- >~
- ~<
- ~>
- !
- -
- abs
- sum
- prod
- floor
- ceil
- round
- sin
- cos
- tan
- re
- im
- sqrt
- pi
- NaN

```
In [22]: Expression("x + sum(3,4,y)", ["x", "y"])(1, 5)
Out[22]: 13
```


## py-expression-eval

https://github.com/AxiaCore/py-expression-eval

Light-weight. And the logical operators are a bit confusing.

Requires pre-parsing of parameter tokens into simple variables (chokes on `<Production capacity>`, needs `x` instead).

Exceptions for:

- invalid expression
- unexpected operator
- unexpected number
- unexpected string
- unexpected constant
- unexpected function
- unexpected operator
- unexpected variable
- unexpected parenthesis
- unmatched parenthesis

Operations & functions

- +: add
- -: sub
- -: neg
- \*: mul
- /: div
- %: mod
- ^: pow
- ,: append
- ||: concat
- ==: equal
- !=: notEqual
- \>: greaterThan
- <: lessThan
- \>=: greaterThanEqual
- <=: lessThanEqual
- sin: sin
- cos: cos
- tan: tan
- asin: asin
- acos: acos
- atan: atan
- sqrt: sqrt
- log: log
- abs: abs
- ceil: ceil
- floor: floor
- round: round
- exp: exp
- and: and
- or: or
- random: random
- fac: fac
- min: min
- max: max
- pyt: pyt
- pow: pow
- atan2: atan2
- concat: concat
- if (possible?)
- E: e
- PI: pi

```
In [9]: parser.parse('if(a >= 5, b*2, b-1)').evaluate({'a': 2, 'b': 10})
Out[9]: 9.0

In [10]: parser.parse('if(a >= 5, b*2, b-1)').evaluate({'a': 6, 'b': 10})
Out[10]: 20.0
```


## pytexit

https://github.com/erwanp/pytexit

Converts python expressions to LaTeX formula.

But we're not supporting _python_ expressions. :-(


Automatic LaTeX conversion might be really hard unless we can tack it onto the
parse/evaluate library.

An alternative would be to have a live-updating field for the LaTeX version of the formula.
