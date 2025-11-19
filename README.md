# Arvores - Estrutura de Dados

# 🐾 AnimalClassifier  
### Jogo simples de adivinhação de animais usando árvore binária em Java

O **AnimalClassifier** é um jogo interativo no terminal em que o programa tenta adivinhar qual animal o usuário está pensando através de perguntas de **Sim/Não**.  
A lógica utiliza uma **árvore binária de decisões**, onde cada pergunta leva a um próximo nó até chegar a um animal.

---

## 📚 Sumário
- [Descrição](#-descrição)
- [Funcionalidades](#-funcionalidades)
- [Estrutura da Árvore Inicial](#-estrutura-da-árvore-inicial)
- [Como Jogar](#-como-jogar)
- [Arquitetura do Projeto](#-arquitetura-do-projeto)
- [Como Executar](#-como-executar)
- [Melhorias Futuras](#-melhorias-futuras)
- [Exemplo de Execução](#-exemplo-de-execução)
- [Licença](#-licença)

---

## 📝 Descrição

Este projeto demonstra como implementar uma árvore de decisão em Java para criar um jogo de perguntas e respostas.  
O jogador pensa em um animal, responde às perguntas, e o sistema tenta identificá-lo.

---

## ✨ Funcionalidades

- Sistema de perguntas interativas com respostas **S/N**.  
- Árvore binária simples com animais pré-definidos.  
- Navegação recursiva pela árvore de decisão.  
- Validação de entrada do usuário.  
- Estrutura de código clara e fácil de expandir.

---

## 🌳 Estrutura da Árvore Inicial

A árvore configurada no código é a seguinte:

Vive primariamente na água?

├── Sim
│ └── Tem pele lisa e úmida, sem escamas ou pelos?
│ ├── Sim → sapo
│ └── Não → salamandra
└── Não
└── É coberto por pelos/cabelo?
└── Sim
└── É um animal tipicamente domesticado/de estimação?
├── Sim → cachorro
└── Não → rato

---

## 🎮 Como Jogar

1. Execute o programa.  
2. Pense em um dos animais disponíveis na árvore inicial:  
   - sapo  
   - salamandra  
   - cachorro  
   - rato  
3. Responda **S** ou **N** às perguntas exibidas.  
4. O programa tentará adivinhar seu animal ao chegar em um nó folha.

---

## 🧩 Arquitetura do Projeto

### 🏗 Classe `AnimalClassifier`
Responsável por:

- Construção da árvore inicial  
- Controle do fluxo do jogo  
- Leitura de entrada via teclado  
- Navegação recursiva na árvore  

### 🌿 Classe `No`

Representa cada nó da árvore.

```java
class No {
    String conteudo; // Pergunta ou nome do animal
    No sim;          // Caminho caso a resposta seja "Sim"
    No nao;          // Caminho caso a resposta seja "Não"

    boolean ehConclusao() {
        return sim == null && nao == null;
    }
}
▶️ Como Executar
Compile o arquivo Java:

javac AnimalClassifier.java
Execute o programa:

java AnimalClassifier
🔮 Melhorias Futuras
Sugestões para expansão do projeto:

Permitir que o usuário ensine novos animais quando o jogo falhar.

Gravar e carregar a árvore de decisões de um arquivo.

Interface gráfica usando Swing ou JavaFX.

Melhor tratamento de respostas (ex.: aceitar “sim”, “nao”, “s”, “n”, etc.).

Completar ramos faltantes da árvore.

🖥 Exemplo de Execução

🎉 BEM-VINDO ao Adivinha-Animal-Simples! 🎉
Pense em um dos animais da lista inicial (Sapo, Salamandra, Cachorro, Rato).

🧐 PERGUNTA: Vive primariamente na água? (S/N): s
🧐 PERGUNTA: Tem pele lisa e úmida, sem escamas ou pelos? (S/N): s
✅ CONCLUÍDO! O seu animal é um(a) SAPO!
