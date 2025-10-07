#include <stdio.h>

int main(){
    int BaseSalaly = 0 ;
    int yearofwork = 0 ;
    int bonus = 0 ;
    int specialbonus = 0 ;
    int totalsalary = 0 ; 
    int position = 0 ;
    //----|รับค่าตำแหน่ง
    printf("Position: ") ;
    scanf("%d",&position) ;
    //----|เช็คว่าตำแหน่งอยู่ในช่วงที่กำหนดหรือไม่
    if (position < 1 || position > 3) {
        printf("Please enter a number between 1 and 3.\n") ;
        return 0 ;
    }//end if
    //----|กำหนดเงินเดือนตามตำแหน่ง
    switch (position) {
        case 1:
            printf("(Junior Programmer)\n") ;
            BaseSalaly = 20000 ;
            break ;
        case 2:
            printf("(Mid-Level Programmer)\n") ;
            BaseSalaly = 35000 ;
            break ;
        case 3:
            printf("(Senior Programmer)\n") ;
            BaseSalaly = 50000 ;
            break ;
        default:
            break;
    }//end switch
    //----|รับค่าปีที่ทำงาน
    printf("Year of experience: ") ;
    scanf("%d",&yearofwork) ;
    //----|เช็คว่าค่าปีที่ทำงานเป็นค่าที่ถูกต้องหรือไม่
    if (yearofwork < 0){
        printf("Please enter a correct number.\n") ;
        return 0 ;
    }//end if
    //----|คำนวณโบนัสตามปีที่ทำงาน
    if (yearofwork == 0) {
        bonus = 0 ;
    }else if (yearofwork >= 1 && yearofwork <= 3) {
        bonus = BaseSalaly * 0.1 ;
    }else if (yearofwork >= 4 && yearofwork <= 5) {
        bonus = BaseSalaly * 0.15 ;
    }else if (yearofwork > 5) {
        bonus = BaseSalaly * 0.2 ;
    }//end if
    //----|รับค่าจำนวนโปรเจคที่ทำได้ในปีนี้
    printf( "Number of project completed this year: " ) ;
    scanf( "%d",&specialbonus ) ;
    //----|เช็คว่าค่าจำนวนโปรเจคที่ทำได้ในปีนี้เป็นค่าที่ถูกต้องหรือไม่
    if ( specialbonus < 0 ) {
        printf( "Please enter a correct number.\n" ) ;
        return 0 ;
    }//end if
    //----|คำนวณโบนัสพิเศษ
    if ( specialbonus > 5 ) {
        specialbonus = BaseSalaly * 0.05 ;
    }else {
        specialbonus = 0 ;
    }//end if 
    //----|คำนวณเงินเดือน
    totalsalary = BaseSalaly + bonus + specialbonus ;
    //----|แสดงผล
    printf( "Base Salary:   %d THB\n" ,BaseSalaly ) ;
    printf( "Bonus:         %d THB\n",bonus ) ;
    printf( "Special Bonus: %d THB\n" ,specialbonus ) ;
    printf( "Total Salary:  %d THB\n" ,totalsalary ) ;
    return 0 ;
}//end function
