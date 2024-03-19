#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct {
    int mat, idade;
    char nome[40];
    float nota, renda;
} aluno;

int main(void) {
    aluno ed[5];
    int maioridade = 0;

    printf("\nTurma de Estrutura de Dados:");
    for (int i = 0; i < 5; i++) {
        printf("\nDigite o ID do %do cliente: ", i + 1);
        scanf("%d", &ed[i].mat);
        printf("\nDigite a IDADE do %do cliente: ", i + 1);
        scanf("%d", &ed[i].idade);
        printf("\nDigite a RENDA do %do cliente: ", i + 1);
        scanf("%f", &ed[i].renda);
        printf("\nDigite o nome do %do cliente: ", i + 1);
        getchar(); 
        gets(ed[i].nome);

        if (ed[i].idade >= 18) {
            maioridade++;
        }
    }
    printf("\nQuantidade de clientes com idade maior ou igual a 18 anos: %d\n", maioridade);

    system("pause");
    
