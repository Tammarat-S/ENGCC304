## โจทย์
ผู้ใช้กรอกค่า "คะแนนดิบ" เข้ามาในระบบเพื่อต้องการตรวจสอบเกรดในรายวิชา Programming ซึ่งมีเกณฑ์การให้คะแนนคือ 
<br />F อยู่ในช่วงคะแนนน้อยกว่า 50 , 
<br />D อยู่ในช่วงระหว่าง 50 ถึง 55 , 
<br />D+ อยู่ในช่วงระหว่าง 55 ถึง 60 , 
<br />C อยู่ในช่วงระหว่าง 60 ถึง 65 , 
<br />C+ อยู่ในช่วงระหว่าง 65 ถึง 70 , 
<br />B อยู่ในช่วงระหว่าง 70 ถึง 75 , 
<br />B+ อยู่ในช่วงระหว่าง 75 ถึง 80 , 
<br />A อยู่ในช่วงคะแนนมากกว่า 80 ขึ้นไป 
<br /><br />(กำหนดให้ข้อนี้ใช้คำสั่ง if else ได้เท่านั้น)

## FIX CODE
```c++
#include <stdio.h>

int main(){
    int score = -1 ;
    printf( "Please enter your score : " ) ;
    scanf( "%d" , &score ) ;
    printf( "Grade : " ) ;
    if( score >= 80 ) {
        printf( "A !" ) ;
    }else if ( score >= 75 && score < 80 ) {
        printf( "B+ !" ) ;
    }else if ( score >= 70 && score < 75 ) {
        printf( "B !" ) ;
    }else if ( score >= 65 && score < 70 ) {
        printf( "C+ !" ) ;
    }else if ( score >= 60 && score < 65 ) {
        printf( "C !" ) ;
    }else if ( score >= 55 && score < 60 ) {
        printf( "D+ !" ) ;
    }else if ( score >= 50 && score < 55 ) {
        printf( "D !" ) ; 
    }else if ( score < 50 && score >= 0 ) {
        printf( "F !" ) ;
    }else {
        printf( "Please enter number only." ) ;
    }//end if
    return 0 ;
}//end function
```

## TEST CASE 1
<img width="279" height="48" alt="Screenshot 2025-07-25 144514" src="https://github.com/user-attachments/assets/d13a81fa-7918-4b95-b691-150e24b4444a" />

## TEST CASE 2
<img width="283" height="48" alt="Screenshot 2025-07-25 144703" src="https://github.com/user-attachments/assets/9a766daf-92e3-407a-a877-5f84e8b8fb0f" />

## TEST CASE 3
<img width="364" height="42" alt="Screenshot 2025-07-25 144949" src="https://github.com/user-attachments/assets/f9af7b6a-ceda-477c-b2b0-dedaf842970c" />

## TEST CASE 4
<img width="308" height="48" alt="Screenshot 2025-07-25 145101" src="https://github.com/user-attachments/assets/f06877e5-b539-4be1-8560-6ab33d5c4077" />

## TEST CASE 5
<img width="369" height="46" alt="Screenshot 2025-07-25 145156" src="https://github.com/user-attachments/assets/43fef7dc-0600-4f8d-b981-bf8e9fdedfbc" />
