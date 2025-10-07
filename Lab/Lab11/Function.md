```c++
#include <stdio.h>
#include <string.h>
#include <math.h>

//----|ฟังก์ชันคำนวณผลรวมของเลขยกกำลัง
int calculate(char check[]){
    int input[100] ;                //----|ตัวแปรสำหรับเก็บต่าจัวเลขที่แปลงจากตัวอักษร
    int sum = 0 ;                   //----|ตัวแปรสำหรับเก็บผลรวมของเลขยกกำลัง
    int n = strlen(check) ;         //----|หาหลักของตัวเลข
    //----|แปลงตัวอักษรเป็นตัวเลข
    for ( int i = 0 ; i < n ; i++ ) {
        input[i] = check[i] - '0' ; //----|แปลงตัวอักษรเป็นจัวเลขโดยการลบด้วย '0' ที่มีค่าเท่ากับ 48
    }//end for
    //----|คำนวณผลรวมของเลขยกกำลัง
    for(int i = 0 ; i < n ; i++){
        sum += pow(input[i], n ) ;
    }//end for
    return sum ;                    //----|ส่งค่าผลรวมกลับเป็นจำนวนเต็ม
}
//----|ฟังก์ชันตรวจสอบผลรวมว่าเป็นเลขอาร์มสตรองหรือไม่
void armscheck( int sum , char check[]) {
    
    if ( sum == atoi(check) ) {     //----|ใช้ฟังก์ชัน atoi() แปลงตัวอักษรเป็นจำนวนเต็มและเปรียบเทียบกับผลรวม
        printf( "Pass" ) ;
    } else {
        printf( "Not Pass" ) ;
    }//end if-else
}//end armscheck

int main(){
    //----|รับค่าตัวเลขจากผู้ใช้
    char check[100] ;
    printf("Enter number: ") ;
    scanf("%s", check) ;
    int sum = calculate(check) ;    //----|เรียกใช้ฟังก์ชันคำนวณผลรวมของเลขยกกำลัง
    armscheck(sum, check) ;         //----|เรียกใช้ฟังก์ชันตรวจสอบผลรวม

    return 0 ;
}
```
<img width="237" height="44" alt="Screenshot 2025-10-07 150502" src="https://github.com/user-attachments/assets/f8176a33-d8af-4ee6-ba80-622d6dd1b5e1" />

