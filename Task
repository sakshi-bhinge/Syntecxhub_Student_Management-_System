import java.util.ArrayList;
import java.util.Scanner;

class Student {
    int id;
    String name;
    int age;
    String department;

    Student(int id, String name, int age, String department) {
        this.id = id;
        this.name = name;
        this.age = age;
        this.department = department;
    }
}

public class StudentManagement {

    static ArrayList<Student> studentList = new ArrayList<>();
    static Scanner input = new Scanner(System.in);

    public static void main(String[] args) {

        int option;

        do {
            System.out.println("\n---- Student Management System ----");
            System.out.println("1. Add Student");
            System.out.println("2. View Students");
            System.out.println("3. Update Student");
            System.out.println("4. Delete Student");
            System.out.println("5. Exit");
            System.out.print("Choose option: ");

            option = input.nextInt();

            switch (option) {
                case 1:
                    addStudent();
                    break;

                case 2:
                    displayStudents();
                    break;

                case 3:
                    updateStudent();
                    break;

                case 4:
                    deleteStudent();
                    break;

                case 5:
                    System.out.println("Program closed.");
                    break;

                default:
                    System.out.println("Invalid choice!");
            }
        } while (option != 5);
    }

    static void addStudent() {
        System.out.print("Enter ID: ");
        int id = input.nextInt();
        input.nextLine();

        System.out.print("Enter Name: ");
        String name = input.nextLine();

        System.out.print("Enter Age: ");
        int age = input.nextInt();
        input.nextLine();

        System.out.print("Enter Department: ");
        String dept = input.nextLine();

        studentList.add(new Student(id, name, age, dept));
        System.out.println("Student added successfully.");
    }

    static void displayStudents() {
        if (studentList.isEmpty()) {
            System.out.println("No student records available.");
            return;
        }

        System.out.println("\nID   Name           Age   Department");
        System.out.println("-------------------------------------");

        for (Student s : studentList) {
            System.out.println(
                s.id + "   " + s.name + "     " + s.age + "     " + s.department
            );
        }
    }

    static void updateStudent() {
        System.out.print("Enter student ID to update: ");
        int id = input.nextInt();
        input.nextLine();

        for (Student s : studentList) {
            if (s.id == id) {
                System.out.print("New Name: ");
                s.name = input.nextLine();

                System.out.print("New Age: ");
                s.age = input.nextInt();
                input.nextLine();

                System.out.print("New Department: ");
                s.department = input.nextLine();

                System.out.println("Student updated.");
                return;
            }
        }
        System.out.println("Student not found.");
    }

    static void deleteStudent() {
        System.out.print("Enter student ID to delete: ");
        int id = input.nextInt();

        for (int i = 0; i < studentList.size(); i++) {
            if (studentList.get(i).id == id) {
                studentList.remove(i);
                System.out.println("Student deleted.");
                return;
            }
        }
        System.out.println("Student not found.");
    }
}
