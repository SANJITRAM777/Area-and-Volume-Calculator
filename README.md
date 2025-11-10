# Area-and-Volume-Calculator
This C++ program is a menu-driven calculator that computes the area and volume of basic shapes like circles, rectangles, triangles, cylinders, cones, and spheres. It uses functions and the &lt;cmath> library for calculations, offering a simple and modular design ideal for beginners learning C++ basics. #
#include <iostream>
#include <cmath>     
using namespace std;
void areaMenu();
void volumeMenu();

void areaOfCircle();
void areaOfRectangle();
void areaOfTriangle();
void volumeOfCylinder();
void volumeOfCone();
void volumeOfSphere();

int main() {
    int choice;

    do {
        cout << "\n==== AREA AND VOLUME CALCULATOR ====\n";
        cout << "1. Calculate Area\n";
        cout << "2. Calculate Volume\n";
        cout << "3. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice) {
            case 1: areaMenu(); break;
            case 2: volumeMenu(); break;
            case 3: cout << "Exiting program...\n"; break;
            default: cout << "Invalid choice! Please try again.\n";
        }
    } while (choice != 3);

    return 0;
}

void areaMenu() {
    int ch;
    cout << "\n--- AREA MENU ---\n";
    cout << "1. Circle\n";
    cout << "2. Rectangle\n";
    cout << "3. Triangle\n";
    cout << "Enter your choice: ";
    cin >> ch;

    switch (ch) {
        case 1: areaOfCircle(); break;
        case 2: areaOfRectangle(); break;
        case 3: areaOfTriangle(); break;
        default: cout << "Invalid option!\n";
    }
}

void areaOfCircle() {
    double r;
    cout << "Enter radius of circle: ";
    cin >> r;
    double area = M_PI * r * r;
    cout << "Area of Circle = " << area << endl;
}

void areaOfRectangle() {
    double l, b;
    cout << "Enter length and breadth: ";
    cin >> l >> b;
    double area = l * b;
    cout << "Area of Rectangle = " << area << endl;
}

void areaOfTriangle() {
    double b, h;
    cout << "Enter base and height: ";
    cin >> b >> h;
    double area = 0.5 * b * h;
    cout << "Area of Triangle = " << area << endl;
}
void volumeMenu() {
    int ch;
    cout << "\n--- VOLUME MENU ---\n";
    cout << "1. Cylinder\n";
    cout << "2. Cone\n";
    cout << "3. Sphere\n";
    cout << "Enter your choice: ";
    cin >> ch;

    switch (ch) {
        case 1: volumeOfCylinder(); break;
        case 2: volumeOfCone(); break;
        case 3: volumeOfSphere(); break;
        default: cout << "Invalid option!\n";
    }
}

void volumeOfCylinder() {
    double r, h;
    cout << "Enter radius and height: ";
    cin >> r >> h;
    double volume = M_PI * r * r * h;
    cout << "Volume of Cylinder = " << volume << endl;
}

void volumeOfCone() {
    double r, h;
    cout << "Enter radius and height: ";
    cin >> r >> h;
    double volume = (M_PI * r * r * h) / 3;
    cout << "Volume of Cone = " << volume << endl;
}

void volumeOfSphere() {
    double r;
    cout << "Enter radius: ";
    cin >> r;
    double volume = (4.0 / 3.0) * M_PI * pow(r, 3);
    cout << "Volume of Sphere = " << volume << endl;
}
