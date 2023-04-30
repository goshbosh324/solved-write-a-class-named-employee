Download Link: https://assignmentchef.com/product/solved-write-a-class-named-employee
<br>
Write a class named Employee that has the following member variables:

<ul>

 <li>name. a string that holds the employee’s name.</li>

 <li>idNumber. an int variable that holds the emlpoyee’s ID number.</li>

 <li>department. a string that holds the name of the department where the employee works.</li>

 <li>position. a string that holds the employee’s job title</li>

</ul>

The class should have the following constructors:

<ul>

 <li>A constructor that accepts the following values as arguments and assigns them to the appropriate member variables: employee’s name, employee’s ID number, department, and position.</li>

 <li>A constructor that accepts the following values as arguments and assigns them to the appropriate member variables: employee’s name and ID number. The department and position fields should be assigned an empty string (“”).</li>

 <li>A default constructor that assigns empty strings (“”) to the name, department, and position member variables, and 0 to the idNumber member variable.</li>

</ul>

Write appropriate mutator functions that store values in these member variables and accessor functions that return the values in these member values. Once you have written the class, write a separate program that creates three Employee objects to hold the following data.

Name ID Number Department Position

Susan Meyers 47899 Accounting Vice President

Mark Jones 39119 IT Programmer

Joy Rogers 81774 Manufacturing Engineer

The program should store this data in three objects and then display the data for each employee on the screen.

<strong>I have included my codes in text below:</strong>

<strong>Main</strong>

#include “stdafx.h”

#include “employee.h”

#include

#include

#include

using namespace std;

int main()

{

//create 1st object for empployee class

Employee worker1;

worker1.setNameOfEmployee(“Susan Meyers”);

worker1.setIdNumberOfEmployee(47899);

worker1.setDepartmentOfEmployee(“Accounting”);

worker1.setPositionOfEmployee(“Vice President”);

//create 2nd object for employee class

Employee worker2;

worker2.setNameOfEmployee(“Mark Jones”);

worker2.setIdNumberOfEmployee(39119);

worker2.setDepartmentOfEmployee(“IT”);

worker2.setPositionOfEmployee(“Programmer”);

//create 3rd object for employee class

Employee worker3;

worker3.setNameOfEmployee(“Joy Rogers”);

worker3.setIdNumberOfEmployee(81774);

worker3.setDepartmentOfEmployee(“Maufacturing”);

worker3.setPositionOfEmployee(“Engineer”);

//display details of three employees

cout &lt;&lt; “————————————–” &lt;&lt; endl;

cout &lt;&lt; left &lt;&lt; setw(15) &lt;&lt; “Name”

&lt;&lt; setw(12) &lt;&lt; “ID Number”

&lt;&lt; setw(15) &lt;&lt; “Department”

&lt;&lt; setw(15) &lt;&lt; “Position” &lt;&lt; endl;

cout &lt;&lt; “————————————–” &lt;&lt; endl;

cout &lt;&lt; setw(15) &lt;&lt; worker1.getNameOfEmployee()

&lt;&lt; setw(12) &lt;&lt; worker1.getNumberOfEmployee()

&lt;&lt; setw(15) &lt;&lt; worker1.getDepartmentOfEmployee()

&lt;&lt; setw(15) &lt;&lt; worker1.getPositionOfEmployee() &lt;&lt; endl;

cout &lt;&lt; setw(15) &lt;&lt; worker2.getNameOfEmployee()

&lt;&lt; setw(12) &lt;&lt; worker2.getNumberOfEmployee()

&lt;&lt; setw(15) &lt;&lt; worker2.getDepartmentOfEmployee()

&lt;&lt; setw(15) &lt;&lt; worker2.getPositionOfEmployee() &lt;&lt; endl;

cout &lt;&lt; setw(15) &lt;&lt; worker3.getNameOfEmployee()

&lt;&lt; setw(12) &lt;&lt; worker3.getNumberOfEmployee()

&lt;&lt; setw(15) &lt;&lt; worker3.getDepartmentOfEmployee()

&lt;&lt; setw(15) &lt;&lt; worker3.getPositionOfEmployee() &lt;&lt; endl;

cout &lt;&lt; “————————————–” &lt;&lt; endl;

system(“pause”);

return 0;

}

<strong>Employee.h</strong>

//Empployee class declaration

//Employee.h

#pragma once

#ifndef EMPLOYEE_H

#define EMPLOYEE_H

#include

using namespace std;

class Employee

{

private:

//declaration of member variables to store the data of an employee

string name;

int idNumber;

string department;

string position;

public:

//declaration of constructors to initialize the member variables with appropriate values

Employee(string, int, string, string);

Employee(string, int);

Employee();

//declaration of mutator function to store the specified values in the member variables

void setNameOfEmployee(string);

void setIdNumberOfEmployee(int);

void setDepartmentOfEmployee(string);

void setPositionOfEmployee(string);

//declaration of accessor functions to return the current values in the member variables

string getNameOfEmployee() const;

int getIdNumberOfEmployee() const;

string getDepartmentOfEmployee() const;

string getPositionOfEmployee() const;

};

#endif

<strong>Employee.cpp</strong>

//Employee class implementation

//Employee.cpp

#include “Employee.h”

#include

using namespace std;

//constructor with four arguments

Employee::Employee(string newNameOfEmployee, int newIdNumberOfEmployee,

string newDepartmentOfEmployee, string newPositionOfEmployee)

{

name = newNameOfEmployee;

idNumber = newIdNumberOfEmployee;

department = “”;

position = “”;

}

//constructor with no arguments

Employee::Employee()

{

name = “”;

idNumber = 0;

department = “”;

position = “”;

}

//setNameOfEmployee implementation

void Employee::setNameOfEmployee(string newNameOfEmployee)

{

name = newNameOfEmployee;

}

//setIdNumberOfEmployee implementation

void Employee::setIdNumberOfEmployee(int newIdNumberOfEmployee)

{

idNumber = newIdNumberOfEmployee;

}

//setDepartmentOfEmployee implementation

void Employee::setDepartmentOfEmployee(string newDeparmentOfEmployee)

{

department = newDepartmentOfEmployee;

}

//setPositionOfEmployee implementation

void Employee::setPositionOfEmployee(string newPositionOfEmployee)

{

position = newPositionOfEmployee;

}

//getNameOfEmployee implementation

string Employee::getNameOfEmployee() const

{

return name;

}

//getIdNumberOfEmployee implementation

int Employee::getIdNumberOfEmployee() const

{

return idNumber;

}

//getDepartmentOfEmployee implementation

string Employee::getDepartmentOfEmployee() const

{

return department;

}

//getPositionOfEmployee

string Employee::getPositionOfEmpoyee() const

{

return position;

}