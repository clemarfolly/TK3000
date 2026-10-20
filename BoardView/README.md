# Boardview do TK3000

Essa pasta aqui é só pra guardar o **arquivo Boardview da placa da TK3000** (Revisão 1). Basicamente é a placa inteira descrita num arquivo de texto, pra você abrir num programa e ficar "navegando" por ela sem precisar ter a placa física na mão.

---

## 📄 O que tem aqui

| Arquivo | O que é |
|---|---|
| `TK3000_Rev1.brd` | O arquivo Boardview da placa da TK3000 Rev.1 |

Dados rápidos do arquivo:

- **327** componentes (partes)
- **352** nets (sinais/trilhas elétricas conectadas)
- **1940** pontos de solda (pads/pins)
- Outline da placa: ~10558 x 10491 (unidades do arquivo)

> ⚠️ Esse `.brd` **não é** arquivo de projeto do KiCad/Eagle apesar do nome. É o formato de boardview.

---

## 🤔 Mas afinal, o que é esse "Boardview"?

Boardview é um **arquivo de texto que descreve uma placa de circuito impresso**: onde fica cada componente, onde estão os pads, quais pads estão conectados em qual net, o contorno da placa e por aí vai.

Ele **não tem** o desenho gráfico bonitinho tipo o do KiCad (trilhas, cobre, silkscreen). O que ele tem é a **informação elétrica e de posição** — ou seja, a "malha" da placa.

### Pra que serve?

É a ferramenta **nº 1 de quem conserta placa** (reparo de placa-mãe, retrocomputação, conserto de videogame etc.). Serve pra:

- **Rastrear um sinal**: "esse pino do processador vai parar onde?" → o programa te mostra todos os pontos conectados naquela net.
- **Achar um componente**: procura pelo designador (R94, C35, UC1...) e ele já te mostra onde está na placa.
- **Testar continuidade sem multímetro**: você clica num pad e vê tudo que está ligado nele.
- **Comparar com outra placa**: muita gente usa boardview de placa boa pra avariar placa ruim.
- **Planejar o reparo**: descobrir o que é cada componente e o que ele faz no circuito.

No fundo, ele funciona parecido com o "netlist" do esquema, só que com **coordenadas na placa** junto.

### E os formatos?

Existem vários formatos de boardview (`.brd`, `.bv`, `.bdv`, `.bvr`, `.fbrd`, `.asc`...), quase todos exportados de softwares de teste de fabricação (tipo GenCAD/IPC-D-356) ou de software proprietário de fabricante. Cada programa lê um formato diferente, então o ideal é usar um que abra **vários** — e é justamente o caso do OpenBoardView.

---

## ✅ Recomendação: abra com o OpenBoardView

O programa que a gente recomenda é o **[OpenBoardView](https://openboardview.org/)**. Motivos:

- É **gratuito** e **open source** (código aberto).
- Roda em **Windows, Linux e Mac**.
- Lê **vários formatos** de boardview, inclusive o `.brd`.
- É rápido, leve e feito **pensando em quem conserta placa**.

### Como abrir o arquivo

1. Baixe o programa na página oficial: **<https://openboardview.org/>** (aba *Releases* / Downloads).
2. Instale (no Windows é só descompactar e rodar o `.exe`).
3. Abre o OpenBoardView.
4. Aperta **`Ctrl + O`** (ou `File > Open`) e navega até essa pasta: BoardView\TK3000_Rev1.brd`
5. Pronto, a placa aparece na tela. 🎉

### Atalhos úteis (os mais usados)

| Atalho | O que faz |
|---|---|
| **`Ctrl + O`** | Abre um arquivo de boardview |
| **Barra de espaço** | Vira a placa (topo ↔ bottom) |
| **`W` / `A` / `S` / `D`** | Anda pela placa |
| **Scroll do mouse**, `-` / `=` | Zoom out / in |
| **`X`** | Reseta o zoom e centraliza |
| **`R`** (e `,` no sentido contrário) | Gira a placa |
| **`/` ou `Ctrl + F`** | Busca componente, net ou pino |
| **`ESC`** | Limpa a busca e a seleção |
| **`L`** | Abre a lista de nets |
| **`K`** | Abre a lista de componentes |
| **`P`** | Liga/desliga a exibição dos pinos |
| **Clica num pad** | Mostra a net e todos os pontos conectados |

> 💡 **Dica:** dá pra **arrastar o arquivo com o mouse** direto pra janela do programa, nem precisa do `Ctrl + O`.

---

## 💡 Dicas de uso no dia a dia

- **Procurando um componente?** Digite o designador na busca. Ele destaca na placa e te mostra a posição.
- **Rastreando um sinal?** Clique em qualquer pad da net → o OpenBoardView marca **todos** os pads daquela net na placa inteira. Aí é só ir testando um por um com o multímetro.
- **Conferindo com o esquema?** O esquema elétrico do TK3000 e o arquivo KiCad do projeto estão na pasta `../KiCad/` lá do repositório. O boardview é o complemento dele: o esquema mostra *o quê* se conecta, o boardview mostra *onde* está na placa.
- **Não achou o pad?** Dê zoom bem perto que os designadores de componente aparecem. 

---

## 📚 Links

- Site oficial do OpenBoardView: <https://openboardview.org/>
- Código-fonte: <https://github.com/OpenBoardView/OpenBoardView>
- Projeto da placa (KiCad): pasta `../KiCad/` deste repositório

---

*Arquivo gerado a partir do projeto da TK3000 — Revisão 1.*
