import java.util.Scanner;

public class CGPACalculator {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int subjects;
        double totalCredits = 0;
        double totalGradePoints = 0;

        System.out.println("===== CGPA CALCULATOR =====");

        System.out.print("Enter number of subjects: ");
        subjects = sc.nextInt();

        double[] grades = new double[subjects];
        double[] credits = new double[subjects];

        for (int i = 0; i < subjects; i++) {

            System.out.print("Enter grade point for Subject " + (i + 1) + ": ");
            grades[i] = sc.nextDouble();

            System.out.print("Enter credit for Subject " + (i + 1) + ": ");
            credits[i] = sc.nextDouble();

            totalGradePoints = totalGradePoints + (grades[i] * credits[i]);
            totalCredits = totalCredits + credits[i];
        }

        double cgpa = totalGradePoints / totalCredits;

        System.out.println("\n===== RESULT =====");
        System.out.println("Final CGPA = " + cgpa);

        sc.close();
    }
}
