# storing-student-mark
#include<stdio.h>
int main(){
char name[100];
int marks;
int num,i,j,p,n;
FILE*f;
f=fopen("my_file.txt","w");
printf("enter number of students:");
scanf("%d",&num);
for(i=0;i<num;i++){
printf("enter name of student %d:",i+1);
scanf("%s",&name);
fprintf(f,"%s\n",name);
printf("enter marks of student:");
scanf("%d",&marks);
fprintf(f,"%d\n",marks);
}
fclose(f);
printf("\n-----------------------\n");
printf("student list:\n");
f=fopen("my_file.txt","r");
for(j=0;j<num;j++){
fscanf(f,"%s",&name);
fscanf(f,"%d",&marks);
printf("%d)%s:%d\n",j+1,name,marks);
}
return 0;
}

