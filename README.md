# AstPrinter

A command line tool that prints the expanded AST (Abstract Syntax Tree) of a dart file.

![Output example](https://raw.githubusercontent.com/GeKorm/docimages/master/astprinter/AST.png)

The above image was created using ```ast <path> > output.txt```, then
opening output.txt in Sublime Text and adding Dart syntax highlighting.

## Usage

```
dart pub get
```
    
To print the AST in the console, run ```dart run bin/ast.dart <"absolutePathToDartFile"> <Type(OPTIONAL)> <-n(OPTIONAL)>```

    dart run bin/ast.dart "C:\Path\web\main.dart" Declaration
The optional argument ```Type``` will print all AST nodes that are subtypes of ```Type```.
Multiple types can be entered as arguments.
To print Types without their subtypes append -n. 

For example

     dart run bin/ast.dart "C:\Path\web\main.dart" Token
will print all tokens, including ```StringToken```, ```BeginToken```, ```KeywordToken```
and ```Token```. However,

     dart run bin/ast.dart "C:\Path\web\main.dart" Token -n
will only print ```Token ``` nodes, such as ```@```, ```=```, ```;``` etc.

