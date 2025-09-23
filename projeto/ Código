#include <stdio.h>
#include <stdlib.h>

int main() {
    // Declaração das variáveis para a carta 01
    char estado01;
    char codigo01[4];
    char nomeCidade01[50];
    unsigned long int populacao01;
    float area01;
    float pib01;
    int pontosTuristicos01;
    float densidade01;

    // Declaração das variáveis para a carta 02
    char estado02;
    char codigo02[4];
    char nomeCidade02[50];
    unsigned long int populacao02;
    float area02;
    float pib02;
    int pontosTuristicos02;
    float densidade02;

    // Leitura dos dados da carta 01
    printf("Insira os dados da carta 01:\n");
    printf("Estado A-H: ");
    scanf(" %c", &estado01);
    printf("Código da Carta: ");
    scanf("%3s", codigo01);
    printf("Nome da Cidade: ");
    scanf(" %[^\n]", nomeCidade01);
    printf("Número de habitantes: ");
    scanf("%lu", &populacao01);
    printf("Tamanho da Área (km²): ");
    scanf("%f", &area01);
    printf("PIB (bilhões de reais): ");
    scanf("%f", &pib01);
    printf("Número de pontos turísticos: ");
    scanf("%d", &pontosTuristicos01);

    densidade01 = (float)populacao01 / area01;

    // Leitura dos dados da carta 02
    printf("\nInsira os dados da carta 02:\n");
    printf("Estado A-H: ");
    scanf(" %c", &estado02);
    printf("Código da Carta: ");
    scanf("%3s", codigo02);
    printf("Nome da Cidade: ");
    scanf(" %[^\n]", nomeCidade02);
    printf("Número de habitantes: ");
    scanf("%lu", &populacao02);
    printf("Tamanho da Área (km²): ");
    scanf("%f", &area02);
    printf("PIB (bilhões de reais): ");
    scanf("%f", &pib02);
    printf("Número de pontos turísticos: ");
    scanf("%d", &pontosTuristicos02);

    densidade02 = (float)populacao02 / area02;

    int atributo1, atributo2;

    // --- Mudança 1: Escolha do primeiro atributo ---
    printf("\nEscolha o primeiro atributo para comparar:\n");
    printf("1. População\n");
    printf("2. Área\n");
    printf("3. PIB\n");
    printf("4. Número de pontos turísticos\n");
    printf("5. Densidade demográfica\n");
    printf("Opção: ");
    scanf("%d", &atributo1);

    // Validação simples do primeiro atributo
    if (atributo1 < 1 || atributo1 > 5) {
        printf("Opção inválida! Encerrando programa.\n");
        return 1;
    }

    // --- Mudança 2: Escolha do segundo atributo, excluindo o primeiro ---
    printf("\nEscolha o segundo atributo para comparar (diferente do primeiro):\n");
    switch (atributo1) {
        case 1:
            // Exclui opção 1 do menu do segundo atributo
            printf("2. Área\n3. PIB\n4. Número de pontos turísticos\n5. Densidade demográfica\n");
            break;
        case 2:
            // Exclui opção 2
            printf("1. População\n3. PIB\n4. Número de pontos turísticos\n5. Densidade demográfica\n");
            break;
        case 3:
            // Exclui opção 3
            printf("1. População\n2. Área\n4. Número de pontos turísticos\n5. Densidade demográfica\n");
            break;
        case 4:
            // Exclui opção 4
            printf("1. População\n2. Área\n3. PIB\n5. Densidade demográfica\n");
            break;
        case 5:
            // Exclui opção 5
            printf("1. População\n2. Área\n3. PIB\n4. Número de pontos turísticos\n");
            break;
    }
    printf("Opção: ");
    scanf("%d", &atributo2);

    // Validação do segundo atributo (não pode ser igual ao primeiro)
    if (atributo2 < 1 || atributo2 > 5 || atributo2 == atributo1) {
        printf("Opção inválida! Encerrando programa.\n");
        return 1;
    }

    // --- Mudança 3: Obter valores e nomes dos atributos escolhidos ---
    float val1_attr1 = 0, val2_attr1 = 0, val1_attr2 = 0, val2_attr2 = 0;
    char nomeAttr1[50], nomeAttr2[50];

    // Obter valores e nome do primeiro atributo
    switch (atributo1) {
        case 1:
            val1_attr1 = (float)populacao01;
            val2_attr1 = (float)populacao02;
            sprintf(nomeAttr1, "População");
            break;
        case 2:
            val1_attr1 = area01;
            val2_attr1 = area02;
            sprintf(nomeAttr1, "Área (km²)");
            break;
        case 3:
            val1_attr1 = pib01;
            val2_attr1 = pib02;
            sprintf(nomeAttr1, "PIB (bilhões de reais)");
            break;
        case 4:
            val1_attr1 = (float)pontosTuristicos01;
            val2_attr1 = (float)pontosTuristicos02;
            sprintf(nomeAttr1, "Número de pontos turísticos");
            break;
        case 5:
            val1_attr1 = densidade01;
            val2_attr1 = densidade02;
            sprintf(nomeAttr1, "Densidade demográfica (habitantes/km²)");
            break;
    }

    // Obter valores e nome do segundo atributo
    switch (atributo2) {
        case 1:
            val1_attr2 = (float)populacao01;
            val2_attr2 = (float)populacao02;
            sprintf(nomeAttr2, "População");
            break;
        case 2:
            val1_attr2 = area01;
            val2_attr2 = area02;
            sprintf(nomeAttr2, "Área (km²)");
            break;
        case 3:
            val1_attr2 = pib01;
            val2_attr2 = pib02;
            sprintf(nomeAttr2, "PIB (bilhões de reais)");
            break;
        case 4:
            val1_attr2 = (float)pontosTuristicos01;
            val2_attr2 = (float)pontosTuristicos02;
            sprintf(nomeAttr2, "Número de pontos turísticos");
            break;
        case 5:
            val1_attr2 = densidade01;
            val2_attr2 = densidade02;
            sprintf(nomeAttr2, "Densidade demográfica (habitantes/km²)");
            break;
    }

    // --- Mudança 4: Comparar individualmente os atributos ---
    int vencedor_attr1 = 0, vencedor_attr2 = 0;

    // Para densidade demográfica, menor valor vence
    if (atributo1 == 5) {
        if (val1_attr1 < val2_attr1) vencedor_attr1 = 1;
        else if (val2_attr1 < val1_attr1) vencedor_attr1 = 2;
        else vencedor_attr1 = 0; // empate
    } else {
        // Para os demais atributos, maior valor vence
        if (val1_attr1 > val2_attr1) vencedor_attr1 = 1;
        else if (val2_attr1 > val1_attr1) vencedor_attr1 = 2;
        else vencedor_attr1 = 0; // empate
    }

    if (atributo2 == 5) {
        if (val1_attr2 < val2_attr2) vencedor_attr2 = 1;
        else if (val2_attr2 < val1_attr2) vencedor_attr2 = 2;
        else vencedor_attr2 = 0; // empate
    } else {
        if (val1_attr2 > val2_attr2) vencedor_attr2 = 1;
        else if (val2_attr2 > val1_attr2) vencedor_attr2 = 2;
        else vencedor_attr2 = 0; // empate
    }

    // --- Mudança 5: Somar os valores dos atributos para cada carta ---
    float soma1 = val1_attr1 + val1_attr2;
    float soma2 = val2_attr1 + val2_attr2;

    // --- Mudança 6: Decidir vencedor pela soma ---
    int vencedor_final = 0;
    if (soma1 > soma2) vencedor_final = 1;
    else if (soma2 > soma1) vencedor_final = 2;
    else vencedor_final = 0; // empate

    // --- Mudança 7: Exibir resultado claro e organizado ---
    printf("\nComparação entre %s e %s:\n", nomeCidade01, nomeCidade02);
    printf("Atributos escolhidos: %s e %s\n\n", nomeAttr1, nomeAttr2);

    printf("%-35s %-20s %-20s\n", "Atributo", nomeCidade01, nomeCidade02);
    printf("-----------------------------------------------------------------\n");
    printf("%-35s %-20.2f %-20.2f\n", nomeAttr1, val1_attr1, val2_attr1);
    printf("%-35s %-20.2f %-20.2f\n", nomeAttr2, val1_attr2, val2_attr2);
    printf("-----------------------------------------------------------------\n");
    printf("%-35s %-20.2f %-20.2f\n", "Soma dos atributos", soma1, soma2);

    if (vencedor_final == 1) {
        printf("\nVencedor da rodada: %s\n", nomeCidade01);
    } else if (vencedor_final == 2) {
        printf("\nVencedor da rodada: %s\n", nomeCidade02);
    } else {
        printf("\nEmpate!\n");
    }

    return 0;
}