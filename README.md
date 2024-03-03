#include<iostream>

using namespace std;

int main()
{
	int a, b, c, MAX;
	cout << "Enter 2 numbers: ";
	cin >> a >> b;

	/*if (a > b)
	{
		swap(a, b);
	}*/
	_asm
	{
	ifu:
		mov eax, a 
			cmp eax, b 
			jl endifu

			mov ecx, b
			mov b, eax
			mov a, ecx

			endifu :


	}
	cout << a << " " << b << endl;

	cout << "Enter 3rd number: ";
	cin >> c;

	_asm
	{
	ifu1:
		mov eax, a
			cmp eax, c
			jl endifu1

			mov ecx, c
			mov c, eax
			mov a, ecx

			endifu1 :

	ifu2:
		mov eax, b
			cmp eax, c
			jl endifu2

			mov ecx, c
			mov c, eax
			mov b, ecx

			endifu2 :

	}

	

	cout << a << " " << b << " " << c << endl;

	



	system("pause");
}
