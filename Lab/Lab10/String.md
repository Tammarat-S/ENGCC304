```c++
#include <stdio.h>
#include <string.h>

int main(){
    char sentence[100] ;    //สร้างstringเก็บข้อความ
    char check[100] ;       //สร้างstringเก็บข้อความที่เรียงจากหลังไปหน้า
    int compare ;           //ตัวแปรสำหรับเปรัียบเทียบข้อความ
    
    //----|รับข้อความ
    printf( "Enter word: \n" ) ;
    scanf( "%s" , sentence ) ;
    
    //----|นับจำนวนตัวอักษรสำหรับกำหนดขอบเขตวนลูป
    int n = strlen(sentence) ;

    //----|เรียงข้อความจากหลังไปหน้า
    for (int i = 0; i <= n ; i++) {
       check[i] = sentence[n-i-1] ;
    }                       //end for

    //----|เปรียบเทียบข้อความ
    compare = strcmp(sentence,check) ;

    //----|แสดงผล
    if(compare == 0){ //ถ้าเหมือนกัน
        printf("pass") ; 
    }else{                  //ถ้าไม่เหมือนกัน
        printf("Not pass") ;
    }                       //end if
    return 0 ;              //คืนค่า 0 เพื่อจบการทำงาน
}                           //end function
```
<img width="132" height="67" alt="Screenshot 2025-10-07 144738" src="https://github.com/user-attachments/assets/972c32ee-3187-46c5-9d4b-cdf0fdc9a0f1" />

