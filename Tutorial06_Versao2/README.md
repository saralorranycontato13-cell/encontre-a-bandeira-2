# Tutorial 06 – Mapa e Câmera (Versão 2)

**Encontre a bandeira!** O personagem só vê um pedaço do mapa, e a câmera acompanha ele revelando novas áreas. Se ele bater em algum obstáculo, a fase recomeça.

- **Fase 1** (Tiny Battle): estrada em S, rio em zigue-zague, lagos com barcos, quartel azul e base vermelha cercada de barricadas. Personagem: soldado azul e bandeira vermelha.
- **Fase 2** (Tiny Ski, desafio): pistas de esqui diferentes, com bonecos de neve e chegada no canto.

## Arquivos (como no tutorial)
| Arquivo | O que é |
|---|---|
| `arte/tilemap_packed.png` | pacote **Tiny Battle** (Kenney) |
| `arte/tiny_ski/tilemap_packed.png` | pacote **Tiny Ski** (Kenney), usado na fase 2 |
| `jogo.tscn` | cena principal: `Jogo > Mundo > Chão, Pista, Água, Decoração` + `Player`, `Alvo` e `Tutorial` (Label) |
| `player.tscn` + `player.gd` | CharacterBody2D com `Animação` (idle/walk), `Corpo` e `Camera` |
| `alvo.tscn` + `alvo.gd` | Area2D com a bandeira animada e o Label "Parabéns!" |
| `fase_2.tscn` | segunda fase (desafio) |
| `menu.tscn` + `menu.gd` | menu com os botões **Fase 1** e **Fase 2** (cena principal do projeto) |

## Configurações usadas
- Janela: viewport 320×180, Esticar em `canvas_items` / `expand`, Filtro de Textura Padrão **Nearest**.
- TileSet com tiles de 16×16, um por camada. Na **Água** e na **Decoração** os tiles têm polígono de colisão na Physics Layer 0.
- Camera2D: zoom 2×, ligada, limites (0, 0, 608, 304), que é o tamanho do mapa (38×19 tiles), e Position Smoothing ligado.

## Controles
Setas do teclado.

Arte: Tiny Battle e Tiny Ski, de Kenney (www.kenney.nl), licença CC0.
