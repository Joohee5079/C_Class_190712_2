# C_Class_190712_2
계좌번호값 입력


#include <stdio.h>
void main()
{
	unsigned int m, n, d, dd, s = 0, x = 100000000, newcode;
	printf("계좌번호를 입력하세요.\n>> ");
	scanf_s("%d", &d);
	dd = d;
	do
	{
		m = d / x;			// m 은 계좌번호 나누기 1억 = 몫의 값이다.
		n = d % x;			// n 은 계좌번호 나누기 1억 = 나누기 값이다.
		s += m;				// s는 초기값이 0이며 m(몫)의 값을 더해져 할당받은 값이다.
		d = n;				// n(나머지)값을 d에 할당한다.
		x /= 10;			// x = x / 10 > x를 10으로 나눈 몫의 값을 x에 다시 할당한다.
	} while (n != 0);		// do while 로 반복되어 돌아가며 n의 값이 0이 되면 빠져나온다.

	n = s % 10;				// n은 몫의 값들이 더해져 할당받아진 값들을 10으로 나눈 나머지 값
	newcode = dd * 10 + n;	//d의 최종값이 바뀌기 때문에 dd로 복사해주어야 한다.
	printf("oldcode = %d\n", dd);
	printf("newcode = %d\n", newcode);   //o.c 에서 n(나머지)값이 마지막 숫자로 더해진 채 n.c로 출력
}
