# ============================================================
# EXERCÍCIO 1 - SÃO MÚLTIPLOS
# ============================================================

a = int(input())
b = int(input())

if a % b == 0 or b % a == 0:
    print("Sao Multiplos")
else:
    print("Nao sao Multiplos")


# ============================================================
# EXERCÍCIO 2 - ORDENAR TRÊS NÚMEROS
# ============================================================

a = int(input())
b = int(input())
c = int(input())

original = [a, b, c]

ordenados = original.copy()

ordenados.sort()

for numero in ordenados:
    print(numero)

print()

for numero in original:
    print(numero)


# ============================================================
# EXERCÍCIO 3 - NÚMEROS ÍMPARES
# ============================================================

x = int(input())

for numero in range(1, x + 1):

    if numero % 2 != 0:
        print(numero)


# ============================================================
# EXERCÍCIO 4 - QUANTIDADE DE LINHAS
# ============================================================

N = int(input())

for _ in range(N):
    print(f"{contador} {contador + 1} {contador + 2} PUM")
    contador += 4


# ============================================================
# EXERCÍCIO 5 - MÁQUINA DE CAFÉ
# ============================================================

a1 = int(input())
a2 = int(input())
a3 = int(input())

tempo1 = a2 * 2 + a3 * 4

tempo2 = a1 * 2 + a3 * 2

tempo3 = a1 * 4 + a2 * 2

resultado = min(tempo1, tempo2, tempo3)

print(resultado)


# ============================================================
# EXERCÍCIO 6 - CONTADOR DE COMBUSTÍVEIS
# ============================================================

alcool = 0
gasolina = 0
diesel = 0

while True:

    codigo = int(input())

    if codigo == 4:
        break

    elif codigo == 1:
        alcool += 1

    elif codigo == 2:
        gasolina += 1

    elif codigo == 3:
        diesel += 1

print("MUITO OBRIGADO")
print(f"Alcool: {alcool}")
print(f"Gasolina: {gasolina}")
print(f"Diesel: {diesel}")


# ============================================================
# EXERCÍCIO 7 - FIZZBUZZ
# ============================================================

n = int(input())

answer = []

for i in range(1, n + 1):

    if i % 3 == 0 and i % 5 == 0:
        answer.append("FizzBuzz")

    elif i % 3 == 0:
        answer.append("Fizz")

    elif i % 5 == 0:
        answer.append("Buzz")

    else:
        answer.append(str(i))

print(answer)


# ============================================================
# EXERCÍCIO 8 - VAI TER COPA!
# ============================================================

while True:

    try:
        n = int(input())

    except EOFError:
        break

    if n == 0:
        print("vai ter copa!")

    else:
        print("vai ter duas!")


# ============================================================
# EXERCÍCIO 9 - FIBONACCI
# ============================================================

n = int(input())

a = 0
b = 1

resultado = []

for i in range(n):

    resultado.append(str(a))

    proximo = a + b

    a = b
    b = proximo

print(" ".join(resultado))


# ============================================================
# EXERCÍCIO 10 - ENIGMA
# ============================================================

mensagem = input()
crib = input()

contador = 0

limite = len(mensagem) - len(crib) + 1

for inicio in range(limite):

    posicao_valida = True

    for j in range(len(crib)):

        letra_mensagem = mensagem[inicio + j]
        letra_crib = crib[j]

        if letra_mensagem == letra_crib:
            posicao_valida = False
            break

    if posicao_valida:
        contador += 1

print(contador)
