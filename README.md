# LabaOP_5_6
Лабораторная работа по Основам Программирования номер 5 и 6

Лаба номер 5:

#include <stdio.h>


int main() 
{
	// Пункт 1
	int a[9] = { 88, 112, 6467, 325, 878, 3, 77, 8, 99 };

	for (int i = 0; i < 9; i++) {
		printf("%d ", a[i]);
	}
	printf("\n");


	// Пункт 2
	int matriza1[2][2] = { {2 ,5}, {2, 2} };
	int matriza2[2][2] = { {1 ,2}, {0, 1} };

	int answer[2][2];

	answer[0][0] = matriza1[0][0] * matriza2[0][0] + matriza1[0][1] * matriza2[1][0];
	answer[0][1] = matriza1[0][0] * matriza2[0][1] + matriza1[0][1] * matriza2[1][1];
	answer[1][0] = matriza1[1][0] * matriza2[0][0] + matriza1[1][1] * matriza2[1][0];
	answer[1][1] = matriza1[1][0] * matriza2[0][1] + matriza1[1][1] * matriza2[1][1];

	for (int i = 0; i < 2; i++) {
		for (int j = 0; j < 2; j++) {
			printf("%d ", answer[i][j]);
		}
		printf("\n");

	}
	return 0;

}




Лаба номер 6:

#include <stdio.h>
#include <stdlib.h>

int main() 
{
	double array[4] = { -8.8, 11.2, 64.67, 55.32 };
	

	for (double * ykaz = array; ykaz < &array[4]; ykaz++) {

		printf("%0.2lf ", *(ykaz));

	}
	
	printf("\n");

	double* massiv; //указатель для блока памяти

	massiv = (double*) malloc(4 * sizeof(double)); //выделяем память под 4 элемента типа дабл (каждый по 8 байт)

	for (int i = 0; i < 4; i++) {

		printf("massiv[%d]: ", i);

		scanf_s("%lf", &massiv[i]); //заполняем массив с клавиатуры

	}

	for (int i = 0; i < 4; i++) {

		printf("%0.2lf ", massiv[i]); //выводим массив на экран 


	}
	free(massiv); // освобождаем динамическу память у нашего массива
	return 0;
}
