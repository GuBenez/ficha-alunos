ficha = []
alunos =[]

while True:
    nome = str(input("Digite um nome: "))
    nota1 = float(input("Insira a primeira nota: "))
    nota2 = float(input("Insira a segunda nota: "))
    media = (nota1 + nota2) / 2
    ficha.append([nome, [nota1, nota2], media])
    resp = str(input("Deseja continuar: [S/N] ")).strip().upper()[0]
    if resp == "N":
        break
print("-=" * 13)
print(f"{'No.':<4}{'NOME':<10}{'MÉDIA':>8}")
print("-=" * 13)
for i, a in enumerate(ficha):
    print(f'{i:<4} {a[0]:<10} {a[2]:>5.1f}')
while True:
    print("-=" * 15)
    opc = int(input("Mostra as notas de qual aluno? (999 para encerrar): "))
    if opc == 999:
        break
        print("Finalizando...")
    if opc <= len(ficha) :
        print(f"Notas de {ficha[opc][0]} são {ficha[opc][1]}")