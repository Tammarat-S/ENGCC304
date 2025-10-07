```c++
#include <stdio.h>
#include <string.h>

//----|สร้างโครงสร้างข้อมูลนักศึกษา
struct Student {
    char Name[20] ;
    char ID[5] ;
    float ScoreSub1 ;
    float ScoreSub2 ;
    float ScoreSub3 ;
    float ScoreSub4 ;
    float ScoreSub5 ;
} typedef S ;

void Grade (float Score) ;

int main(){
    int n = 3 ; int i = 0 ;
    S list[n] ;
    float sum ;                 //ตัวแปรเก็บคะแนนรวม
    char first[20], last[20];   //ตัวแปรเก็บชื่อและนามสกุล
    printf("Enter the details of 3 students") ;
    //----|รับข้อมูลชื่อนักศึกษา รหัสนักศึกษา และคะแนน
    for ( i = 0 ; i < n ; i++ ) {
        printf("Student[%d]\n",i+1) ;
        printf("Name:") ;
        scanf("%s %s", first, last);
        strcpy(list[i].Name, first);
        strcat(list[i].Name," ");
        strcat(list[i].Name,last);
        printf("ID:") ;
        scanf("%s",list[i].ID) ;
        printf("Scores in Subject 1:") ;
        scanf("%f",&list[i].ScoreSub1) ;
        printf("Scores in Subject 2:") ;
        scanf("%f",&list[i].ScoreSub2) ;
        printf("Scores in Subject 3:") ;
        scanf("%f",&list[i].ScoreSub3) ;
        printf("Scores in Subject 4:") ;
        scanf("%f",&list[i].ScoreSub4) ;
        printf("Scores in Subject 5:") ;
        scanf("%f",&list[i].ScoreSub5) ;
        }//end for      
    //----|แสดงผลชื่อนักศึกษา รหัสนักศึกษา คะแนน เกรด และคะแนนเฉลี่ย
    for(i = 0 ; i < n ; i++) {
        sum = 0 ;
        printf("\nName: %s\n",list[i].Name) ;
        printf("ID: %s\n",list[i].ID) ;
        printf("Scores :") ;
        printf(" %0.f",list[i].ScoreSub1) ;
        printf(" %0.f",list[i].ScoreSub2) ; 
        printf(" %0.f",list[i].ScoreSub3) ;
        printf(" %0.f",list[i].ScoreSub4) ;
        printf(" %0.f",list[i].ScoreSub5) ;
        sum = list[i].ScoreSub1 + list[i].ScoreSub2 + list[i].ScoreSub3 + list[i].ScoreSub4 + list[i].ScoreSub5 ; //คำนวณคะแนนรวม
        printf("\nGrade: ") ;
        Grade(list[i].ScoreSub1) ;
        Grade(list[i].ScoreSub2) ;
        Grade(list[i].ScoreSub3) ;
        Grade(list[i].ScoreSub4) ;
        Grade(list[i].ScoreSub5) ;
        printf("\nAverage: %.2f\n",sum/5) ;             //แสดงคะแนนเฉลี่ย
        }//end for
}//end main

//----|ฟังก์ชันให่เกรด
void Grade ( float Score) {
        if( Score >= 80 ) {
            printf( "A " ) ;
        }else if ( Score >= 75 && Score < 80 ) {
            printf( "B+ " ) ;
        }else if ( Score >= 70 && Score < 75 ) {
            printf( "B " ) ;
        }else if ( Score >= 65 && Score < 70 ) {
            printf( "C+ " ) ;
        }else if ( Score >= 60 && Score < 65 ) {
            printf( "C " ) ;
        }else if ( Score >= 55 && Score < 60 ) {
            printf( "D+ " ) ;
        }else if ( Score >= 50 && Score < 55 ) {
            printf( "D " ) ; 
        }else if ( Score < 50 && Score >= 0 ) {
            printf( "F " ) ;
        }//end if else
}//end Grade
```
<img width="1658" height="917" alt="Screenshot 2025-10-07 152126" src="https://github.com/user-attachments/assets/26efc1b5-08ad-4c87-ad05-5955a4ff6b56" />

