#include <iostream>
#define MAX_STACK_SIZE 10
using namespace std;

struct Element {
int data, atas;
Element *next;
};

class MyStack {
	private:
		Element deret;
		Element *head = NULL;

	public:
		void max(){
		deret.atas = -1;
		}
		bool kosong(){
		if(deret.atas == -1){
			return 1;
		}else{
			return 0;
		}
			}

	bool penuh(){
		if(deret.atas == MAX_STACK_SIZE-1){
			return 1;
		} else{
			return 0;
		}
	}
	
	void push(int a){
		if (!penuh()){
			
			Element *drt = new Element;
			drt->data = a;
			drt->next = NULL;
			if(kosong()){
				head = drt;
				head->next = NULL;
			} else{
				drt->next = head;
				head = drt;
				
				}
				deret.atas++;
			}
		else {
			cout<<"\nStack Penuh!!\n"<<endl;
			}
		}
	Element pop(){
		Element item;
			if (kosong()){
				cout<<"\nStack Kosong\n";
			}
			else{
				Element *drt = new Element;
				drt = head;
				head = head->next;
				delete drt;
				deret.atas--;
			}
		return item;
		}
	void printStackList(){
		if (!kosong()){
				Element *drt = new Element;
				drt = head;
				cout<<"\nisi stack = ";
				while(drt!=NULL){
					cout<<drt->data<<" ";
					drt = drt->next;
					}
					cout<<"\n";
				}
				else {
					cout<<"Stack Kosong"<<endl;
				}
			}
	int getTop(){
		if(kosong()){
			cout<<"tumpukkan kosong\n";
		} else{
			cout<<"top = "<<head->data<<endl;
		}	
	}	
};

int main(){

	MyStack n;
	
	int x, y, z;
	do{

		cout<<"\nDaftar perintah:\n";
		cout<<"[1]. push\n"; 
		cout<<"[2]. pop\n";
		cout<<"[3]. get top\n";
		cout<<"masukkan pilihan: ";
		cin>>x;
		
		if(x == 1){
			cout<<"masukkan angka: ";
			cin>>y;
			n.push(y);
			}
			
		else if(x == 2){
			n.pop();	
			}
		else if(x == 3){
			n.getTop();	
			}
		else{
			cout<<"\n===pilihan tak ada, tolong ulangi===\n";
			}
			
		n.printStackList();
		
		cout<<"\n[1]. lakukan get top/push/pop lagi\n";
		cout<<"[2]. tidak\n";
		cout<<"masukkan pilihan: ";
		cin>>z;
	} while (z == 1);
		n.printStackList();
		cout<<"\n\nTERIMA KASIH\n";
	return 0;
}
