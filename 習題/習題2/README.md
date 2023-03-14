## 測試程式

```
int a=0;
do {
      a += 1;
}while( a < 10);
```

## 執行結果

```
jung@JUNGLAPTOP:/mnt/c/Users/alex2/NQU/sp111b/習題/習題2$ make
gcc -std=c99 -O0 lexer.c compiler.c main.c -o compiler
jung@JUNGLAPTOP:/mnt/c/Users/alex2/NQU/sp111b/習題/習題2$ ./compiler test.c
int a=0;
do {
      a += 1;
}while( a < 10);
========== lex ==============
token=int
token=a
token==
token=0
token=;
token=do
token={
token=a
token=+
token==
token=1
token=;
token=}
token=while
token=(
token=a
token=<
token=10
token=)
token=;
========== dump ==============
0:int
1:a
2:=
3:0
4:;
5:do
6:{
7:a
8:+
9:=
10:1
11:;
12:}
13:while
14:(
15:a
16:<
17:10
18:)
19:;
============ parse =============
skip(=) got a fail!
compiler: compiler.c:36: skip: Assertion `0' failed.
Aborted
``` 