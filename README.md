# 📘 Resumo para Prova de Sistemas Operacionais

---

## 🧵 1. Programação Concorrente
- Execução **simultânea** de múltiplos fluxos de instruções.
- Threads compartilham a mesma memória do processo, tornando a troca de contexto mais rápida.
- Melhora a capacidade de resposta, economiza recursos e aumenta o desempenho em sistemas com vários processadores.

---

## 👥 2. Processo vs. Thread
- **Processo:** unidade de execução com memória isolada.
- **Thread:** "processo leve", compartilha memória com outras threads do mesmo processo.
- Vantagens das threads: criação mais rápida, menor custo para troca de contexto, ideal para tarefas paralelas.

### Modelos de Multithreading:
- **N:1:** várias threads de usuário mapeadas para uma única thread de kernel.
- **1:1:** cada thread de usuário tem uma thread de kernel.
- **M:N:** várias threads de usuário para várias de kernel, escalonamento em dois níveis.

---

## ⚠️ 3. Condição de Corrida (Race Condition)
- Ocorre quando dois ou mais processos acessam dados ao mesmo tempo e o resultado depende da ordem de execução.
- Solução: técnicas de sincronização como semáforos, mutexes e monitores.

---

## 🔁 4. Escalonamento de Processos
### Preemptivo vs. Não-Preemptivo
- **Preemptivo:** a CPU pode ser retirada de um processo (ex: Round Robin).
- **Não-Preemptivo:** o processo libera a CPU voluntariamente (ex: FIFO).

### Objetivos do escalonamento:
- Maximizar uso da CPU 🧠
- Minimizar tempos de espera e resposta ⏳
- Garantir justiça entre os processos ⚖️

### Escalonadores e Dispatcher
- **Escalonador de curto prazo:** escolhe qual processo será executado.
- **Dispatcher:** faz a troca de contexto e passa o controle para a CPU.

---

## 📊 5. Políticas de Escalonamento
- **FIFO (FCFS):** simples, mas pode causar longas esperas.
- **SJF:** ótimo para tempos curtos, mas difícil prever surto de CPU. Pode ser preemptivo (SRTF).
- **Prioridade:** escolhe com base em número; pode causar starvation.
- **Round Robin (RR):** bom para tempo compartilhado, depende do quantum.
- **Múltiplas Filas:** separa por tipo (interativo, batch). Cada fila pode ter seu algoritmo.
- **Múltiplas Filas com Realimentação:** processos migram entre filas, evita starvation.

### Técnicas auxiliares:
- **Envelhecimento (Aging):** aumenta prioridade de processos que esperam muito.

---

## ⏱️ 6. Métricas de Desempenho
- **Tempo de Espera:** tempo na fila de prontos.
- **Tempo de Retorno:** tempo desde a submissão até finalização.
- **Tempo de Resposta:** tempo até a primeira resposta do sistema.

---

## 🔐 7. Problema da Seção Crítica
### Requisitos:
- Exclusão mútua ✅
- Progresso ✅
- Espera limitada ✅
- Independência de velocidade ✅

---

## 🔄 8. Semáforos
- Controlam o acesso a recursos compartilhados.
- Operações: `P()` (wait) e `V()` (signal).
- Problemas: deadlock ou inanição se mal utilizados.

---

## 🔒 9. Mutex
- Lock binário que garante exclusão mútua.
- Ideal para evitar condições de corrida.

---

## 🧩 10. Monitores
- Estrutura de sincronização de alto nível.
- Utiliza `wait()` e `signal()` para controlar acesso.
- Muito usado em linguagens OO como Java.

---

## 🛠️ 11. Técnicas de Proteção da Seção Crítica
- Semáforos ✅
- Mutexes ✅
- Desabilitar interrupções ✅ (uso em sistemas embarcados)
- Monitores ✅

---

## 🛑 12. Deadlock
### Condições de Coffman:
1. Exclusão mútua
2. Retenção e espera
3. Não-preempção
4. Espera circular

### Estratégias:
- **Prevenção:** remove uma das condições.
- **Evitação:** ex: algoritmo do banqueiro.
- **Detecção e Recuperação:** identifica e mata processos ou retira recursos.

---

## 🧯 13. Starvation
- Quando um processo **nunca é executado** por estar sempre sendo preterido.
- Solução: **envelhecimento** (aging).

---

## 💻 14. Modo Dual e Chamadas ao Sistema
- **Modo usuário** vs. **Modo kernel**: garante segurança e proteção dos recursos.
- **Chamada ao sistema (System Call):** forma do programa acessar serviços do SO.
- Ex: fork, exec, wait, open, read, write, exit.
  
---
