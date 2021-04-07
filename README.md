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
			return false;
	   }
		else {
			int element = arr[top];
			top--;
			cout << "the element is poped" << endl;
			return true;
		}

	}
	int getMin() {
		int temp = arr[0];
   for(int i=0; i<5; i++) {
      if(temp>arr[i]) {
         temp=arr[i];
      }
   }
      cout<<temp;
   return temp;
	}


};
int main() {
	stack stack;
	stack.push(5);
	stack.push(2);
	stack.push(1);
	stack.push(4);
	stack.push(6);
    stack.pop();
    stack.getMin();

}
