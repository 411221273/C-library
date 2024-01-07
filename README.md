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
    
   printf("請輸入字符串： ");
   scanf("%s", str);
   assert(str != NULL);
   printf("輸入的字符串是： %s\n", str);
    
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
  
   /* 輸出字符串直到控制字符 \a */
   
   while( !iscntrl(str1[i]) ) 
   {
      putchar(str1[i]);
      i++;
   }
  
   /* 輸出字符串直到控制字符 \n */
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
       printf("var1 = |%c| 是標點符號字符\n", var1 );
   }
   else
   {
       printf("var1 = |%c| 不是標點符號字符\n", var1 );
   }
   if( ispunct(var2) )
   {
       printf("var2 = |%c| 是標點符號字符\n", var2 );
   }
   else
   {
       printf("var2 = |%c| 不是標點符號字符\n", var2 );
   }
   if( ispunct(var3) )
   {
       printf("var3 = |%c| 是標點符號字符\n", var3 );
   }
   else
   {
       printf("var3 = |%c| 不是標點符號字符\n", var3 );
   }
   return(0);
}  
(資料來源:https://www.runoob.com/cprogramming/c-function-ispunct.html)


範例八 : isspace()
"用於檢查所傳的字符是否是空白字符"
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
       printf("var1 = |%c| 是空白字符\n", var1 );
   }
   else
   {
       printf("var1 = |%c| 不是空白字符\n", var1 );
   }
   if( isspace(var2) )
   {
       printf("var2 = |%c| 是空白字符\n", var2 );
   }
   else
   {
       printf("var2 = |%c| 不是空白字符\n", var2 );
   }
   if( isspace(var3) )
   {
       printf("var3 = |%c| 是空白字符\n", var3 );
   }
   else
   {
       printf("var3 = |%c| 不是空白字符\n", var3 );
   }
   
   return(0);
}
(資料來源:https://www.runoob.com/cprogramming/c-function-isspace.html)


範例九 : isxdigit()
"用於檢查所傳的字元是否為十六進位數字"
------
#include < ctype.h > 
#include < stdio.h > 
 
int main ( ) { char c = ' 5 ';
    int result ;
 
    // 傳入字符  
     
   result = isxdigit ( c ) ; // result 回傳非0
   printf ( " %c 傳入到isxdigit() 函數結果為: %d " , c , isxdigit ( c ) ) ;
    printf ( " \ n " ) ;   // 換行
   c = ' M ';
 
    // 非十六進位數為參數
   result = isxdigit ( c ) ; // result 為0
 
   printf ( " %c 傳入到isxdigit() 函數結果為: %d " , c , isxdigit ( c ) ) ;
 
    return 0 ;
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


範例五 : exit()
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












































