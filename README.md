# Projeto-em-C
Esse é um código básico feito na linguagem de Programação C que permite o gerenciamento de Cadastros de alunos de  Escolas/ou Faculdades.




#include <stdio.h>
int main(){
    int idade, Matricula;
    float altura;
    char nome[50];

//codigo que vai permitir a entrada e saida de dados(informações) do usuario e adicionarinformações.

    printf("Digite sua idade: \n");
    scanf("%d", &idade);

    printf("Digite a sua altura: \n");
    scanf("%f", &altura);

    printf("Digite o seu nome: \n");
    scanf("%s", &nome);

    printf("Digite a sua matricula: \n");
    scanf("%d", &Matricula);

//como será lido as informações do usuario,ou seja: Com Expecificadores de formato(o visual).

    printf("Nome do aluno: %s - Matricula: %d\n", nome, Matricula);
    printf("idade: %d - altura: %f", idade, altura);

    return 0;
}
