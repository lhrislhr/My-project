#include<stdio.h>
#include<math.h>
#include<stdlib.h>
#include<time.h>
float translate_unit (int a , float b)
{
if (a == 1)
{
    b = b / 10 ;
    return b ;
}
else if (a == 2)
{
    return b;
}
else if (a == 3)
{
    b = b*10;
    return b;
}
}




 int main()
 {
    float length1,length2;
   //边长1
    printf("input the first length of the triangle's side(边长>0且边长不能<10cm):");
    scanf("%f",&length1);
    int a = 0;
    printf("选择单位:1 = mm, 2 = cm, 3 = m");
    scanf("%d",&a);
    length1 = translate_unit(a,length1);
    //边长2
    printf("input the second length of the triangle's side:");
    scanf("%f",&length2);
    int b=0;
    printf("选择单位:1=mm, 2=cm, 3=m");
    scanf("%d",&b);
    length2 = translate_unit(b,length2);
    
    printf("边长1为%fcm\n\
    边长2为%fcm",length1,length2);
    
    


        while (length1<0||length2<0)
            {
                printf("error,你个傻逼，边长不能为负数,请再次输入。");
                //边长1
                printf("input the first length of the triangle's side(边长>0且边长不能<10cm):");
                scanf("%f",&length1);
                int a = 0;
                printf("选择单位:1 = mm, 2 = cm, 3 = m");
                scanf("%d",&a);
                length1 = translate_unit(a,length1);
                //边长2
                printf("input the second length of the triangle's side:");
                scanf("%f",&length2);
                int b=0;
                printf("选择单位:1=mm, 2=cm, 3=m");
                scanf("%d",&b);
                length2 = translate_unit(b,length2);
                
                printf("边长1为%fcm,边长2为%fcm",length1,length2);

            }


            while (length1<10||length2<10)
            {
            printf("error,一边或两边<10cm,");
            //边长1
            printf("请重新输入。input the first length of the triangle's side(边长>0且边长不能<10cm):");
            scanf("%f",&length1);
            int a = 0;
            printf("选择单位:1 = mm, 2 = cm, 3 = m");
            scanf("%d",&a);
            length1 = translate_unit(a,length1);
            //边长2
            printf("input the second length of the triangle's side:");
            scanf("%f",&length2);
            int b=0;
            printf("选择单位:1=mm, 2=cm, 3=m");
            scanf("%d",&b);
            length2 = translate_unit(b,length2);
            
            printf("边长1为%fcm\n\
            边长2为%fcm",length1,length2);
            }




            while (length1<length2*0.1||length2<length1*0.1)
            {
                printf("error,一边小于另一边的百分之10");
                //边长1
                printf("input the first length of the triangle's side(边长>0且边长不能<10cm):");
                scanf("%f",&length1);
                int a = 0;
                printf("选择单位:1 = mm, 2 = cm, 3 = m");
                scanf("%d",&a);
                length1 = translate_unit(a,length1);
                //边长2
                printf("input the second length of the triangle's side:");
                scanf("%f",&length2);
                int b=0;
                printf("选择单位:1=mm, 2=cm, 3=m");
                scanf("%d",&b);
                length2 = translate_unit(b,length2);
                
                printf("边长1为%fcm,边长2为%fcm",length1,length2);

            }
            
    /*计算*/    
    double A=length1+length2;//大
    double B=length1-length2;//小
    double abs_B=fabs(B);
    double length3;
    srand(time(NULL));
    int i = rand();
    //printf("i=%d\n",i);
    double n;
    n = (double) i ;
    //printf("n=%f\n",n);
    double x = fmod(n,A+1);
    //printf("x=%f\n",x);
    length3 = x;
{
    
}
    float square;
    square=(length1+length2+length3)*(length1+length2-length3)*(length1+length3-length2)*(length2+length3-length1);
    float area;
    area=(float)sqrt(square);     //运算是否能正常进行？
    
     printf("\n\
边长1:  %fcm,\n\
边长2:  %fcm, \n\
边长3:  %fcm(random)",length1,length2,length3);
     printf("\n\
面积%f 平方厘米",area);

    
     
    return 0;






 }   
