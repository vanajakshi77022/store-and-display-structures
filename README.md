# store-and-display-structures
PROGRAM:
#include <stdio.h>
struct student {
    int roll_no;
    char name[100];
    float marks1, marks2, marks3;
};
int main() {
    int n, i;
    printf("25331A05E8\n");
    printf("Enter number of students: ");
    scanf("%d", &n);
    getchar(); 
    struct student s[n];
    for(i = 0; i < n; i++) {
        printf("\nEnter details of student %d\n", i + 1);
        printf("Roll Number: ");
        scanf("%d", &s[i].roll_no);
        getchar(); 
        printf("Name: ");
        fgets(s[i].name, sizeof(s[i].name), stdin);
        printf("Marks in 3 subjects: ");
        scanf("%f %f %f", &s[i].marks1, &s[i].marks2, &s[i].marks3);
        getchar(); 
    }
    printf("\n");
    for(i = 0; i < n; i++) {
        float total = s[i].marks1 + s[i].marks2 + s[i].marks3;
        float average = total / 3;
        printf("\nStudent %d\n", i + 1);
        printf("Roll Number: %d\n", s[i].roll_no);
        printf("Name: %s", s[i].name);
        printf("Total Marks: %.2f\n", total);
        printf("Average Marks: %.2f\n", average);
    }
   return 0;
}
