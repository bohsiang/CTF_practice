 
# OverFlow 0 - Points: 100

### This should be easy. Overflow the correct buffer in this program and get a flag. Its also found in /problems/overflow-0_3_dc6e55b8358f1c82f03ddd018a5549e0 on the shell server. Source.

## vuln.c file
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <signal.h>

#define FLAGSIZE_MAX 64

char flag[FLAGSIZE_MAX];

// sigsegv_handler會幫我們把Flag印出來
void sigsegv_handler(int sig) {
  fprintf(stderr, "%s\n", flag);
  fflush(stderr);
  exit(1);
}

void vuln(char *input){
  char buf[128];    // 這裡代表程式開了128個給輸入作為buffer
  strcpy(buf, input);
}

int main(int argc, char **argv){

  FILE *f = fopen("flag.txt","r");
  if (f == NULL) {
    printf("Flag File is Missing. Problem is Misconfigured, please contact an Admin if you are running this on the shell server.\n");
    exit(0);
  }
  fgets(flag,FLAGSIZE_MAX,f);
  signal(SIGSEGV, sigsegv_handler); // 如果造成segmentation fault就會印出flag

  gid_t gid = getegid();
  setresgid(gid, gid, gid);

  if (argc > 1) {
    vuln(argv[1]);  // 當輸入>128這裡成立後就會觸發segmentation fault
    printf("You entered: %s", argv[1]);
  }
  else
    printf("Please enter an argument next time\n");
  return 0;
}
```
這題主要的重點如上面所示

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%200_1.PNG)

基本上只要把程式搞到OverFlow就會自己吐flag出來了

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%200_2.PNG)

















