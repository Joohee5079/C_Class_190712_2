# C_Class_190712_2
계좌번호값 입력


#include <stdio.h>
void main()
{
	unsigned int m, s = 0, n, n2, x = 100000000, d;
	printf("계좌번호를 입력하세요.\n>> ");
	scanf_s("%d", &d);
	do
	{
		m = d / x;
		n = d % x;
		s += m;
		d = n;
		x = x / 10;
	} while (x != 0);

	n2 = s % 10;
	printf("%d", n2);
}
