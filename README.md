# Classificador de triângulos em C++
Classificando triângulos em escaleno, isósceles e equilátero 

<h2>Explicação</h2>
<ul>
  <li>Usamos o if para verificar se a entrada foi válida, ou seja, nenhum número menor que 0 e todos satisfazendo a condição de ser um triângulo: lado1 + lado2 > lado </li>
  <li>Com o primeiro if, verificamos se ele é equilátero (todos os lados iguais)</li>
  <li>If else: usado para verificar se é isósceles, ou seja, apenas dois lados são iguais</li>
  <li>Else: se ele não satisfazer nenhuma das condições acima, significa que ele é escaleno (nunhum de seus lados são iguais ) </li>
</ul>
<div align="center">
<h2>Fluxograma</h2>
<img src="https://raw.githubusercontent.com/LeticiaHartstein/Triangulo-Classificando_Cpp/refs/heads/main/Fluxograma-Classificar_triangulos.svg" alt="fluxograma-classificandoTriângulos">
</div>
<h2>Código</h2>
<a href="">veja/baixe o código aqui</a>

````CPP
#include <iostream>
using namespace std;

void programa() //função onde está todo o programa
{
	//decoração, não há nenhuma fuincionalidade real
	cout << "__________________________________________________________________________ \n";
	cout << "                Classificando Triangulos em C++                            \n";
	cout << "__________________________________________________________________________ \n";
	//declarando as váriaveis
	int ladoA = 0, ladoB = 0, ladoC = 0;
	//inserindo e armazenando valores (input)
	cout << "insira o tamanho dos tres lados de seu triangulo: \n";	
	cin >> ladoA >> ladoB >> ladoC;

	
	if (ladoA > 0 && ladoB > 0 && ladoC > 0 && ladoA+ladoC>ladoB && ladoC+ladoB > ladoA && ladoA+ladoB > ladoC) //verificar se todos os N° inseridos são maiores que 0 e se satisfaz a condição de triângulo
	{
		if (ladoA == ladoB && ladoB == ladoC) // verificando se todos os lados são iguais (equilátero)
		{
			cout << "equilatero";
		}
		else if (ladoA == ladoB || ladoA == ladoC || ladoC == ladoB) // verificando se dois lados são iguais (isósceles)
		{
			cout << "isosceles";
		}
		else // se não satisfazer nenhuma das consições anteriores, significa que todos os lados são diferentes (escaleno)
		{
			cout << "escaleno";
		}
	}
	else // caso o n° seja menor que zero, ou os três lados inseridos não satisfaçam a condição de triângulo
	{
		cout << "insira numeros validos!!";
	}
};
int main ()
{
	programa(); //chamar função programa()
	return 0;
}

````
<div align="center">
<h2>Testes</h2>
<table>
  <tr>
    <td><br></td>
    <td>Input:</td>
    <td>Resultado esperado:</td>
    <td>Output do programa: </td>
  </tr>
  <tr>
    <td>1°</td>
    <td>3, 2, 5</td>
    <td>Números inválidos</td>
    <td><img src="https://github.com/LeticiaHartstein/Triangulo-Classificando_Cpp/blob/main/Imagens%20de%20teste%20-%20pode%20ser%20ignorado/img-tst-1.png?raw=true" alt="primeiro teste numeros inválidos "></td>
  </tr>
  <tr>
    <td>2°</td>
    <td> 5,5,5</td>
    <td>Equilátero </td>
    <td><img src="https://github.com/LeticiaHartstein/Triangulo-Classificando_Cpp/blob/main/Imagens%20de%20teste%20-%20pode%20ser%20ignorado/img-tst-2.png?raw=true" alr="segundo teste Equilatero"></td>
  </tr>
  <tr>
    <td> 3° </td>
    <td> 10,10,5</td>
    <td> Isósceles </td>
    <td><img src="https://github.com/LeticiaHartstein/Triangulo-Classificando_Cpp/blob/main/Imagens%20de%20teste%20-%20pode%20ser%20ignorado/img-tst-3.png?raw=true" alt="terceiro teste isosceles"></td>
  </tr>
  <tr>
    <td>4°</td>
    <td>3,4,5</td>
    <td>Escaleno</td>
    <td><img src="https://github.com/LeticiaHartstein/Triangulo-Classificando_Cpp/blob/main/Imagens%20de%20teste%20-%20pode%20ser%20ignorado/img-tst-4.png?raw=true" alt="quarto teste Escaleno"></td>
  </tr>
</table>
</div>
