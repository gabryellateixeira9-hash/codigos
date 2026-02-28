# codigosdef calculadora(num1, num2, operacao):
    if operacao == 1:
        return num1 + num2
    elif operacao == 2:
        return num1 - num2
    elif operacao == 3:
        return num1 * num2
    elif operacao == 4:
        if num2 != 0:
            return num1 / num2
        else:
            return "Erro: divisão por zero"
    else:
        return None


executar = True

while executar:
    print("\n--- CALCULADORA ---")
    print("1 - Soma")
    print("2 - Subtração")
    print("3 - Multiplicação")
    print("4 - Divisão")
    print("0 - Sair")

    opcao = int(input("Escolha uma opção: "))

    if opcao == 0:
        executar = False
        print("Programa encerrado.")
    elif opcao in [1, 2, 3, 4]:
        num1 = int(input("Digite o primeiro número: "))
        num2 = int(input("Digite o segundo número: "))

        resultado = calculadora(num1, num2, opcao)
        print("Resultado:", resultado)
    else:
        print("Essa opção não existe!")
