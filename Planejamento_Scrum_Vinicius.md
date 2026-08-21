# Planejamento Ágil (Scrum)

> **Documentação referente à Tarefa 6**  
> **Responsável:** Vinícius (viniciusgabrielos)  
> **Tema:** 7 - Saúde: Uso de Medicamentos  

---

## 1. Introdução e Justificativa da Metodologia
Para organizar o desenvolvimento do sistema, optamos por trabalhar com o framework **Scrum** em vez do Kanban. A justificativa para essa escolha é que o Scrum se encaixa perfeitamente na proposta de transformar um projeto grande em entregas incrementais (Sprints), permitindo desenvolver e avaliar o software aos poucos, gerando valor para o paciente desde a primeira entrega.

## 2. Planning Poker e Estimativas
As 10 User Stories definidas foram estimadas em conjunto pela equipe utilizando o Planning Poker. Os *Story Points* abaixo representam a complexidade relativa de cada funcionalidade (esforço e incerteza), e não horas de trabalho.

| Código | User Story | Prioridade | Story Points |
| :---: | :--- | :---: | :---: |
| **US01** | Interações medicamentosas | 1 | 13 |
| **US02** | Alerta de dose incorreta | 2 | 5 |
| **US03** | Contraindicações | 3 | 13 |
| **US04** | Alerta de alergias | 4 | 8 |
| **US05** | Lembretes | 5 | 5 |
| **US06** | Duração do tratamento | 6 | 3 |
| **US07** | Orientações de uso | 7 | 3 |
| **US08** | Cadastro de medicamento | 8 | 3 |
| **US09** | Controle de estoque | 9 | 5 |
| **US10** | Histórico | 10 | 5 |
| | **TOTAL** | | **63 Pontos** |

## 3. Product Backlog
O Product Backlog foi organizado considerando a prioridade, o esforço e o valor entregue ao paciente. 
*Nota Técnica:* As prioridades foram usadas como guia, mas dependências técnicas foram respeitadas. Por exemplo, a US08 (Cadastro) é a prioridade 8, mas foi movida para o início do desenvolvimento pois todas as outras histórias dependem dela.

| Ordem | User Story | Pontos | Valor para o Paciente |
| :---: | :--- | :---: | :--- |
| **1º** | Interações medicamentosas | 13 | Segurança |
| **2º** | Alerta de dose incorreta | 5 | Prevenção de erros |
| **3º** | Contraindicações | 13 | Segurança |
| **4º** | Alerta de alergias | 8 | Prevenção de riscos |
| **5º** | Lembretes | 5 | Adesão ao tratamento |
| **6º** | Duração do tratamento | 3 | Organização |
| **7º** | Orientações de uso | 3 | Uso correto |
| **8º** | Cadastro de medicamento | 3 | Organização da medicação |
| **9º** | Controle de estoque | 5 | Evitar falta de medicamento |
| **10º**| Histórico | 5 | Acompanhamento |

## 4. Planejamento das Sprints

O backlog foi distribuído em cinco Sprints para garantir utilidade real desde a primeira entrega.

### Sprint 1 - Rotina Básica (14 pts)
* **Objetivo:** Permitir que o paciente cadastre e organize seus medicamentos.
* **Backlog da Sprint:** US08 (Cadastro), US05 (Lembretes), US06 (Duração), US07 (Orientações).
* **Entrega:** O paciente já consegue cadastrar um medicamento, definir seu uso e receber lembretes.

### Sprint 2 - Segurança Medicamentosa (13 pts)
* **Objetivo:** Identificar riscos relacionados à combinação de medicamentos.
* **Backlog da Sprint:** US01 (Interações).
* **Entrega:** O sistema passa a identificar possíveis interações entre os medicamentos cadastrados.

### Sprint 3 - Prevenção de Erros (18 pts)
* **Objetivo:** Reduzir erros relacionados ao uso dos medicamentos.
* **Backlog da Sprint:** US02 (Dose incorreta), US03 (Contraindicações).
* **Entrega:** Alertas ativos sobre doses incorretas e contraindicações de saúde.

### Sprint 4 - Acompanhamento e Alergias (13 pts)
* **Objetivo:** Ampliar a proteção e facilitar o acompanhamento do tratamento.
* **Backlog da Sprint:** US04 (Alergias), US10 (Histórico).
* **Entrega:** Alertas de alergias e disponibilização do histórico de tratamento para consulta.

### Sprint 5 - Controle e Integração (5 pts)
* **Objetivo:** Completar o acompanhamento e finalizar a integração do sistema.
* **Backlog da Sprint:** US09 (Controle de estoque).
* **Entrega:** Gestão de estoque e espaço reservado para ajustes finais e verificação de requisitos não funcionais.
