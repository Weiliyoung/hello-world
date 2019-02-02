 #include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct Student
{
    char num[20];
    char name[24];
    char sex;
    char school[20];
    char subject[20];
    char phone[20];
    char qq[20];
    char wechat[20];
    char address[20];
} student;

void add_student(student stu[50], student stu_new);
// void search_student(student stu[N], void *keyword);
// void delete_student(student stu[N], void *keyword);
void list_student(student stu[50]);

void main()
{
    int friendnumber = 0;
    int choice = 0;
    student stu[50];
    void *keyword;
    student stu_new;
    while (1)
    {
        printf("1: 新增同学录\n");
        printf("2: 查找同学录\n");
        printf("3: 删除同学录\n");
        printf("4: 查看同学录\n");
        printf("0: 退出\n");
        printf("\n 请选择输入(0 - 4):");
        scanf("%d", &choice);
        switch (choice)
        {
        case 1:
            printf("请输入学号:");
            scanf("%s", stu_new.num);
            printf("\n");
            add_student(stu, stu_new);
        case 2:
        case 3:
        case 4:
            list_student(stu);
        }
    }
}

void add_student(student stu[50], student stu_new)
{
    printf("%s", stu_new.num);
    printf("\n");
}

void list_student(student stu[50])
{
    FILE *fp;
    int i = 0;

    if ((fp = fopen("test.txt", "r")) == NULL)
    {
        printf("Can not open file\n");
        return;
    }
    while (!feof(fp))
    {
        fscanf(fp, "%s %s %c %s %s %s %s %s %s %s", &stu[i].num, &stu[i].name, &stu[i].sex, &stu[i].school, &stu[i].subject, &stu[i].phone, &stu[i].qq, &stu[i].wechat, &stu[i].address);
        i++;
    }
    fclose(fp);
    for (int j = 0; j < 11; j++)
    {
        printf("%s %s %c %s %s %s %s %s %s %s\n", &stu[j].num, &stu[j].name, &stu[j].sex, &stu[j].school, &stu[j].subject, &stu[j].phone, &stu[j].qq, &stu[j].wechat, &stu[j].address);
    }
    return;
}
