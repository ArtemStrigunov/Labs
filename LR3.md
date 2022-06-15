## Лабораторная работа №3

### Содержание

1. Задание
2. Блок-схема
3. Текст программы
4. Описание работы программы

### 1. Задание

Создать программу, которая бы брала данные из заранее записанного файла, например, input.txt (в моём случае File.txt) , в виде a,b,c и обрабатывала их, как модуль вектора с такими координатами. 
### Блок схема
![схема](https://github.com/ArtemStrigunov/Labs/blob/main/%D1%81%D1%85%D0%B5%D0%BC%D0%B0%203.png)

### 3.Текст программы 
```c++
#include <iostream>
#include <fstream>
#include <cmath>
using namespace std;
int main()
{
	setlocale(LC_ALL, "Russian");
	double a = 0, b = 0, c = 0, d = 0;
	ifstream ifs;
	ofstream ofs;

	ifs.open("FileS.txt");

	if (!ifs.is_open()) 
	{
		cout << "you're a loser" << endl;
	}

	else
	{
		ifs >> a >> b >> c;
	}

	d = sqrt((a * a) + (b * b) + (c * c));

	ofs.open("lr.txt");

	if (!ofs.is_open())
	{
		cout << "you're a loser" << endl;
	}
	else
	{
		ofs << "d=" << d;
	}

	ofs.close();


	system("pause");
	return 0;
}
	


### 4. Описание работы программы

Программа была написана  в компиляторе Microsoft Visual Studio. Сначала мы создаём файл в коренной папке(вводим название файла и разрешение) туда записываем три цифры(координаты вектора). Затем в программе мы открываем файл уже с готовыми числами, присваиваим им имена переменных и считаем модуль вектора, закрываем файл, открываем другой файл и туда записываем модуль вектора и закрываем. 
![image](https://github.com/ArtemStrigunov/Labs/blob/main/%D1%80%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82%203.png)
