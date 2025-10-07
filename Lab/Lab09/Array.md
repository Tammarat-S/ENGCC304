```c++
#include <stdio.h>

int main(){
    int Num[100] ; //สร้างอาเรย์เก็บค่าตัวเลข
    int N = 0 ; //ตัวแปรเก็บขนาดของอาเรย์
    int i = 0 ; // สร้างตัวแปรสำหรับใช้ในการวนลูป
    int num = 0 ; //ตัวแปรเก็บค่าตัวเลขที่รับเข้ามา
    //----|ใส่ขนาดของอาเรย์
    printf( "Enter N \n" ) ;
    scanf( "%d" , &N ) ;
    //----|เช็คว่าขนาดของอาเรย์อยู่ในช่วงที่กำหนดหรือไม่และเป็นตัวเลขหรือไม่
    if( N < 1 || N > 15 ) {
        printf( "Please enter a number between 1 and 10\n" ) ;
        return 0 ;
    }//end if
    //----|ใส่ค่าตัวเลขลงในอาเรย์
    for( i = 0 ; i < N ; i++ ) {
        printf( "Enter value [%d] : \n" , i ) ;
        scanf( "%d" , &Num[i] ) ;
    }//end for
    //----|แสดงตำแหน่งของอาเรย์
    printf( "index:" ) ;
    for( i = 0 ; i < N ; i++ ) {
        printf( " %d" , i ) ;
    }//end for
    //----|แสดงค่าตัวเลขในอาเรย์และเช็คว่าเป็นจำนวนเฉพาะหรือไม่
    printf( "\nArray:" ) ;
    //----|วนลูปเช็คจำนวนเฉพาะ
    for( i = 0 ; i < N ; i++ ) {
        num = Num[i] ; //เก็บค่าตัวเลขจากอาเรย์ลงในตัวแปร num
        //----|เช็คว่าค่าตัวเลขเป็นจำนวนเฉพาะหรือไม่
        for( int a = 2 ;a <= num ; a++ ) {
            if (num == 2) {  //ถ้าเป็น 2 ซึ่งเป็นจำนวนเฉพาะ
                printf( "%2d" , num ) ;
                break ; //ออกลูปforแล้ววนลูปค่าตัวเลขถัดไป
            }else if( num % a == 0 ) { //ถ้าไม่ใช่จำนวนเฉพาะ
                printf( " #" ) ;
                break ; //ออกลูปforแล้ววนลูปค่าตัวเลขถัดไป
            }else if ( a == num - 1 ) {
                printf( "%2d" , num ) ;
                break ; //ออกลูปforแล้ววนลูปค่าตัวเลขถัดไป
            }
            }//end if
        }//end for
        return 0 ; //คืนค่า 0 เพื่อจบการทำงาน
    }//end function
   ```
## TEST CASE
### Input & Output
<img width="401" height="312" alt="Screenshot 2025-10-07 140833" src="https://github.com/user-attachments/assets/934125b9-b764-4446-bf58-93a53c64aa16" />


