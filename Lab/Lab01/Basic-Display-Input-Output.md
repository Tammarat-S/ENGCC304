## โจทย์
จงแก้ไขโค้ดต่อไปนี้ ให้สามารถรับค่าจากผู้ใช้ เพื่อแสดงผลบนหน้าจอคอมพิวเตอร์ให้ได้ พร้อมทั้งจัดรูปแบบให้ตรงตาม Syntax ที่เรียนมาในห้องเรียน

```c++
#include <stduio.h>

int main() {
    char Name[50] ;
    int  Age = 0 ;
    printf( "Enter your name: " ) 
    scanf( "%s", Name ) ;
    printf( "Enter your age: " ) ;
    scanf( "%d", Age ) ;
    print( "- - - - - -\n" ) ;
    printf( "Hello %s \n", ___ ) ; 
    printf( "Age = %d\n", ___ ) ; 
    
}//end main function
```

## FIX CODE
```c++
#include <stdio.h>

int main() {
    char Name[50] ;
    int  Age = 0 ;
    printf( "Enter your name: " ) ;
    scanf( "%s", Name ) ;
    printf( "Enter your age: " ) ;
    scanf( "%d", &Age ) ;
    printf( "- - - - - -\n" ) ;
    printf( "Hello %s \n", Name ) ; 
    printf( "Age = %d\n", Age ) ; 

    return 0 ;
    
}
```

## TEST CASE
### Input
```bash
Enter your name: Tammarat_Suriyawong
Enter you age: 18
```
![Screenshot 2025-07-03 120720](https://github.com/user-attachments/assets/e44d12ef-24c3-46aa-845e-da89404e4b16)


### Output
```bash
- - - - - -
Hello Tammarat_Suriyawong
Age = 18
```
![image](https://github.com/user-attachments/assets/1533c7ae-5230-46ec-878e-f12361f1b782)

## มาตรฐานการตรวจตามหลักการเรียนรู้ของบลูม
| ลำดับการเรียนรู้ | เกณฑ์การวัด | คะแนน |
| -------- | -------- | -------- |
| รู้จำ | เห็นโครงสร้างของโค้ดโปรแกรมชัดเจน ได้มาตรฐาน | 1 pts |
| เข้าใจ | แก้ไขปัญหาได้ตามที่โจทย์กำหนด | 1 pts |
| ประยุกต์ใช้ | สามารถผ่านเงื่อนไขได้ทุก testcase | 1 pts |
| วิเคราะห์ | หาจุดผิดของโปรแกรมได้ | 1 pts |
| ประเมินค่า | โปรแกรมเสร็จสมบูรณ์ระยะเวลาที่กำหนด | 1 pts |
| สร้างสรรค์ | แก้ไขสถานการณ์ของโจทย์ | 1 pts |
||<p style='text-align: right !important;'>**รวม**</p>|**6 pts**|
