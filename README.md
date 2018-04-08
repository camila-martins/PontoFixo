# PontoFixo

# Código

//Tarefa 2 - Métodos Numéricos 2
#include <stdio.h>
#include <math.h>
#include <stdlib.h>

//FILE *fp

int SolucaoPontoFixo(double *x0, double prec)
{
	double x, dx, c=0;
	//fp=fopen("dados1.dat","w"); 
	do
	{
		x=cos(*x0);
		dx=fabs(x- *x0);
		*x0=x;
		//fprintf(fp,"%g\n", *x0); salvei os valores de x0 no arquivo fp para ser mais fácil plotar o gráfico do valor de x0 em função do número de interações.
		printf(""%g\n", *x0);
		c=c+1;
	}while(dx>prec);
	fclose(fp);
	return (c);
}
int main( int argc,char **argv)
{
	double x, x0, dx, prec;
	
	x0= atof(argv[1]);
	prec=atof(argv[2]);
	
	printf("\n Raiz = %.10g em %d interacoes\n", x0 ,SolucaoPontoFixo(&x0, prec));
	
	return 0;
}

