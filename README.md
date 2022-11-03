#include <iostream>
using namespace std;

int main()
{
	float item_price,
		amount_paid,
		change;

	int dollars_return,
		quarters_return,
		dimes_return,
		nickels_return,
		pennies_return;

	const float QUARTER_VALUE = 0.25,
				DIME_VALUE = 0.10,
				NICKEL_VALUE = 0.05,
				PENNY_VALUE = 0.01;

	cout << "How much does the iteam cost? ";
	cin >> item_price;

	cout << "How much you paid for it? ";
	cin >> amount_paid;

	change = amount_paid - item_price;
	cout << "The total change is: " << change << endl;

	//int cuts off the decimals so it left with dollars
	dollars_return = amount_paid - item_price;
	cout << "The total dollars to return is: " << dollars_return << endl;

	//update change to reflect dollars that have been handed back
	change = change - dollars_return;

	quarters_return = change / QUARTER_VALUE;
	cout << "The total quarters to return is: " << quarters_return << endl;

	//update change to reflect quarters that have been handed back
	change = change - (quarters_return * QUARTER_VALUE);

	dimes_return = change / DIME_VALUE;
	cout << "The total dimes to return is: " << dimes_return << endl;

	//update change to reflect dimes that have been handed back
	change = change - (dimes_return * DIME_VALUE);

	nickels_return = change / NICKEL_VALUE;
	cout << "The total nickels to return is: " << nickels_return << endl;

	//update change to reflect nickels that have been handed back
	change = change - (nickels_return * NICKEL_VALUE);

	pennies_return = change / PENNY_VALUE;
	cout << "The total pennies to return is: " << pennies_return << endl;


	system("pause");
	return 0;
}
