# Classes-C-

1. Includes and Constants



const double PI {3.1415926535897932384626433832795};

This allows us to use input/output functions like std::cout for printing to the console.

#include <iostream>: 
    
PI: A constant value for π (pi), used to calculate the volume of the cylinder.

2. The Cylinder Class

The Cylinder class models a geometric cylinder and provides methods to calculate its volume and modify its dimensions.

a. Public Members

public:

    Cylinder() = default;
    
    Cylinder(double rad_param, double height_param) {
    
        base_radius = rad_param;
        
        height = height_param;
        
    }

    Creates a cylinder object with default values for base_radius and height (set to 1 in the private section).
    
    Default Constructor: Cylinder() = default; 

    Initializes the cylinder with specific values for base_radius and height.
    
    Parameterized Constructor: Cylinder(double rad_param, double height_param) 

Purpose: Calculates and returns the volume of the cylinder using the formula:

b. Volume Calculation

double volume() {

    return PI * base_radius * base_radius * height;
}


c. Setter and Getter Methods

    Getters:

double get_base_radius() {

    return base_radius;
    
}

double get_height() {

    return height;
    
}

These allow retrieval of the base_radius and height values.

    Setters:

void set_base_radius(double rad_param) {

    base_radius = rad_param;
    
}

void set_height(double height_param) {

    height = height_param;
    
}

These allow modification of the base_radius and height.

d. Private Members

private:

base_radius and height: Represent the cylinder's radius and height, respectively.

Default Values: Both are initialized to 1.

double base_radius{1};
    
double height{1};


3. Main Function

The main function demonstrates the functionality of the Cylinder class.

a. Create a Cylinder Object

Cylinder cylinder1(10,10);

std::cout << "volume : " << cylinder1.volume() << std::endl;

A Cylinder object (cylinder1) is created with a radius of 10 and a height of 10.
    
The volume() method calculates and prints the volume:

b. Modify the Cylinder

cylinder1.set_base_radius(100);

cylinder1.set_height(10);

std::cout << "volume : " << cylinder1.volume() << std::endl;

Setters modify the base_radius to 100 and the height to 10.

4. Key Features Demonstrated

Encapsulation:
   
Member variables (base_radius and height) are private.
   
Getters and setters allow controlled access and modification.
   
Constructors:
   
A default constructor (= default) provides initial values.
   
A parameterized constructor allows custom initialization.
   
Object-Oriented Programming:
   
Methods (volume, get_, set_) and data are encapsulated within the Cylinder class.

6. Output

volume : 3141.59

volume : 314159.27

The first line is the initial volume of the cylinder (radius = 10, height = 10).
    
The second line is the updated volume after modifying the radius to 100 and height to 10.

