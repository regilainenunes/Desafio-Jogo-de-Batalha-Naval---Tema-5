# Desafio-Jogo-de-Batalha-Naval---Tema-5
#include <stdio.h>

/*
 * DESAFIO TEMA 5 - JOGO DE BATALHA NAVAL
 * Objetivo: Posicionar navios em um tabuleiro 10x10 usando matrizes e vetores.
 * Nível: Novato
 */

int main() {
    // 1. Represente o Tabuleiro: Matriz 10x10 inicializada com 0 (água)
    int tabuleiro[10][10];
    
    // Inicializando o tabuleiro com zeros usando loops aninhados
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            tabuleiro[i][j] = 0;
        }
    }

    // 2. Posicione os Navios: Dois vetores de tamanho 3 (valor 3 representa o navio)
    int navioHorizontal[] = {3, 3, 3};
    int navioVertical[] = {3, 3, 3};

    // Coordenadas iniciais (definidas diretamente no código conforme requisito)
    int linhaH = 2, colunaH = 1; // Navio Horizontal
    int linhaV = 5, colunaV = 7; // Navio Vertical

    // Posicionando o Navio Horizontal no tabuleiro
    for (int i = 0; i < 3; i++) {
        tabuleiro[linhaH][colunaH + i] = navioHorizontal[i];
    }

    // Posicionando o Navio Vertical no tabuleiro
    for (int i = 0; i < 3; i++) {
        tabuleiro[linhaV + i][colunaV] = navioVertical[i];
    }

    // 3. Exiba o Tabuleiro: Loops aninhados para mostrar a matriz no console
    printf("### TABULEIRO DE BATALHA NAVAL ###\n\n");
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            printf("%d ", tabuleiro[i][j]); // Exibe o valor com um espaço separador
        }
        printf("\n"); // Quebra de linha ao final de cada linha da matriz
    }

    return 0;
}
