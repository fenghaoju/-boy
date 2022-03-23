#include<stdio.h>
#include<string.h>
int main()
{
	printf("您可以输入一句英语，将为你统计其出现的次数\n");
	char f[1000];
	gets(f);
	printf("请您输入一个单词，出现的个数将可查\n");
	char w[10];
	gets(w);
	strlwr(f);
	strlwr(w);
	int wlen=strlen(w);
	int slen=strlen(f);
	int cnt=0;
	for(int i=0;i<=slen-wlen;i++)
	{
		char tempw[wlen+1];
		tempw[wlen]='\0';
		for(int j=0;j<wlen;j++) tempw[j]=f[i+j];
		if(strcmp(tempw,w)==0) cnt++;
		 
	}
	printf("%d",cnt);
	return 0;
}
