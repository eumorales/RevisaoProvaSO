# 📘 Resumo para Prova 

---

## 🧵 1. Programação Concorrente
- Execução **simultânea** de múltiplos fluxos de instruções.
- Cada thread pode operar de forma independente dentro de um processo.
- Reduz a sobrecarga de criação e gerenciamento comparado à multiprogramação tradicional.

---

## ⚠️ 2. Condição de Corrida (Race Condition)
- Ocorre quando dois ou mais processos acessam dados compartilhados ao mesmo tempo e o resultado depende da ordem de execução.
- Solução: técnicas de sincronização como semáforos, mutexes e monitores.

---

## 🔁 3. Escalonamento de Processos
### Preemptivo vs. Não-Preemptivo
- **Preemptivo:** a CPU pode ser retirada de um processo em execução (ex: RR, SJF preemptivo).
- **Não-Preemptivo:** o processo libera a CPU voluntariamente (ex: FIFO, SJF não-preemptivo).

### Objetivos do escalonamento:
- Maximizar a utilização da CPU 🧠
- Minimizar tempo de resposta e espera 🕐
- Garantir justiça entre os processos ⚖️

### Tipos de Escalonamento:
- **FIFO (First In, First Out)**
- **SJF (Shortest Job First)**
- **Prioridade** (preemptivo e não-preemptivo)
- **Round Robin (RR)**
- **Múltiplas Filas com Realimentação**

---

## 🔐 4. Problema da Seção Crítica
### Requisitos:
- Exclusão mútua ✅
- Progresso ✅
- Espera limitada ✅
- Independência de velocidade ✅

---

## 🔄 5. Semáforos
- Usados para controlar o acesso a recursos compartilhados.
- Operações: `P()` (decrementa) e `V()` (incrementa).
- Podem levar a **deadlock** ou **inanição** se mal utilizados.

---

## 🔒 6. Mutex
- Tipo de lock binário para garantir exclusão mútua.
- Usado em regiões críticas para evitar condição de corrida.

---

## 🛑 7. Deadlock
### Condições de Coffman:
1. Exclusão mútua
2. Retenção e espera
3. Não-preempção
4. Espera circular

### Estratégias:
- **Prevenção:** quebra das condições de Coffman.
- **Evitação:** análise dinâmica (ex: algoritmo do banqueiro).
- **Detecção e recuperação:** monitoramento e intervenção.

---

## 🧯 8. Starvation
- Quando um processo **nunca é escalonado** por causa da baixa prioridade.
- Solução: **realimentação de prioridades** (ex: Múltiplas Filas com Realimentação).

---

## 🧩 9. Monitores
- Estrutura de sincronização de alto nível.
- Utiliza `wait()` e `signal()` para controle de acesso.
- Muito usados em linguagens orientadas a objeto (ex: Java).

---

## 🛠️ 10. Técnicas de Proteção da Seção Crítica
- **Semáforos**
- **Mutexes**
- **Desabilitar interrupções** (sistemas embarcados)
- **Monitores**

---

## 📊 11. Políticas de Escalonamento Detalhadas
### FIFO
- Ordem de chegada.
- Simples, mas pode causar starvation de processos curtos.

### SJF
- Executa os processos com menor tempo de CPU.
- Versões: **preemptivo (SRTF)** e **não-preemptivo**.

### Round Robin (RR)
- Cada processo recebe um **quantum** de tempo.
- Boa para sistemas interativos.
- Quantum muito grande = vira FIFO; muito pequeno = muitas trocas de contexto.

### Prioridade
- Executa o processo com **maior prioridade**.
- Pode causar starvation dos processos com baixa prioridade.

### Múltiplas Filas com Realimentação
- Os processos migram entre filas com base em seu comportamento (I/O bound ou CPU bound).
- Garante justiça e evita starvation.

---

### ⏱️ Cálculos Importantes:
- **Tempo de Espera:** tempo total na fila de prontos.
- **Tempo de Retorno:** tempo total desde a chegada até o término.
- **Tempo Médio de Espera:** média dos tempos de espera de todos os processos.

---
