## โจทย์
เขียนโปรแกรมภาษาซีเพื่อรับข้อมูลพนักงานของบริษัทซอร์ฟแวร์ โดยรับข้อมูล รหัสประจำตัวพนักงาน , จำนวนชั่วโมงที่ทำงาน , รายได้ต่อชั่วโมง จากนั้นให้แสดงข้อมูลเลขประจำตัวพนักงาน พร้อมกับรายได้ทั้งหมดที่หนักงานจะได้รับทั้งหมด

## CODE
```c++
#include <stdio.h>

int main(){
    char ID[11] ;
    int workhrs ;
    int salary ;
    printf( "Input Employees ID Max. 10 chars):\n" ) ;
    scanf( "%10s" , ID ) ;
    printf( "Input the working hrs: \n" ) ;
    scanf( "%d" , &workhrs ) ;
    printf( "Salary amount/hr:\n" ) ;
    scanf( "%d" , &salary ) ;
    printf( "Expected Output:\n" ) ;
    printf( "Employees ID = %s \n" ,ID ) ;
    printf( "Salary = U$ %0.2f" , (float)(salary*=workhrs) ) ;

    return 0 ;

}// end function
```
## TEST CASE 1
### Input
<img width="324" height="133" alt="Screenshot 2025-07-25 105018" src="https://github.com/user-attachments/assets/cd2d30f2-4f20-4a52-8417-bf658f2f2839" />

### Output
<img width="261" height="63" alt="Screenshot 2025-07-25 105113" src="https://github.com/user-attachments/assets/99c957d3-e939-4c8f-95b7-dc6ebd56d7f8" />

## TEST CASE 2
### Input
<img width="335" height="129" alt="Screenshot 2025-07-25 105251" src="https://github.com/user-attachments/assets/a7a42bc5-7997-4d1f-a5ec-ce0feedb44d2" />

### Output
<img width="317" height="68" alt="Screenshot 2025-07-25 105409" src="https://github.com/user-attachments/assets/7fbd89e0-5598-4bce-bfb9-cf6d635e0ca7" />

