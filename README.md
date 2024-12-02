# Simple-Calculator
Calculator

#include <iostream>
#include <iomanip>

using namespace std;

int main() {

	double num1, num2, sum;

	char op;

	cout << "Shtyp nr 1: ";
	cin >> num1;

	cout << "Shtyp operatorin (+,-,*,/)";
	cin >> op;


	cout << "Shtyp nr 2: ";
	cin >> num2;

	switch (op) {

	case '+':
		sum = num1 + num2;
		break;

	case '-':
		sum = num1 - num2;
		break;
		
	case '*':
		sum = num1 * num2;
		break;

	case '/':
		if (num2 != 0){ 
			sum = num1 / num2;
		}
		else {
			cout << "Error: Division by zero is not allowed." << endl;

			return 1;
		}
		break;
	default:
		cout << "Error invalid operator!! ";

		return 1;
	}

	cout << "The result is: " << sum << endl;

	return 0;
}
