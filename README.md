
Lógica para o desenvolvimento
O programa simula um pedido de lanchonete, Primeiro recebe a escolha e a quantidade do usuário, Depois usa pra identificar o lanche e calcular o total. Se o valor passar de R$20 e tiver 2 ou mais itens, aplica 10% de desconto.
# Entrada de dados interna - cardápio com nome dos lanches
lanche1_nome = "Hambúrguer"  # str
lanche1_preco = 10.00        # float
lanche2_nome = "Batata Frita" # str
lanche2_preco = 7.50         # float
lanche3_nome = "Refrigerante" # str
lanche3_preco = 5.00         # float

# Mostra o cardápio usando o nome dos lanches
print("--- Cardápio da Lanchonete ---")
print(f"1 - {lanche1_nome}: R$ {lanche1_preco:.2f}")
print(f"2 - {lanche2_nome}: R$ {lanche2_preco:.2f}")
print(f"3 - {lanche3_nome}: R$ {lanche3_preco:.2f}")

# Entrada de dados externa - usuário
opcao = int(input("\nDigite o número do lanche: ")) # int
quantidade = int(input("Digite a quantidade: "))   # int

# Processamento
nome_lanche = ""        # str
preco_lanche = 0.0      # float
tem_desconto = False    # bool
opcao_valida = True     # bool

if opcao == 1:
    nome_lanche = lanche1_nome
    preco_lanche = lanche1_preco
elif opcao == 2:
    nome_lanche = lanche2_nome
    preco_lanche = lanche2_preco
elif opcao == 3:
    nome_lanche = lanche3_nome
    preco_lanche = lanche3_preco
else:
    opcao_valida = False
    print("Opção inválida! Escolha 1, 2 ou 3.")

if opcao_valida:
    total = preco_lanche * quantidade # Operação matemática

    # Operadores lógicos and
    if total > 20.00 and quantidade >= 2:
        tem_desconto = True
        total_com_desconto = total * 0.9

    # Saída de dados com nome do lanche
    print("\n--- Resumo do Pedido ---")
    print(f"L
