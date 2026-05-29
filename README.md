# desenvolver-algoritmo-py
A pessoa digita nome e dados do aluno e codigo indica se ele foi aprovado ou nao



    alunos = []
    while True:
        nome = input("Digite nome do aluno:")
        cpf=input("Digite o CPF:")
        email=input("Digite o email:")
        matricula = input("Digite a matricula:")

    nota1 = float(input("Digite a nota 1:"))
    nota2 = float(input("Digite a nota 2:"))
    nota3 = float(input("Digite a nota 3:"))

    media = (nota1 + nota2 + nota3) / 3

    #Se menor que 6 pede outra nota
    if media <6:
        print("Media insuficiente. Digite uma nota extra")
        nota_extra = float(input("Nota extra: "))
        media = (nota1 + nota2 + nota3 + nota_extra) / 4

    #Apro Reprov
    
    if media >= 6:
        situacao = "Aprovado"
    else:
        situacao = "Reprovado"

    if media >= 6:
        print(f"\nAluno {nome}, você foi aprovado!")
        print("Seu diploma terá os seguintes dados:")
        print(f"Nome: {nome}")
        print(f"CPF: {cpf}")
        print(f"Email: {email}")
        print(f"Matrícula: {matricula}")
        print(f"Média: {media:.2f}")
    else:
        print(f"\nAluno {nome}, você foi reprovado.")


    aluno = {
        "nome": nome,
        "cpf": cpf,
        "email": email,
        "matricula": matricula,
        "media": media,
        "situação": situacao
    }        

    alunos.append(aluno)

    continuar = input("Quer cadastrar outro aluno? (s/n)")
    if continuar.lower() != 's':
        break
        
    print("\nLista de alunos:")
    for a in alunos:
        print(a)
