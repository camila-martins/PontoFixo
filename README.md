# PontoFixo

Tarefa 2 - Métodos Numéricos 2

# Código

#include <stdio.h>
#include <math.h>
#include <stdlib.h>

int SolucaoPontoFixo(double *x0, double prec)
{
	double x, dx, c=0;
	
	do
	{
		x=cos(*x0);
		dx=fabs(x- *x0);
		*x0=x;
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

# Conclusão e Observação

Através do Gráfico.png, o qual obtive através salvando os dados nos arquivos dados1.dat e dados2.date logo plotando através do gnuplot, é possível observar um comportamento oscilatório, o qual para x0=0.75 foi obtido 50 iteracoes e x0=1.50 foi obtido 60 iterações, e os dois valores de x0 converge para o mesmo valor (0.73095).

@thadeupenna
