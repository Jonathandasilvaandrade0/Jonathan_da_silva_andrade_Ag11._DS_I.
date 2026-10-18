# Jonathan_da_silva_andrade_Ag11._DS_I.
from colorama import Fore, Style, init

# Inicializa o colorama para garantir o funcionamento correto das cores no terminal
init(autoreset=True)

# Lista contendo os níveis, suas situações e as cores sugeridas
niveis_reservatorio = [
    {"nivel": 1, "situacao": "Muito baixo (crítico)", "cor": Fore.RED},
    {"nivel": 2, "situacao": "Baixo", "cor": Fore.YELLOW},
    {"nivel": 3, "situacao": "Médio", "cor": Fore.GREEN},
    {"nivel": 4, "situacao": "Alto", "cor": Fore.CYAN},
    {"nivel": 5, "situacao": "Muito alto (alerta)", "cor": Fore.BLUE},
]


def exibir_monitoramento(niveis):
    """Função responsável por percorrer a lista de níveis e exibir cada situação no terminal com sua respectiva cor."""
    print("=" * 60)
    print("SISTEMA DE MONITORAMENTO DE RESERVATÓRIO DE ÁGUA")
    print("=" * 60)
    for item in niveis:
        num_nivel = item["nivel"]
        situacao = item["situacao"]
        cor_alerta = item["cor"]
        print(f"{cor_alerta}[Nível {num_nivel}] - Situação: {situacao}")
    print("=" * 60)
    print(Style.RESET_ALL)


if __name__ == "__main__":
    exibir_monitoramento(niveis_reservatorio)
    input("Pressione Enter para sair...")
