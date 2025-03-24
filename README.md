#include<iostream>
#include<string>
using namespace std;
class Shape
{
public:
	virtual float area() = 0;
	
};
class Circle: public Shape
{
	float radius;
	const float pi = 3.141;
public:
	Circle():radius(0.0){}
	Circle(float r) :radius(r) ,pi(3.141){}

	float area( )override
	{
		return pi * radius * radius;
	}
	void display()
	{
		cout << "Area of Circle:" << area() << endl;
	}

};
class Rectangle : public Shape
{
	float length, width;
public:
	 Rectangle():length(0.0),width(0.0){}
	 Rectangle(float l,float w) :length(l), width(w) {}

	 float area( )override
	 {
		 return length * width;
	 }
	 void display()
	 {
		 cout << "Area of Rectangle:" << area() << endl;
	 }

};

int main()
{
	Circle c1(2.4);
	c1.display();
	Rectangle R1(1.4, 2.4);
	R1.display();
	
	return 0;
}
