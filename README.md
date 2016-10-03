# Visual Basic 6.0 Grammar for ANTLR4 JavaScript

prebuilt for ANTLR4 JavaScript target.  
grammar is originally cloned from [uwol/vb6grammar](https://github.com/uwol/vb6grammar).  

## How to use

```sh
npm install antlr4-vb6 antlr4
```

```js
import antlr4 from 'antlr4';
import {VisualBasic6Lexer, VisualBasic6Parser} from 'antlr4-vb6';

let stream = new antlr4.InputStream('Dim i As Integer\n');
let lexer = new VisualBasic6Lexer(stream);
let tokens = new antlr4.CommonTokenStream(lexer);
let parser = new VisualBasic6Parser(tokens);
parser.buildParseTrees = true;
let tree = parser.startRule();

console.log(tree);
```

## How to build from source

install ANTLR4  
[Getting Started with ANTLR v4](https://github.com/antlr/antlr4/blob/master/doc/getting-started.md)

then, `npm run build`
