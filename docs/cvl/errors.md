% NOTE: This list autogenerated by `ErrorList`;
% DO NOT EDIT

List of CVL errors
==================

```{contents}
```


## Basic syntax errors


### `ArraySizeMustBeLiteral`

>
> Array sizes must be constant
>
> *No example provided*


### `LhsIsDynamicArray`

>
> Error message indicating an assignment to a dynamic array access
>
> Example:
> ```{code-block} cvl
> :emphasize-lines: 2-2
> 
> rule example {
>     x[] = 2;
> }
> ```
> ```
> Example:3:17: Assigning to an array element requires an index
> ```


### `LhsIsMapping`

>
> Error message indicating an assignment to a mapping type
>
> *No example provided*


### `SyntaxError`

>
> Syntax error (from the parser)
>
> Example:
> ```{code-block} cvl
> :emphasize-lines: 1-1
> 
> rule example oopsie { }
> ```
> ```
> Example:2:22: Syntax error: unexpected token near `oopsie`
> ```


### `TwoStateOnNonGhostFunction`

>
> You can only use `f@old` or `f@new` in the context of a `havoc...assuming` statement, and it can only be applied to a ghost.  See {ref}`havoc-stmt` for more information.
>
> Example:
> ```{code-block} cvl
> :emphasize-lines: 5-5
> 
> function f(uint x) returns uint {
>     return x;
> }
> rule example {
>     uint y = f@old(0);
> }
> ```
> ```
> Example:6:22: Cannot use `@old` with non-ghost function `f`
> ```



## Type checking errors



## Methods block errors



## CVL 2 errors


### `CVL2MissingFunctionKW`

>
> Since CVL 2, methods block entries must begin with `function`.  See {ref}`cvl2-function-keyword`.
>
> Example:
> ```{code-block} cvl
> :emphasize-lines: 2-2
> 
> methods {
>     balanceOf(address);
> }
> ```
> ```
> Example:3:17: Since CVL 2, methods block entries must begin with `function`
> ```


### `CVL2MissingSemicolon`

>
> Indicates one of the places that CVL became more strict about semicolons.  See {ref}`cvl2-semicolons`.
>
> Example:
> ```{code-block} cvl
> :emphasize-lines: 2-2
> 
> methods {
>     function balanceOf(address)
> }
> ```
> ```
> Example:3:40: Since CVL 2, methods block entries must end with `;`
> ```



## Unsupported feature errors


