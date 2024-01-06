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
















   
