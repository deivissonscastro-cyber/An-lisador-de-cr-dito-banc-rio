# An-lisador-de-cr-dito-banc-rio
Criado no intuíto de avaliação de crédito
# Projeto: Simulador de Aprovação de Empréstimo
print("--- Sistema de Suporte à Decisão - Banco do Brasil (Simulação) ---")

nome = input("Nome do Cliente: ")
salario = float(input("Salário Mensal (R$): "))
valor_parcela = float(input("Valor da Parcela Desejada (R$): "))
tempo_trabalho = int(input("Meses de registro no emprego: "))

# Regra de Negócio: A parcela não pode exceder 30% do salário
limite_parcela = salario * 0.30

print(f"\nAnalisando perfil de {nome}...")

if valor_parcela <= limite_parcela and tempo_trabalho >= 6:
    print("✅ CRÉDITO PRÉ-APROVADO!")
    print(f"O valor de R$ {valor_parcela:.2f} está dentro da margem de segurança de R$ {limite_parcela:.2f}.")
else:
    print("❌ CRÉDITO NEGADO.")
    if valor_parcela > limite_parcela:
        print(f"Motivo: Parcela compromete mais que 30% da renda (Limite: R$ {limite_parcela:.2f}).")
    if tempo_trabalho < 6:
        print("Motivo: Tempo de casa insuficiente (Mínimo 6 meses).")
