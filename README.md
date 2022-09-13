#include <stdio.h>
#include <locale.h>
#include <stdlib.h>
#include <time.h>

int main ()
{
	int numero = rand ();
	int chute, numeroaleatorio;
	int tamanho;
	
	int dificuldade;
	int tentativas=0, jogadas=0;
	int cont=0;
	
		setlocale (LC_ALL, "Portuguese");
	
	printf ("\nJOGOS-JOGOS-JOGOS\n1-FÃCIL (30 chances)\n2-MÃ‰DIO (10 chances)\n3-DIFÃCIL (10 chances)\nEscolha:");
	scanf ("%d", &dificuldade);
	
	switch (dificuldade){
			case 1:
				tamanho=10;
			tentativas = 20;
				break;
			case 2:
				tamanho=100;
			tentativas = 15;
				break;
			case 3:
				tamanho=1000;	
			tentativas = 5;
				break;
				default:
					printf ("OPÃ‡ÃƒO INVÃLIDA");
					while(getchar() != '\n');
            getchar();
            return 0;
		}
				double pontos = 1000;
		srand (time(NULL));
		
				int numerosecreto = rand () % 100;
				
			do{
		printf("\nAdivinhe o nÃºmero: ");
		scanf("%d", &numero);
		jogadas++;
		
		if(numero == numerosecreto){
			printf("ParabenizaÃ§Ã£o. VocÃª irÃ¡ acumular pontos!\n", tentativas-jogadas);
			break;
		} else if
			(numero < numerosecreto) {
				
				printf ("\nO nÃºmero secreto Ã© maior. Tente um pouco mais.\n");
				printf("\n%do tentativa\n", jogadas, tentativas);
			} else if
				(numero > numerosecreto){
					printf ("O nÃºmero secreto Ã© menor. Tente um pouco menos do valor.");
					printf ("\n%d tentativa\n", jogadas, tentativas);
					cont = tentativas; 
				}	
			
		cont ++;
		
		if (cont > tentativas) {
			break;
		}
	}while (numero != numeroaleatorio);
	
	
	if(jogadas == tentativas && cont <= tentativas){
        printf("\nGAME OVER!");
      	printf("\nO nÃºmero sorteado era: %d\n", numerosecreto);
    }
    else{
        printf("\nParabÃ©ns! PontuaÃ§Ã£o:%d\n", pontos++);
    }
}


			



