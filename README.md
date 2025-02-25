#include <stdio.h>
#include <stdlib.h>

int main() {
    int n;
    int *arr;

    printf("Ingrese el numero de elementos: ");
    scanf("%d", &n);

    arr = (int*) malloc(n * sizeof(int));

    if (arr == NULL) {
        printf("Error en la asignacion de memoria.\n");
        return 1;
    }

    for (int i = 0; i < n; i++) {
        arr[i] = i + 1;
    }

    printf("Los elementos del array son: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");


    free(arr);

    return 0;
}
