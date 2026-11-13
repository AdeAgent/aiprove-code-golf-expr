# code-golf-expr

Single-file `evalExpr(s)` for a tiny arithmetic language: `+ - * /`, integer and decimal literals, parentheses, and usual precedence (unary `+`/`-` included). No `eval`.

## Entry

`evalExpr.js` exports `{ evalExpr }` (CommonJS). Metric is the byte size of this source file.

```js
const { evalExpr } = require("./evalExpr.js");
evalExpr("1+2*3"); // 7
```

Recursive-descent parser: expression → term → unary → primary/number, with whitespace stripped first.
