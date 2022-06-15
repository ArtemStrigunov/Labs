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
	double a, b, c, d;
	ifstream ifs;
	ofstream ofs;
	
	ofs.open("Text2.txt");
	if (!ifs.is_open())
	{
		cin >> a;
		cin >> b;
		cin >> c;
		ofs << a << " ";
		ofs << b << " ";
		ofs << c << " ";
		d = sqrt((a * a) + (b * b) + (c * c));
		ofs << d;

	}
	else
	{
		cout << "you're a loser" << endl;
	}
	ofs.close();
	ofs.open("lr.txt");
	if (!ifs.is_open())
	{
		ofs << "d=" << d;
		ofs.close();

	}
	else
	{
		cout << "you're a loser" << endl;
		
	}

	system("pause");
	return 0;
} 

	


### 4. Описание работы программы

Программа была написана  в компиляторе Microsoft Visual Studio. Сначала мы создаём файл в коренной папке(вводим название файла и разрешение), если он уже есть то новый файл создаваться не будет, далее мы открываем этот файл и вводим значения координаты вектора.После мы закрываем файл, и открываем его заново. Читаем файл и выводим на дисплей что там написанно. Затем мы считаем модуль вектора, выводим его на экран и закрываем файл.В целом, по моей логике файл должен всегда открываться, потому что я сам создаю файл, но всё равно проверяю, открыт файл или нет.
![image](https://github.com/ArtemStrigunov/Labs/blob/main/%D1%80%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82%203.png)
