# 🎮 League of Pacman  
### Pacman em C++ Orientado a Objetos com Allegro 5

<p align="center">
  <img src="docs/menu.png" width="800"/>
</p>

---

## 📌 Sobre o Projeto

O **League of Pacman** é um jogo desenvolvido em **C++** utilizando a biblioteca gráfica **Allegro 5**, aplicando conceitos de **Programação Orientada a Objetos**.

O jogador controla o Pacman em um mapa baseado em matriz, onde deve:

- 🍪 Comer todas as pirulas do mapa  
- 👾 Evitar os inimigos  
- 🏆 Vencer ao limpar completamente o labirinto  

O projeto utiliza:

- Estrutura de mapa baseada em arquivo `.txt`
- Sistema de colisão por grid
- Herança para comportamento dos inimigos
- Áudio com Allegro Audio
- Renderização por sprites
- Organização modular em múltiplas classes

---

# 🖼️ Demonstração

## 🔹 Menu Inicial

<p align="center">
  <img src="docs/menu.png" width="800"/>
</p>

## 🔹 Gameplay

<p align="center">
  <img src="docs/gameplay.png" width="800"/>
</p>

---

# 🧠 Arquitetura do Projeto

## 📁 Estrutura do Projeto

```

Projeto/
│
├── Main.cpp
├── Linux.mak
├── MacOS.mak
├── Projeto.sln
├── Projeto.vcxproj
├── Projeto.vcxproj.filters
├── packages.config
│
├── Codigo/
│   ├── Aleatorios.cpp / .h
│   ├── Display.cpp / .h
│   ├── Inimigos.cpp / .h
│   ├── Mapa.cpp / .h
│   ├── Matriz.cpp / .h
│   ├── Movimentacao.cpp / .h
│   ├── Pacman.cpp / .h
│   ├── Perseguidor.cpp / .h
│   ├── Pirula.cpp / .h
│   ├── Placar.cpp / .h
│   ├── StructMatriz.h
│   └── Tijolinho.cpp / .h
│
├── Arquivos/
│   ├── Mapa.txt
│   └── Mapa_Antigo.txt
│
├── Images/
├── Audios/
├── Fonts/
│
└── .vscode/

````

---

# 🧩 Explicação das Classes

## 🔹 Main.cpp

Arquivo principal do jogo.  
Responsável por:

- Inicializar Allegro
- Criar o display
- Carregar o mapa
- Instanciar:
  - 1 inimigo perseguidor
  - 3 inimigos aleatórios
- Controlar o loop principal
- Gerenciar vitória e derrota
- Executar sons

---

## 🔹 Matriz

Lê o arquivo `Arquivos/Mapa.txt` e preenche a matriz:

```cpp
int dados_matriz[62][56];
````

Essa matriz representa toda a estrutura do labirinto.

---

## 🔹 Movimentacao

Classe base de movimentação.

Responsável por:

* Controle de posição
* Colisão com paredes
* Verificação de limites
* Direções (cima, baixo, esquerda, direita)

---

## 🔹 Pacman

Classe do jogador.

Controla:

* Movimento
* Colisão
* Coleta de pirulas
* Renderização do sprite

---

## 🔹 Inimigos

Classe base dos inimigos.

Define:

* Movimentação padrão
* Colisões
* Renderização

---

## 🔹 Perseguidor

Deriva de `Inimigos`.

* Segue o jogador
* Implementa comportamento mais inteligente

---

## 🔹 Aleatorios

Deriva de `Inimigos`.

* Movimento baseado em direção aleatória

---

## 🔹 Pirula

Gerencia os itens coletáveis do mapa.

---

## 🔹 Placar

Controla:

* Pontuação
* Renderização dos números
* Atualização dinâmica do score

---

# 🎮 Sistema de Inimigos

O jogo possui:

* 👁️ 1 Perseguidor (segue o Pacman)
* 🎲 3 Aleatórios (movimento randômico)

Aplicando:

* Herança
* Polimorfismo
* Reuso de código
* Especialização de comportamento

---

# 🛠️ Tecnologias Utilizadas

* C++
* Allegro 5
* Programação Orientada a Objetos
* Sistema de matriz
* Sistema de colisão por grid
* Makefile (Linux/Mac)
* Visual Studio (Windows)

---

# ▶️ Como Compilar

## ✔ Windows (Visual Studio)

1. Abra `Projeto.sln`
2. Compile
3. Execute

---

## ✔ Linux

Instale Allegro 5:

```bash
sudo apt install liballegro5-dev
```

Compile:

```bash
make -f Linux.mak
```

---

## ✔ macOS

Instale Allegro:

```bash
brew install allegro
```

Compile:

```bash
make -f MacOS.mak
```

---

# 🎮 Controles

| Tecla   | Ação         |
| ------- | ------------ |
| ↑ ↓ ← → | Movimentação |
| ENTER   | Iniciar      |
| ESC     | Sair         |

---

# 📚 Conceitos Aplicados

* Programação Orientada a Objetos
* Encapsulamento
* Herança
* Polimorfismo
* Matrizes
* Arquivos externos
* Modularização
* Controle de FPS
* Manipulação de áudio

---

# 🚀 Melhorias Futuras

* Sistema de vidas
* Power-ups
* IA mais avançada
* Ranking
* Sistema de fases
* Refatoração para ECS

---

# 👨‍💻 Autor

**Leandro Cesar Pereira**
Desenvolvedor Full Stack

🔗 [https://github.com/CrisBid](https://github.com/CrisBid)

```
