# Carga

App pessoal para registar treinos de força: exercícios, séries, cargas e RPE, com sugestão automática da próxima carga.
Funciona no telemóvel e no computador, offline, sem contas nem servidor.

## O que faz

- **Hoje**: só o treino do dia, em letra grande para consultar durante o treino. O ecrã fica ligado. Os treinos de ginásio abrem o registo de séries.
- **Semana**: calendário em grelha. Arrastas blocos (ginásio, bike, corrida, natação) para os dias, moves treinos entre dias e largas no caixote para apagar. Cada treino tem intensidade, duração e estrutura. Mostra a carga semanal (minutos × RPE), o tempo por modalidade e um gráfico por dia.
- **Alertas de carga** (aparecem também enquanto arrastas): pernas no ginásio no mesmo dia ou na véspera de corrida de qualidade/longa ou bike de intervalos/longa; pernas pesado a seguir a um dia duro; dois dias duros seguidos; semana sem descanso; mais de 3 dias duros; subida de carga acima de 30% face à semana anterior.
- **Treinar**: escolhe o treino (A/B alternam sozinhos) e regista cada série. A app preenche a carga e as reps com base na sessão anterior.
- **Progressão dupla**: quando fazes todas as séries no topo do intervalo de reps com RPE ≤ 8,5, sugere +2,5 kg e volta ao mínimo de reps. Caso contrário, mantém a carga e pede +1 rep.
- **Descanso**: ao marcar uma série, arranca o temporizador definido no plano.
- **Histórico** com volume e duração de cada treino.
- **Progresso** por exercício: 1RM estimado (Epley), carga máxima e gráfico.
- **Plano** editável: treinos, exercícios, séries, intervalos de reps e descanso.
- **Exportar/importar** cópia em JSON.

## Plano de base

Pensado para triatlo, fase pós-época, 2×/semana:

| Treino A, inferior e core | Treino B, posterior e tronco |
|---|---|
| Agachamento 3×5–8 | Hip thrust 3×8–10 |
| Peso morto romeno 3×6–8 | Step-up 3×8–10 |
| Agachamento búlgaro 3×8–10 | Gémeos em pé unilateral 3×12–15 |
| Gémeos sentado (sóleo) 3×12–15 | Remada unilateral 3×8–10 |
| Prancha Copenhagen 3×20–30 s | Puxada / elevações 3×6–10 |
| Pallof press 3×10–12 | Face pull 3×12–15 |
| | Dead bug 3×8–10 |

## Publicar no GitHub Pages

1. Cria um repositório novo (ex.: `carga`) e envia estes ficheiros para a raiz.
2. *Settings → Pages → Build and deployment*: Source **Deploy from a branch**, branch `main`, pasta `/ (root)`.
3. Abre `https://<utilizador>.github.io/carga/` no telemóvel e escolhe **Adicionar ao ecrã principal**.

## Dados

Ficam no `localStorage` do browser de cada dispositivo (telemóvel e computador não sincronizam).
Usa **Plano → Exportar cópia** com regularidade.

## Estrutura

```
index.html            app completa (HTML, CSS, JS)
sw.js                 cache offline
manifest.json         instalação como app
icon.svg, *.png       ícones
```
