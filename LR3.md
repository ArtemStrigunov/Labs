#include <iostream>
#include <fstream>//fstream-запись и чтение, ifstream and ofstream- чтение и запись
#include <cmath>
#include <string>
using namespace std;

int main()
{
	setlocale(LC_ALL, "Russian");
	int a, b, c;
	double d = 0;
	string A;
	ifstream fout;
	ofstream llout;
	fout.open("D:/проги с++/ConsoleApplication1/input.txt");

	if (!(fout.is_open()))
	{	
		cout << "Файл не открыт" << endl;
	}
	else
	{
		cout << "Программа начинает свою работу..." << endl;
		fout >> a >> b >> c;
		fout.close();
		cout << "Даны следующие координаты вектора:" << " x = " << a << "; y = " << b << "; z = " << c << ";" << endl;	
		d = sqrt((a*a) + (b*b) + (c*c));
		cout << "Модуль вектора равен: " << d << endl;
		llout.open("D:/проги с++/ConsoleApplication1/output.txt");
		if (!(llout.is_open()))
		{
			cout << "Файл не найден" << endl;
		}
		else
			cout << "Программа загружает в файл output значение модуля вектора(d)" << endl;
			llout << "Значние модуля d =" << d;
			llout.close();
	}
	system (" pause ");
	return (0);
}
