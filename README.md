#include <stdio.h>

// Define a structure to hold student details
struct Student {
    char name[50];
    int rollNumber;
    float marks;
};

int main() {
    int n, i;

    // Ask the user for the number of students
    printf("Enter the number of students: ");
    scanf("%d", &n);

    // Declare an array of structures
    struct Student s[n];

    // Read details for each student
    for (i = 0; i < n; i++) {
        printf("\nEnter details for Student %d:\n", i + 1);
        
        printf("Enter name: ");
        scanf("%s", s[i].name); // Note: use fgets() for full names with spaces

        printf("Enter roll number: ");
        scanf("%d", &s[i].rollNumber);

        printf("Enter marks: ");
        scanf("%f", &s[i].marks);
    }

    // Display details of all students
    printf("\n--- Stored Student Details ---\n");
    for (i = 0; i < n; i++) {
        printf("\nStudent %d:\n", i + 1);
        printf("Name: %s\n", s[i].name);
        printf("Roll Number: %d\n", s[i].rollNumber);
        printf("Marks: %.2f\n", s[i].marks);
    }

    return 0;
}
