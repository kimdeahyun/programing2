# programing2
report
// 1. 명령창에서 계산기를 구현하시오. 매개변수가 
// 모자라면 프로그램을 종료하시오.
#include<stdio.h>

#include<stdlib.h>

int main(int n, char* v[]) {

 int a, b, c;
 
 if (n < 4){
 
  printf("매개변수가 모자라요.\n");
  
  exit(0);
  
 }
 
 a = atoi(v[1]);
 
 b = atoi(v[3]);
 
 switch (v[2][0]) {
 
  case '+': c = a + b; break;
  
  case '-': c = a - b; break;
  
  default: break;
  
 }
 
 printf("%d\n", c);
 
}


//2. my.txt 에 첫줄에 33 다음 줄에 22들어 있다. 

// 이를 읽고 add() 함수를 이용하여

// 더하고 결과를 출력하시오
// 반드시 오류에 대해 처리를 포함하시오.
#include<stdio.h>

#include<stdlib.h>

int add(int a, int b) {

 return a + b;
 
}

int main() {

 int a, b;
 
 FILE* fp = fopen("my.txt", "r");
 
 if (fp == NULL) { 
 
  puts("File not found!!");
  
  exit(0); 
  
 }
 
 fscanf(fp, "%d%d", &a, &b);
 
 fclose(fp);
 
 printf("%d\n", add(a, b));
 
}


// 3.하드디스크에서 읽고 더하시오

#include<stdio.h>

int add(int a, int b) {

	return(a + b);
}

int main() {

	int a, b, c;
	
	FILE* fp;
	
	fp = fopen("my1.txt", "r");
	
	fscanf(fp, "%d%d", &a, &b);
	
	fclose(fp); //필수적으로 넣어야 하는 문장
	
	c = add(a, b);//a + b;
	
	printf("%d\n", c);
	
}




// 4. 두명의 구조체 정보를 배열에 초기화하고
// 포인터로 화면에 출력하시오.
#include<stdio.h>

struct user {

 int a;
 
 char n[80];
 
} we[2] = { { 18,"jcshim" },{ 16,"jskim" } };

int main() {

 struct user* p;
 
 p = we;
 
 printf("%d %s\n", p->a, p->n);
 
 p++;
 
 printf("%d %s\n", p->a, p->n);
 
}

