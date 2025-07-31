## โจทย์
จงเขียนโปรแกรมรับค่าตัวเลขจากผู้ใช้ ใส่ไว้ในตัวแปร N และทำการแสดงข้อมูลดังเงื่อนไขต่อไปนี้
<br />- หากผู้ใช้กรอกเลขคี่ ให้โปรแกรมแสดงลำดับตัวเลขตั้งแต่ 1 ถึง N และให้แสดงเฉพาะตัวเลขคี่เท่านั้น
<br />- หากผู้ใช้กรอกเลขคู่ ให้โปรแกรมแสดงลำดับตัวเลขตั้งแต่ N ถึง 0 และให้แสดงเฉพาะตัวเลขคู่เท่านั้น

## FIX CODE
```c++
#include <stdio.h>

int input = -1 ;// ตั้ง -1 เพราะกัน input ที่เป็นอักษร

int main() {
    printf( "enter value: \n" ) ;
    scanf( " %d" , &input ) ;
    if ( input < 0 ) {
        printf( "กรุณาใส่ตัวเลข\n" ) ;
        return 0 ; //ทำการจบการทำงาน
    }//end if
    else if ( input %2 == 0 ) {
        printf( "Series: " ) ;
        for ( int i = input ; i >= 0 ; i-- ) {
            if (i % 2 == 0) {
                printf( "%d ", i ) ;
            }//end if
        }//end for
    }//end else if
    else if ( input %2 != 0 ) {
        printf( "Series: " ) ;
        for ( int i = 0 ; i <= input ; i++ ) {
            if ( i %2 != 0 ) {
                printf( "%d ", i ) ;
            }//end if
        }//end for
    }//end else if
    return 0 ;
}//end function
```
## TEST CASE 1
<img width="248" height="65" alt="Screenshot 2025-07-31 111321" src="https://github.com/user-attachments/assets/86a23bc9-e144-4b63-a708-5d06e1d1f6b4" />

## TEST CASE 2
<img width="437" height="100" alt="Screenshot 2025-07-31 111548" src="https://github.com/user-attachments/assets/76e1517d-565f-4c66-84b3-d198c51ebf2b" />


