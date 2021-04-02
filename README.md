# data-struc
#include<iostream>
using namespace std;
#define cap 5
class stack {
	int size = 5;
	int top = -1;
	int arr[cap];
	
public:
	bool push(int val) {
		if (top>=cap) {
			cout << "stack is full " << endl;
			return false;
		}
		else {
			top++;
			arr[top] = val;
			return true;
		}
	}
	int pop() {

		if (top < 0) {
			cout << "stack is empty" << endl;
			return 0;
	   }
		else {
			int element = arr[top];
			top--;
			cout << "the element is poped" << endl;
			return 1;
		}

	}
	int getMin() {
		int smallest = arr[0];
		for (int i = 0;i < 5;i++) {
			arr[i] = smallest;
		}
		cout << smallest << endl;
	}


};
int main() {
	stack stack;
	stack.push(1);
	stack.push(2);
	stack.push(3);
	stack.push(4);
	stack.push(5);
  stack.pop();
  stack.getMin();

}
