# 📘 Resumo de Sistemas Operacionais - Palavras-Chave

---

## 🧵 Programação Concorrente
- **Execução simultânea**
- **Threads**: compartilham memória
- **Multiprocessamento**: aumento de desempenho

---

## 👥 Processo vs. Thread
- **Processo**: memória isolada
- **Thread**: "processo leve", compartilha memória
- **Vantagens**: rápido, baixo custo, paralelismo

### Modelos de Multithreading:
- **N:1**, **1:1**, **M:N**

---

## ⚠️ Condição de Corrida
- **Acesso simultâneo** a dados
- **Solução**: semáforos, mutexes, monitores

---

## 🔁 Escalonamento de Processos
- **Preemptivo** vs **Não-preemptivo**
- **Objetivos**: maximizar CPU, minimizar espera, justiça

### Escalonadores:
- **Curto prazo**: escolhe processo
- **Dispatcher**: troca de contexto

---

## 📊 Políticas de Escalonamento
- **FIFO**, **SJF**, **Prioridade**, **Round Robin**
- **Múltiplas Filas**, **Aging**

---

## ⏱️ Métricas de Desempenho
- **Tempo de Espera**
- **Tempo de Retorno**
- **Tempo de Resposta**

---

## 🔐 Problema da Seção Crítica
- **Exclusão mútua**, **Progresso**, **Espera limitada**, **Velocidade independente**

---

## 🔄 Semáforos
- **P()** (wait), **V()** (signal)
- **Controle de acesso** a recursos

---

## 🔒 Mutex
- **Lock binário**, **Exclusão mútua**

---

## 🧩 Monitores
- **Sincronização de alto nível**
- **wait()**, **signal()**

---

## 🛠️ Técnicas de Proteção da Seção Crítica
- **Semáforos**, **Mutexes**, **Interrupções**, **Monitores**

---

## 🛑 Deadlock
- **Coffman**: exclusão mútua, retenção, não-preempção, espera circular
- **Estratégias**: Prevenção, Evitação, Detecção e Recuperação

---

## 🧯 Starvation
- **Processo não executado**
- **Solução**: envelhecimento

---

## 💻 Modo Dual e Chamadas ao Sistema
- **Modo usuário** vs **Modo kernel**
- **System Call**: acesso aos serviços do SO (ex: fork, exec, wait, open)
