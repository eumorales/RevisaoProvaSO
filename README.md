# 📘 Resumo para Prova

---

## 🧵 1. Programação Concorrente
- Execução **simultânea** de múltiplos fluxos de instruções.
- Diferente de execução sequencial ou alternada.

---

## ⚠️ 2. Condição de Corrida (Race Condition)
- Ocorre quando o **resultado depende da ordem** de execução dos processos.
- Problema comum em ambientes de concorrência mal gerenciada.

---

## 🔁 3. Escalonamento
### Preemptivo vs. Não-Preemptivo
- **Preemptivo:** o sistema pode interromper um processo para executar outro.
- **Não-Preemptivo:** o processo sai da CPU apenas voluntariamente.

---

## 🔐 4. Problema da Seção Crítica
### Requisitos para solução:
- Exclusão mútua ✅
- Progresso ✅
- Espera limitada ✅
- Independência da velocidade dos fluxos ✅

---

## 🔄 5. Semáforo
- Ferramenta de **sincronização** com valor inteiro.
- Possui **fila de espera**.
- Operações básicas: `P` (wait) e `V` (signal).

---

## 🔒 6. Mutex
- Um tipo de **lock** para garantir exclusão mútua.
- Pode ser implementado com **spin-lock** (espera ativa).

---

## 🛑 7. Deadlock
### Condições necessárias (Coffman):
1. Exclusão mútua
2. Espera circular
3. Não-preempção
4. Espera por recurso

- A **ausência** de qualquer condição impede o deadlock.
- Um sistema pode **entrar** em deadlock, mas **não necessariamente**.

---

## 🧯 8. Prevenção e Recuperação de Deadlocks
### Métodos:
- **Prevenção**: evitar as condições de Coffman
- **Detecção**: identificar e agir
- **Recuperação**: ex: terminar processo, preemptar recurso
- ❌ **Desabilitar interrupções** não é método válido de recuperação

---

## 🧩 9. Monitores
- Usam **variáveis de condição** com `wait` e `signal`
- Permitem controle refinado da **seção crítica**

---

## 🛠️ 10. Técnicas de Proteção da Seção Crítica
- Semáforos ✅
- Spin-locks ✅
- Desabilitar interrupções (em sistemas embarcados) ✅

---

## 📊 11. Políticas de Escalonamento
### FIFO (First In, First Out)
- Executa os processos na ordem de chegada.

### SJF (Shortest Job First)
- Executa os processos com **menor tempo de execução** primeiro.
- Pode ser:
  - **Preemptivo**
  - **Não-preemptivo**

### Métricas importantes:
- ⏳ **Tempo de Espera**: tempo esperando na fila.
- ⏱️ **Tempo de Retorno**: do início até o fim da execução.

---
