# 1_NAP_20123.1_B_Forma_Para769
C:\Users\crist\Downloads\1_NAP_20123.1_B_Forma_Para769.pdf Respondido.docx
UNIVERSIDADE FEDERAL RURAL DA AMAZÔNIA - INSTITUTO CIBERESPACIAL 
Curso: Bacharelado em Sistema de Informação 
Disciplina: Técnicas de Programação II 	 	 	Professor: Edvar da Luz Oliveira 
Aluno:  Maria Cristina Dantas de Sousa	Nota:______________________ 
Prova: 1º NAP 	 	 	 	 	                           Data: 15 / 12 / 2023 
Instruções: 
•	Prova individual, sem consulta; 
•	Todas as questões devem ser resolvidas e serão corrigidas em sala de aula 
•	Esta prova deve ser resolvida utilizando a linguagem Python. 
 
 
1.	(5,0 pts) Desenvolva um programa onde o usuário deverá informar a nota final do aluno (entre 0.0 e 10.0) e a quantidade de faltas, o programa deve informar ao aluno qual seu conceito 
(utilizar tabela abaixo para realizar a comparação). 
 
Nota 	Conceito 
	Até 6 faltas 	Acima de 6 faltas 
9.0 até 10.0 	A 	B 
7.5 até 8.9 	B 	C 
5.0 até 7.4 	C 	D 
4.0 até 4.9 	D 	D 
0.0 até 3.9 	D 	E 
 
Resposta:  
def conceito_aluno ():
    nota = float (input ("Insira a nota final do aluno (entre 0.0 e 10.0): "))
    faltas = int (input ("Insira a quantidade de faltas do aluno: "))

    if faltas <= 6:
        if 9.0 <= nota <= 10.0:
            return 'A'
        elif 7.5 <= nota < 9.0:
            return 'B'
        elif 5.0 <= nota < 7.5:
            return 'C'
        elif 4.0 <= nota < 5.0:
            return 'D'
        else:
            return 'D'
    else:
        if 9.0 <= nota <= 10.0:
            return 'B'
        elif 7.5 <= nota < 9.0:
            return 'C'
        elif 5.0 <= nota < 7.5:
            return 'D'
        else:
            return 'E'

print (conceito_aluno ())

Saída do Código:
Insira a nota final do aluno (entre 0.0 e 10.0): 9
Insira a quantidade de faltas do aluno: 6
A
O resultado é o conceito A 

2.	(2,5 pts) Desenvolva um programa para verificar se o usuário está apto a emitir o visto americano, conforme critérios estabalecidos abaixo. O programa deve emitir uma única notificação para o usuário informando se está apto ou não. 
Regras:  
a)	Possuir carteira de identidade emitida a no máximo 5 anos; 
b)	Possuir passaporte válido; 
c)	Não ser extraterrestre; 
d)	Não ter dívidas no país de origem; 
e)	Não pertencer a grupos que estimulem a violência; 
f)	Visto de negócios ou turismo. 
 Resposta:
def verifica_visto ():
    carteira_identidade = int (input ("Insira o ano de emissão da sua carteira de identidade: "))
    passaporte_valido = input ("Você possui um passaporte válido? (s/n): ") == 's'
    extraterrestre = input ("Você é um extraterrestre? (s/n): ") == 's'
    dívidas = input ("Você tem dívidas no seu país de origem? (s/n): ") == 's'
    violencia = input ("Você pertence a grupos que estimulam a violência? (s/n): ") == 's'
    visto = input ("Você está solicitando um visto de negócios ou turismo? (negócios/turismo): ")

    if carteira_identidade < 2018:
        return 'Não está apto'
    elif not passaporte_valido:
        return 'Não está apto'
    elif extraterrestre:
        return 'Não está apto'
    elif dividas:
        return 'Não está apto'
    elif violencia:
        return 'Não está apto'
    elif visto not in ['negócios', 'turismo']:
        return 'Não está apto'
    else:
        return 'Está apto'

print (verifica_visto ())

Saída do código:
Insira o ano de emissão da sua carteira de identidade: 2019
Você possui um passaporte válido? (s/n): s
Você é um extraterrestre? (s/n): n
Você tem dívidas no seu país de origem? (s/n): n
Você pertence a grupos que estimulam a violência? (s/n): n
Você está solicitando um visto de negócios ou turismo? (negócios/turismo): turismo
Está apto
________________________________________


3.	(2,5 pts) Crie uma função chamada conta_ocorrencias que recebe uma string e um caractere como parâmetros. A função deve contar o número de ocorrências do caractere na string e retornar esse valor para o programa principal, que por sua vez, deverá mostrar o resultado.

Resposta:
def conta_ocorrencias (s, c):
    contador = 0
    for caractere in s:
        if caractere == c:
            contador += 1
    return contador

frase = input ("Digite uma frase: ")
caractere = input ("Digite um caractere: ")
resultado = conta_ocorrencias (frase, caractere)
print (f"O caractere '{caractere}' aparece {resultado} vezes na frase.")


Saída do Código:

Digite uma frase: bom dia professor
Digite um caractere: o
O caractere 'o' aparece 3 vezes na frase.


 
“Os limites só existem se você os deixar existir.” 
(Goku, sem data) 
 
