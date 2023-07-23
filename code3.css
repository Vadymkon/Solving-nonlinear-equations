#include <iostream>
#include <vector>
#include <iomanip> // std::setprecision
using namespace std;
vector <double> iterations, accuracy;
double a=-1, b=0; //границы
double ab = -0.75; //начальный икс в условиях где то между границ
double func(double x) {
double rez = exp(x) + exp(-3 * x) - 4; //розрахунок самой функции
return rez;
}
double func_2(double x) {
double rez = exp(x) - exp(-3 * x) * 3; //подсчёт похидной
return rez;
}
double func_3(double x) {
double rez = exp(x) + exp(-3 * x) * 9; //подсчёт второй похидной
return rez;
}
void NewTone()
{
double x0; //ща будем определять чё из границ - наша точка
отправления
if (
func_2(ab) < 0 && func_3(ab) < 0
|| //or
func_2(ab) > 0 && func_3(ab) > 0
)
{
x0 = b;
}
else if (
func_2(ab) > 0 && func_3(ab) < 0
|| //or
func_2(ab) < 0 && func_3(ab) > 0
)
{
x0 = a;
}
iterations.push_back(x0); //вектора для вывода
accuracy.push_back(0);
double x1; //доп.
for (int i = 0; i < 10; i++)
{
x1 = x0 - func(x0) / func_2(x0);
iterations.push_back(x1);
accuracy.push_back(x1 - x0);
x0 = x1;
}
for (int i = 0; i < iterations.size(); i++)
{
cout << i << setprecision(4) << " iteration \t" << iterations[i] << " - value\t"
<< "accuracy: " << accuracy[i] << endl;
}
}
int main()
{
NewTone();
}
