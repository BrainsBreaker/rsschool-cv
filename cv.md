# Oleg Kachurin
****
*e-mail*: kopspb@gmail.com

*discord*: BrainsBreaker(@BrainsBreaker)
****
Hi, I am starting to learn programming frontend basics
****
I have a bit experience in C and C++
****
Traning in C++:
```
#include <iostream>
using namespace std;
int Count = 0;
class Tree {
public:
	int n;
	Tree* Right;
	Tree* Left;
};
Tree* MakeTree(Tree* Head, int size)
{
	Tree* L, * R;
	L = new(Tree);
	R = new(Tree);
	Head->n = Count++;
	if (size > 1)
	{
		Head->Left=MakeTree(L, size - 1);
		Head->Right=MakeTree(R, size - 1);
	}
	else {
		Head->Left = Head->Right = NULL;
	}
	return Head;
}
int WriteTree(Tree* Head)
{
	cout << Head->n << endl;
	if (Head->Left != NULL)
		WriteTree(Head->Left);
	if (Head->Right != NULL)
		WriteTree(Head->Right);
	return 0;
}
int DellAll(Tree* Head)
{
	if (Head->Left != NULL)
		DellAll(Head->Left);
	if (Head->Right != NULL)
		DellAll(Head->Right);
	free(Head);
	return 0;
}

int main()
{
	Tree* Head;
	int n = 4;
	Head = new(Tree);
	Head=MakeTree(Head, n);
	WriteTree(Head);
	DellAll(Head);
	return 0;
}
```
I have no working experience
****
I learned C at school. I learned basics in other languages by myself
****
I learned english at school. My english level is A2/B1. I need more practices