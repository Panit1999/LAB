#include <iostream>
#include <string>
#include<iomanip>
using namespace std;
void Menu();
float Area(const float R); //วงกลม
int Area(const int w,int l,int h); //ปริมาตร
float Area(const float L,const float W); //สี่เหลี่ยม
double Area(const double based1,double based2, double h);

int main(){
	char C;
	bool Flag=true;
	do{
		Menu();
		cin >> C;
		if(C=='1'){
			float R;
			cout << "Enter Radius :: " <<endl;
			cin >> R;
			cout << "Area of Circle = "<< fixed <<endl;
			cout << setprecision(2) << Area(R)<< endl;
		}
		else if(C=='2'){
			float L,W;
			cout << "Enter Length & Width :: " <<endl;
			cin >> L>>W;
			cout << "Area of Rectangle = "<< fixed <<endl;
			cout << setprecision(2) << Area(L,W)<< endl;
		
		}
		else if(C=='3'){
			float w,l,h;
			cout << "Enter Width & Length &  Height :: " <<endl;
			cin >> w>>l>>h;
			cout << "Area of Trapezium = "<< fixed <<endl;
			cout << setprecision(2) << Area(w,l,h)<< endl;
		
		}
		else if(C=='4'){
			float l,h;
			cout << "Enter Length &  sum :: " <<endl;
			cin >>l>>h;
			cout << "Area of Capacity = "<< fixed <<endl;
			cout << setprecision(2) << Area(l,h)<< endl;
		
		}
	}while (Flag);
	cout << "Exit Program"<< endl;
	return 0;
}
float Area(const float R) //วงกลม
{
	return (3.14159F*R*R);
}
float Area(const float L,const float W) //สี่เหลี่ยม
{
	return(L*W);
}
int Area(const int w,int l,int h)//ปริมาตร
{
	return(w*l*h);
}
double Area(const double based1,double based2, double h) //คางหมู
{
	return(0.5*h*(based1+based2));
}
void Menu()
{	
	cout << "Program Calculate Area"<<endl;
	cout << "1.Circle"<<endl;
	cout << "2.Rectangle"<<endl;
	cout << "3.Trapezium"<<endl;
	cout << "4.Capacity"<<endl;
	cout << "5.Exit"<<endl;
}
