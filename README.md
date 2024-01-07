---assert.h---
範例一 : assert()
"用於驗證程式所做的假設，並在假設為假時輸出診斷訊息"
------
#include <assert.h>
#include <stdio.h>
 
int main()
{
   int a;
   char str[50];
     
   printf("請輸入一個整數值： ");
   scanf("%d", &a);
   assert(a >= 10);
   printf("輸入的整數是： %d\n", a);
    
   printf("請輸入字串： ");
   scanf("%s", str);
   assert(str != NULL);
   printf("輸入的字串是： %s\n", str);
    
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-macro-assert.html)



---ctype.h---
範例一 : isalnum()
"用於檢查所傳的字元是否為字母和數字"
------
#include <stdio.h>
#include <ctype.h> 
 
int main ()
{ 
int var1 = 'd' ;
int var2 = '2' ; 
int var3 = '\t'; 
int var4 = ' ' ;

   if ( isalnum ( var1 ) ) { 
      printf ( "var1 = |%c| 是字母數字\n" , var1 ); }
      else { 
      printf ( "var1 = |%c| 不是字母數字\n" , var1 ); } 
      if ( isalnum ( var2 ) ) { 
      printf ( "var2 = |%c| 是字母數字\n" , var2 ); } 
      else { 
      printf ( "var2 = |%c| 不是字母數字\n" , var2 ); }
      if ( isalnum ( var3 ) ) { 
      printf ( "var3 = |%c| 是字母數字\n" , var3 ); }
      else { 
      printf ( "var3 = |%c| 不是字母數字\n" , var3 ); }
      if ( isalnum ( var4 ) ) { 
      printf ( "var4 = |%c| 是字母數字\n" , var4 ); }
      else { 
      printf ( "var4 = |%c| 不是字母數字\n" , var4 ); } 
    
   return ( 0 ); 
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isalnum.html)


範例二 :  isalpha()
"用於檢查所傳的字元是否為字母"
------
#include <stdio.h> 
#include <ctype.h> 
  
int main () 
{ 
  int var1 = 'd' ; 
  int var2 = '2' ; 
  int var3 = '\t' ; 
  int var4 = ' ' ;

  if ( isalpha ( var1 ) ) { 
      printf ( "var1 = |%c| 是一個字母\n" , var1 ); }
  else { 
      printf ( "var1 = |%c| 不是一個字母\n" , var1 ); } 
  if ( isalpha ( var2 ) ) { 
      printf ( "var2 = |%c| 是一個字母\n" , var2 ); } 
  else { 
      printf ( "var2 = |%c| 不是一個字母\n" , var2 ); } 
  if ( isalpha ( var3 ) ) { 
      printf ( "var3 = |%c| 是一個字母\n" , var3 ); }
  else { 
      printf ( "var3 = |%c| 不是一個字母\n" , var3 ); } 
  if ( isalpha ( var4 ) ) { 
      printf ( "var4 = |%c| 是一個字母\n" , var4 ); } 
  else { 
      printf ( "var4 = |%c| 不是一個字母\n" , var4 ); } 
      
  return ( 0 ); 
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isalpha.html)


範例三 : iscntrl()
"用於檢查所傳的字符是否是控制字符"
------
#include <stdio.h>
#include <ctype.h>
   int main ()
   {
   int i = 0, j = 0;
   char str1[] = "all \a about \t programming";
   char str2[] = "Runoob \n tutorials";
  
   /* 輸出字串直到控制字符 \a */
   
   while( !iscntrl(str1[i]) ) 
   {
      putchar(str1[i]);
      i++;
   }
  
   /* 輸出字串直到控制字符 \n */
   while( !iscntrl(str2[j]) ) 
   {
      putchar(str2[j]);
      j++;
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-iscntrl.html)


範例四 : isdigit()
"用於檢查所傳的字元是否為十進位數字字元"
------
#include <stdio.h>
#include <ctype.h>

int main()
{
   int var1 = 'h';
   int var2 = '2';
    
   if( isdigit(var1) )
   {
      printf("var1 = |%c| 是一個數字\n", var1 );
   }
   else
   {
      printf("var1 = |%c| 不是一個數字\n", var1 );
   }
   if( isdigit(var2) )
   {
      printf("var2 = |%c| 是一個數字\n", var2 );
   }
   else
   {
      printf("var2 = |%c| 不是一個數字\n", var2 );
   }
  
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isdigit.html)


範例五 : islower()
"用於檢查所傳的字元是否為小寫字母"
------
#include <stdio.h>
#include <ctype.h>

int main()
{
   int var1 = 'Q';
   int var2 = 'q';
   int var3 = '3';
    
   if( islower(var1) )
   {
       printf("var1 = |%c| 是小寫字母\n", var1 );
   }
   else
   {
      printf("var1 = |%c| 不是小寫字母\n", var1 );
   }
   if( islower(var2) )
   {
       printf("var2 = |%c| 是小寫字母\n", var2 );
   }
   else
   {
      printf("var2 = |%c| 不是小寫字母\n", var2 );
   }
   if( islower(var3) )
   {
       printf("var3 = |%c| 是小寫字母\n", var3 );
   }
   else
   {
      printf("var3 = |%c| 不是小寫字母\n", var3 );
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-islower.html)


範例六 : isupper()
"用於檢查所傳的字元是否為大寫字母"
------
#include <stdio.h>
#include <ctype.h>

int main()
{
   int var1 = 'M';
   int var2 = 'm';
   int var3 = '3';
    
   if( isupper(var1) )
   {
      printf("var1 = |%c| 是大寫字母\n", var1 );
   }
   else
   {
      printf("var1 = |%c| 不是大寫字母\n", var1 );
   }
   if( isupper(var2) )
   {
      printf("var2 = |%c| 是大寫字母\n", var2 );
   }
   else
   {
      printf("var2 = |%c| 不是大寫字母\n", var2 );
   }   
   if( isupper(var3) )
   {
      printf("var3 = |%c| 是大寫字母\n", var3 );
   }
   else
   {
      printf("var3 = |%c| 不是大寫字母\n", var3 );
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isupper.html)


範例七 : ispunct()
"用於檢查所傳的字元是否為標點符號字元"
------
#include <stdio.h>
#include <ctype.h>

int main()
{
   int var1 = 't';
   int var2 = '1';
   int var3 = '/';

   if( ispunct(var1) )
   {
       printf("var1 = |%c| 是標點符號字元\n", var1 );
   }
   else
   {
       printf("var1 = |%c| 不是標點符號字元\n", var1 );
   }
   if( ispunct(var2) )
   {
       printf("var2 = |%c| 是標點符號字元\n", var2 );
   }
   else
   {
       printf("var2 = |%c| 不是標點符號字元\n", var2 );
   }
   if( ispunct(var3) )
   {
       printf("var3 = |%c| 是標點符號字元\n", var3 );
   }
   else
   {
       printf("var3 = |%c| 不是標點符號字元\n", var3 );
   }
   return(0);
}  
(資料來源:https://www.runoob.com/cprogramming/c-function-ispunct.html)


範例八 : isspace()
"用於檢查所傳的字符是否是空白字元"
------
#include <stdio.h>
#include <ctype.h>

int main()
{
   int var1 = 't';
   int var2 = '1';
   int var3 = ' ';

   if( isspace(var1) )
   {
       printf("var1 = |%c| 是空白字元\n", var1 );
   }
   else
   {
       printf("var1 = |%c| 不是空白字元\n", var1 );
   }
   if( isspace(var2) )
   {
       printf("var2 = |%c| 是空白字元\n", var2 );
   }
   else
   {
       printf("var2 = |%c| 不是空白字元\n", var2 );
   }
   if( isspace(var3) )
   {
       printf("var3 = |%c| 是空白字元\n", var3 );
   }
   else
   {
       printf("var3 = |%c| 不是空白字元\n", var3 );
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isspace.html)


範例九 : isxdigit()
"用於檢查所傳的字元是否為十六進位數字"
------
#include <ctype.h>
#include <stdio.h>
 
int main() {
   char c = '5';
   int result;
 
   // 傳入字符
   result = isxdigit(c); // result 傳回非 0
   printf("%c 傳入到 isxdigit() 函數结果為: %d", c, isxdigit(c));
   printf("\n");  // 換行
   c = 'M';
 
   // 非十六進制數作為参數
   result = isxdigit(c); // result 為 0
 
   printf("%c 傳入到 isxdigit() 函數结果為: %d", c, isxdigit(c));
 
   return 0;
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isxdigit.html)
 
 
 範例十 : isgraph()
 "用於檢查所傳的字元是否有圖形表示法"
 ------
 #include < stdio.h >
 #include < ctype.h > 
 
 int main ( ) 
 { 
    int var1 = ' 3 ';
    int var2 = ' m ';
    int var3 = ' ';
    
    if ( isgraph ( var1 ) ) { 
    printf ( " var1 = |%c| 是可列印的\ n " , var1 ) ;
    } 
    else { 
    printf ( " var1 = |%c| 是不可列印的\ n " , var1 ) ;
    } 
    if ( isgraph ( var2 ) ) { printf ( " var2 = |%c| 是可列印的\ n " , var2 ) ;
    } 
    else { 
    printf ( " var2 = |%c| 是不可列印的\ n " , var2 ) ;
    } 
    if ( isgraph ( var3 ) ) { printf ( " var3 = |%c| 是可列印的\ n " , var3 ) ;
    } 
    else { printf ( " var3 = |%c| 是不可列印的\ n " , var3 ) ;
    } 
    return ( 0 );
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isgraph.html)



---math.h---
範例一 : acos()
"double acos(double x)傳回以弧度表示的x的反餘弦"
------
#include <stdio.h> 
#include <math.h> 
 
#define PI 3.14159265

int main () 
{ 
   double x , ret , val ;
   
   x = 0.9 ; 
   val = 180.0 / PI ;   

   ret = acos ( x ) * val ; 
   printf ( "%lf 的反餘弦是%lf 度" , x , ret ); 
   
   return ( 0 );
}
(資料來源:https://www.runoob.com/cprogramming/c-function-acos.html)


範例二 : asin()
"double asin(double x)傳回以弧度表示的x的反正弦"
------
#include <stdio.h>
#include <math.h> 
 
#define PI 3.14159265

int main ()
{ 
double x , ret , val ; 
   x = 0.9 ; 
   val = 180.0 / PI ;

      

   ret = asin ( x ) * val ; 
   printf ( "%lf 的反正弦是%lf 度" , x , ret ); 
   
   return ( 0 ); 
}
(資料來源:https://www.runoob.com/cprogramming/c-function-asin.html)


範例三 : atan()
"double atan(double x)傳回以弧度表示的x的反正切"
------
#include <stdio.h> 
#include <math.h> 
 
#define PI 3.14159265

int main () 
{ 
double x , ret , val ; 
   x = 1.0 ; 
   val = 180.0 / PI ;

 
   ret = atan ( x ) * val ; 
   printf ( "%lf 的反正切是%lf 度" , x , ret ); 
   
   return ( 0 ); 
}
(資料來源:https://www.runoob.com/cprogramming/c-function-atan.html)


範例四 : cos()
"double cos(double x)傳回弧度角 x 的餘弦"
------
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main ()
{
   double x, ret, val;

   x = 60.0;
   val = PI / 180.0;
   ret = cos( x*val );
   printf("%lf 的餘弦是 %lf 度\n", x, ret);
   
   x = 90.0;
   val = PI / 180.0;
   ret = cos( x*val );
   printf("%lf 的餘弦是 %lf 度\n", x, ret);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-cos.html)


範例五 : sin()
"double sin(double x)傳回弧度角 x 的正弦"
------
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main ()
{
   double x, ret, val;

   x = 45.0;
   val = PI / 180;
   ret = sin(x*val);
   printf("%lf 的正弦是 %lf 度", x, ret);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-sin.html)


範例六 : cosh()
"double cosh(double x)傳回 x 的雙曲餘弦"
------
#include <stdio.h>
#include <math.h>

int main ()
{
   double x;

   x = 0.5;
   printf("%lf 的雙曲餘弦是 %lf\n", x, cosh(x));

   x = 1.0;
   printf("%lf 的雙曲餘弦是 %lf\n", x, cosh(x));

   x = 1.5;
   printf("%lf 的雙曲餘弦是 %lf\n", x, cosh(x));

   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-cosh.html)


範例七 : sinh()
"double sinh(double x)傳回x的雙曲正弦"
------
#include <stdio.h>
#include <math.h>

int main ()
{
   double x, ret;
   x = 0.5;

   ret = sinh(x);
   printf("%lf 的雙曲正弦是 %lf 度", x, ret);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-sinh.html)


範例八 : tanh()
"double tanh(double x)傳回 x 的雙曲正切"
------
#include <stdio.h>
#include <math.h>

int main ()
{
   double x, ret;
   x = 0.5;

   ret = tanh(x);
   printf("%lf 的雙曲正切是 %lf 度", x, ret);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-tanh.html)


範例九 : exp()
"double exp(double x)傳回e的x次方的值"
------
#include <stdio.h>
#include <math.h>

int main ()
{
   double x = 0;
  
   printf("e 的 %lf 次方是 %lf\n", x, exp(x));
   printf("e 的 %lf 次方是 %lf\n", x+1, exp(x+1));
   printf("e 的 %lf 次方是 %lf\n", x+2, exp(x+2));
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-exp.html)


範例十 : log()
"double log(double x)傳回x的自然對數（基數為e 的對數）"
------
#include <stdio.h>
#include <math.h>

int main ()
{
   double x, ret;
   x = 2.7;

   /* 計算 log(2.7) */
   ret = log(x);
   printf("log(%lf) = %lf", x, ret);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-log.html)



---stdlib.h---
範例一 : atof()
"double atof(const char *str) 把參數 str 所指向的字符串轉換為一個浮點數（類型為 double 型）"
------
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
 
int main()
{
   float val;
   char str[20];
   
   strcpy(str, "98993489");
   val = atof(str);
   printf("字符串值 = %s, 浮點值 = %f\n", str, val);
 
   strcpy(str, "runoob");
   val = atof(str);
   printf("字符串值 = %s, 浮點值 = %f\n", str, val);
 
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-atof.html)


範例二 : atoi()
"int atoi(const char *str) 把參數 str 所指向的字符串轉換為一個整數（類型為 int 型）"
------
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
   int val;
   char str[20];
   
   strcpy(str, "98993489");
   val = atoi(str);
   printf("字符串值 = %s, 整數值 = %d\n", str, val);

   strcpy(str, "runoob.com");
   val = atoi(str);
   printf("字符串值 = %s, 整數值 = %d\n", str, val);

   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-atoi.html)


範例三 : abs()
"int abs(int x) 傳回整數 x 的絕對值"
------
#include <stdio.h>
#include <stdlib.h>

int main ()
{
   int a, b;

   a = abs(5);
   printf("a 的值 = %d\n", a);

   b = abs(-10);
   printf("b 的值 = %d\n", b);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-abs.html)


範例四 : ldiv()
"div_t ldiv(long int numer, long int denom) 把 numer（分子）除以 denom（分母），即用於計算兩個長整型數值的商餘數"
------
#include <stdlib.h>
#include <stdio.h>

int main() {
    // 被除數是11，除數是3
    long int numer = 11;
    long int denom = 3;

    ldiv_t result = ldiv(numer, denom);

    printf("商 = %ld\n", result.quot);
    printf("餘數 = %ld\n", result.rem);
    
    return 0;
}
(資料來源:https://www.runoob.com/cprogramming/c-function-ldiv.html)


範例五 : div()
"div_t div(int numer, int denom) 把 numer（分子）除以 denom（分母）"
------
#include <stdio.h>
#include <stdlib.h>

int main()
{
   div_t output;

   output = div(27, 4);
   printf("(27/ 4) 的商  = %d\n", output.quot);
   printf("(27/4) 的餘數 = %d\n", output.rem);

   output = div(27, 3);
   printf("(27/ 3) 的商 = %d\n", output.quot);
   printf("(27/3) 的餘數 = %d\n", output.rem);

   return(0);
}

(資料來源:https://www.runoob.com/cprogramming/c-function-div.html)


範例六 : exit()
"void exit(int status) 用來結束程式，並將 exit 的引數回傳給作業系統"
------
#include <stdio.h>
#include <stdlib.h>

int main ()
{
   printf("程序的開頭....\n");
   
   printf("退出程序....\n");
   exit(0);

   printf("程序的结尾....\n");

   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-exit.html)


範例七 : rand()
"int rand(void)傳回一個範圍在0 到RAND_MAX之間的隨機數"
------
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
 
int main()
{
   int i, n;
   time_t t;
   
   n = 5;
   
   /* 初始化隨機數產生器 */
   srand((unsigned) time(&t));
 
   /* 輸出 0 到 49 之間的 5 個隨機數 */
   for( i = 0 ; i < n ; i++ ) {
      printf("%d\n", rand() % 50);
   }
   
  return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-rand.html)


範例八 : srand()
"void srand(unsigned int seed)種子函式rand使用的隨機數產生器"
------
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
 
int main()
{
   int i, n;
   time_t t;
   
   n = 5;
   
   /* 初始化隨機數產生器 */
   srand((unsigned) time(&t));
 
   /* 輸出 0 到 50 之間的 5 個隨機數 */
   for( i = 0 ; i < n ; i++ ) {
      printf("%d\n", rand() % 50);
   }
   
  return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-srand.html)


範例九 : wctomb()
"int wctomb(char *str, wchar_t wchar)把寬字元wchar轉換成它的多位元組表示形式，並將其儲存在str引用的字元讀寫的起始位置"
------
#include <stdio.h>
#include <stdlib.h>

int main()
{
   int i;
   wchar_t wc = L'a';
   char *pmbnull = NULL;
   char *pmb = (char *)malloc(sizeof( char ));

   printf("要轉換的寬字元：\n");
   i = wctomb( pmb, wc );
   printf("被轉換的字元：%u\n", i);
   printf("多位元組字元：%.1s\n", pmb);
 
   printf("當要轉換的字元為 NULL 時嘗試轉換：\n");
   i = wctomb( pmbnull, wc );
   printf("被轉換的字元：%u\n", i);
   /* 不會輸出任何值 */
   printf("多位元組字元：%.1s\n", pmbnull);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-wctomb.html)


範例十 : mbtowc()
"int mbtowc(whcar_t *pwc, const char *str, size_t n)把一個多位元組序列轉換為一個寬字元"
------
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
   char *str = "這裡是 runoob.com";
   wchar_t mb[100];
   int len;
   
   len = mblen(NULL, MB_CUR_MAX); 

   mbtowc(mb, str, len*strlen(str) );
   
   wprintf(L"%ls \n", mb );   
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-mbtowc.html)



---string.h---
範例一 : strlen()
"size_t strlen(const char *str)strlen 來計算字元陣列裡的字串長度，strlen 計算字串長度是不包含結束字元"
------
#include <stdio.h>
#include <string.h>

int main ()
{
   char str[50];
   int len;

   strcpy(str, "This is runoob.com");

   len = strlen(str);
   printf("|%s| 的長度是 |%d|\n", str, len);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strlen.html)


範例二 : memset()
"void *memset(void *str, int c, size_t n)複製字元c（一個無符號字元）到參數str所指向的字串的前n個字元"
------
#include <stdio.h>
#include <string.h>
 
int main ()
{
   char str[50];
 
   strcpy(str,"This is string.h library function");
   puts(str);
 
   memset(str,'$',7);
   puts(str);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-memset.html)


範例三 : memcmp()
"int memcmp(const void *str1, const void *str2, size_t n))把儲存區str1和儲存區str2的前n個位元組做比較"
------
#include <stdio.h>
#include <string.h>

int main ()
{
   char str1[15];
   char str2[15];
   int ret;

   memcpy(str1, "abcdef", 6);
   memcpy(str2, "ABCDEF", 6);

   ret = memcmp(str1, str2, 5);

   if(ret > 0)
   {
      printf("str2 小於 str1");
   }
   else if(ret < 0) 
   {
      printf("str1 小於 str2");
   }
   else 
   {
      printf("str1 等於 str2");
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-memcmp.html)


範例四 : strcpy()
"char *strcpy(char *dest, const char *src) 把 src 所指向的字串複製到 dest"
------
#include <stdio.h>
#include <string.h>
 
int main()
{
   char src[40];
   char dest[100];
  
   memset(dest, '\0', sizeof(dest));
   strcpy(src, "This is runoob.com");
   strcpy(dest, src);
 
   printf("最終的目標字串： %s\n", dest);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strcpy.html)


範例五 : strtok()
"char *strtok(char *str, const char *delim) 分割字串str為一組字串，delim為分隔符號"
------
#include <string.h>
#include <stdio.h>
 
int main () {
   char str[80] = "This is - www.runoob.com - website";
   const char s[2] = "-";
   char *token;
   
   /* 獲取第一個子字串 */
   token = strtok(str, s);
   
   /* 繼續獲取其他的子字串 */
   while( token != NULL ) {
      printf( "%s\n", token );
    
      token = strtok(NULL, s);
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strtok.html)


範例六 : memchr()
"void *memchr(const void *str, int c, size_t n)在參數str所指向的字串的前n個位元組中搜尋第一次出現字元c（一個無符號字元）的位置"
------
#include <stdio.h>
#include <string.h>
 
int main ()
{
   const char str[] = "http://www.runoob.com";
   const char ch = '.';
   char *ret;
 
   ret = (char*)memchr(str, ch, strlen(str));
 
   printf("|%c| 之後的字串是 - |%s|\n", ch, ret);
 
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-memchr.html)


範例七 : strcat()
"char *strcat(char *dest, const char *src)把src所指向的字串追加到dest所指向的字串的結尾"
------
#include <stdio.h>
#include <string.h>
 
int main ()
{
   char src[50], dest[50];
 
   strcpy(src,  "This is source");
   strcpy(dest, "This is destination");
 
   strcat(dest, src);
 
   printf("最终的目標字串： |%s|", dest);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strcat.html)


範例八 : strcmp()
"int strcmp(const char *str1, const char *str2)把str1所指向的字串和str2所指向的字串做比較"
------
#include <stdio.h>
#include <string.h>
 
int main ()
{
   char str1[15];
   char str2[15];
   int ret;
 
 
   strcpy(str1, "abcdef");
   strcpy(str2, "ABCDEF");
 
   ret = strcmp(str1, str2);
 
   if(ret < 0)
   {
      printf("str1 小於 str2");
   }
   else if(ret > 0) 
   {
      printf("str1 大於 str2");
   }
   else 
   {
      printf("str1 等於 str2");
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strcmp.html)


範例九 : strerror()
"char *strerror(int errnum)從內部陣列中搜尋錯誤號errnum，並傳回一個指向錯誤訊息字串的指標。strerror產生的錯誤字串取決於開發平台和編譯器"
------
#include <stdio.h>
#include <string.h>
#include <errno.h>

int main ()
{
   FILE *fp;

   fp = fopen("file.txt","r");
   if( fp == NULL ) 
   {
      printf("Error: %s\n", strerror(errno));
   }
   
  return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strerror.html)


範例十 : strrchr()
"char *strrchr(const char *str, int c)在參數str所指向的字串中搜尋最後一次出現字元c（一個無符號字元）的位置"
------
#include <stdio.h>
#include <string.h>
 
int main ()
{
   int len;
   const char str[] = "https://www.runoob.com";
   const char ch = '.';
   char *ret;
 
   ret = strrchr(str, ch);
 
   printf("|%c| 之後的字串是 - |%s|\n", ch, ret);
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strrchr.html)



---time.h---
範例一 : asctime()
"char *asctime(const struct tm *timeptr)傳回一個指向字串的指針，它代表了結構struct timeptr的日期和時間"
------
#include <stdio.h>
#include <string.h>
#include <time.h>

int main()
{
   struct tm t;

   t.tm_sec    = 10;
   t.tm_min    = 10;
   t.tm_hour   = 6;
   t.tm_mday   = 25;
   t.tm_mon    = 2;
   t.tm_year   = 89;
   t.tm_wday   = 6;

   puts(asctime(&t));
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-asctime.html)


範例二 : clock()
"clock_t Clock(void)回傳程式執行啟動（一般為程式的起始位置），處理器時脈所使用的時間"
------
#include <time.h>
#include <stdio.h>
 
int main()
{
   clock_t start_t, end_t;
   double total_t;
   int i;
 
   start_t = clock();
   printf("程式啟動，start_t = %ld\n", start_t);
    
   printf("開始一個大迴圈，start_t = %ld\n", start_t);
   for(i=0; i< 10000000; i++)
   {
   }
   end_t = clock();
   printf("大迴圈结束，end_t = %ld\n", end_t);
   
   total_t = (double)(end_t - start_t) / CLOCKS_PER_SEC;
   printf("CPU 占用的總時間：%f\n", total_t  );
   printf("程式退出...\n");
 
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-clock.html)


範例三 : ctime()
"har *ctime(const time_t *timer)傳回一個表示當地時間的字串，當地時間是基於參數timer"
------
#include <stdio.h>
#include <time.h>
 
int main ()
{
   time_t curtime;
 
   time(&curtime);
 
   printf("當前時間 = %s", ctime(&curtime));
 
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-ctime.html)


範例四 : time()
"time_t time(time_t *seconds)傳回自紀元Epoch（1970-01-01 00:00:00 UTC）起經過的時間，以秒為單位。如果seconds不為空，則傳回值也儲存在變數seconds中"
------
#include <stdio.h>
#include <time.h>
 
int main ()
{
  time_t seconds;
 
  seconds = time(NULL);
  printf("自 1970-01-01 起的小時數 = %ld\n", seconds/3600);
  
  return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-time.html)


範例五 : localtime()
"struct tm *localtime(const time_t *timer)使用timer 的值來填入tm結構。timer的值被分解為tm結構，並以本地時區表示"
------
#include <stdio.h>
#include <time.h>
 
int main ()
{
   time_t rawtime;
   struct tm *info;
   char buffer[80];
 
   time( &rawtime );
 
   info = localtime( &rawtime );
   printf("當前的本地時間和日期：%s", asctime(info));
 
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-localtime.html)


範例六 : difftime()
"double difftime(time_t time1, time_t time2)傳回time1和time2之間相差的秒數(time1 - time2)。這兩個時間是在日曆時間中指定的，表示了自紀元Epoch（協調世界時UTC：1970-01-01 00:00:00）起經過的時間"
------
#include <stdio.h>
#include <time.h>
#ifdef _WIN32
#include <Windows.h>
#else
#include <unistd.h>
#endif
 
int main ()
{
   time_t start_t, end_t;
   double diff_t;
 
   printf("程式啟動...\n");
   time(&start_t);
 
   printf("休眠 5 秒...\n");
   sleep(5);
 
   time(&end_t);
   diff_t = difftime(end_t, start_t);
 
   printf("執行時間 = %f\n", diff_t);
   printf("程式退出...\n");
 
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-difftime.html)


範例七 : gmtime()
"struct tm *gmtime(const time_t *timer)使用timer的值來填入tm結構，並以協調世界時（UTC）也稱為格林尼治標準時間（GMT）表示"
------
#include <stdio.h>
#include <time.h>
 
#define BST (+1)
#define CCT (+8)
 
int main ()
{
 
   time_t rawtime;
   struct tm *info;
 
   time(&rawtime);
   /* 獲取 GMT 時間 */
   info = gmtime(&rawtime );
   
   printf("當前的世界時鐘：\n");
   printf("倫敦：%2d:%02d\n", (info->tm_hour+BST)%24, info->tm_min);
   printf("中國：%2d:%02d\n", (info->tm_hour+CCT)%24, info->tm_min);
 
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-gmtime.html)


範例八 : mktime()
"time_t mktime(struct tm *timeptr)把timeptr所指向的轉換轉換為自 1970 年 1 月 1 日以來持續時間的秒數，發生錯誤時傳回-1"
------
#include <stdio.h>
#include <time.h>

int main () {
    int ret;
    struct tm info;
    char buffer[80];

    info.tm_year = 2021 - 1900;
    info.tm_mon = 7 - 1;
    info.tm_mday = 4;
    info.tm_hour = 0;
    info.tm_min = 0;
    info.tm_sec = 1;
    info.tm_isdst = -1;

    ret = mktime(&info);
    if( ret == -1 ) {
        printf("Error: unable to make time using mktime\n");
    } else {
        strftime(buffer, sizeof(buffer), "%c", &info );
        printf(buffer);
    }

    return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-mktime.html)


範例九 : strftime()
"size_t strftime(char *str, size_t maxsize, const char *format, const struct tm *timeptr)根據format中定義的格式化規則，格式化結構timeptr表示的時間，並把它儲存在str中"
------
#include <stdio.h>
#include <time.h>
 
int main ()
{
   time_t rawtime;
   struct tm *info;
   char buffer[80];
 
   time( &rawtime );
 
   info = localtime( &rawtime );
 
   strftime(buffer, 80, "%Y-%m-%d %H:%M:%S", info);
   printf("格式化的日期 & 時間 : |%s|\n", buffer );
  
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-strftime.html)




