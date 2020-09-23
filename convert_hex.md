# Convertendo um número inteiro (entre 1 e 255) para um número hexadecimal

## O que é um número hexadecimal
	O sistema decimal consiste em um conjunto de 10 caracteres:
		0 1 2 3 4 5 6 7 8 9
	e utilizamos esse conjunto para construir números, combinando esses caracteres.
	Num sistema hexadecimal, utilizamos um conjunto de 16 caracteres para representar números:
		0 1 2 3 4 5 6 7 8 9 A B C D E F
	por exemplo, o número 10 no sistema decimal é representado pelo caracter "A" no sistema hexadecimal; ou ainda o número 15 decimal (15d, para simplificar) é representado pela letra "F" no sistema hexadecimal (Fh, para simplificar); Agora o número 16d é representado pelo número 10h em hexa.

	Acredito que já seja possível ver o padrão.
## Construindo o algoritmo: hexadecimal -> decimal
	Como construir um algoritmo que converta de decimal para hexadecimal?
	Primeiro notamos que o número FFh representa o número 255d. Como transformar?
		0  1  2  3  4  5  6  7  8  9  A  B  C  D  E  F
		|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
		0  1  2  3  4  5  6  7  8  9  10 11 12 13 14 15
	Transformamos a primeira letra F através da multiplicação: F*16 = 15*16=240
	A segunda letra nós somamos 240 com o seu valor na tabela: 240+F=240+15=255
	Então mostramos que o número FFh corresponde ao número 255d.
	
## Construindo o algoritmo: decimal -> hexadecimal
	Sabemos agora como transformar de hexadecimal para decimal. Mas e o contrário?

	Para transformar um número inteiro para hexadecimal, fazemos o algoritmo inverso!
	Vamos pegar um número inteiro... digamos 182. Primeiro devemos dividir 182 por 16 para obter o primeiro digito (queremos apenas o valor inteiro da divisão):
		182 / 16 = 11
	O número 11 em decimais corresponde ao dígito "B" em hexadecimais. então nosso número até agora é B#, e temos que descobrir quem é o digito #. Mas isso é fácil, pois é simplesmente o resto da divisão que acabamos de fazer!
		182 % 16 = 6 (resto da divisão de 182 por 16)
	Temos então nosso dígito! Então podemos afirmar que o número 182d corresponde a B6h.
