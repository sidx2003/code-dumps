# code-dumps
dumping all the trash i have done
#include <stdio.h>
char stack[50];
int top=-1;
void push(char ptr){
  top++;
  stack[top]=ptr;
}
void pop(){
  top--;
}
int main(void) {
char s[100];
  printf("enter the equation \n");
  scanf("%s",s);
  printf("%s\n",s);
  for(int i=0;s[i]!='\0';i++){
    if(s[i]=='('||s[i]=='['||s[i]=='{'){
      push(s[i]);
    }
    else if(s[i]==')'||s[i]==']'||s[i]=='}'){
      pop();
    }
  }
  if(top==-1){
    printf("valid input!!!");
  }
  else{
    printf("invalid output bitch");
  }
  return 0;
}
