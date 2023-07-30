# calc_by_lex
## change1
- 입력 자료형을 float형으로 변환
```
[0-9]+(\.[0-9]+)? { yylval.floatval = atof(yytext); return NUMBER; }
```
https://github.com/M3NGo0/calc_by_lex/blob/f9856b3e396be0d07f6389313857e1e23007dee9/fb1-5.l#L11

## change2
- union을 이용해서 floatval 선언
```
%union{
float floatval;
}
```
https://github.com/M3NGo0/calc_by_lex/blob/f9856b3e396be0d07f6389313857e1e23007dee9/fb1-5.y#L6

## change 3
- 자료형이 floatval인 변수를 선언
```
%type <floatval> exp
%type <floatval> factor
%type <floatval> term
```
https://github.com/M3NGo0/calc_by_lex/blob/f9856b3e396be0d07f6389313857e1e23007dee9/fb1-5.y#L17C1-L19C22

