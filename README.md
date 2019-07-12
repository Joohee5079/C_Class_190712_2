# C_Class_190712_2
계좌번호값 입력


#include <stdio.h>
void main()
{
	unsigned int m, s = 0, n, x = 100000000, d;
	printf("계좌번호를 입력하세요.\n>> ");
	scanf_s("%d", &d);
	do
	{
		m = d / x;
		n = d % x;
		s += m;
		d = n;
		x = x / 10;
	} while ( != 0);

	n = s % 10;
	printf("%d", n);
}
