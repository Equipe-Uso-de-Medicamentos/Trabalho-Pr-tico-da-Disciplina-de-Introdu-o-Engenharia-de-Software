# Engenharia de Requisitos

> **Documentação referente à Tarefa 3**  
> **Responsável:** José Felipe dos Santos Souza (felipesouj)  
> **Tema:** 7 - Saúde: Uso de Medicamentos  
> **Sistema:** Sistema de Apoio ao Uso Correto de Medicamentos  

---

## 1. Stakeholders (Partes Interessadas)

| Stakeholder | Descrição / Interesse no sistema |
| :--- | :--- |
| **Paciente (usuário principal)** | Pessoa que utiliza medicamentos de forma contínua e precisa de apoio para administrá-los corretamente. |
| **Familiar / Cuidador (usuário secundário)** | Pessoa que acompanha a rotina de medicação do paciente e precisa de visibilidade remota sobre essa rotina. |
| **Equipe do projeto** | Responsável por definir, especificar, planejar, prototipar e documentar o sistema ao longo das etapas do trabalho. |
| **Professor da disciplina** | Avaliador do projeto; define os critérios e as entregas esperadas em cada etapa. |
| **Profissionais de saúde (indireto)** | Destino recomendado em caso de alertas de interação, contraindicação ou alergia; não são usuários diretos do sistema. |

## 2. Requisitos Funcionais (RF)

| Código | Descrição | Prioridade | Critério de Aceitação |
| :---: | :--- | :---: | :--- |
| **RF01** | O sistema deve verificar possíveis interações entre os medicamentos cadastrados para o mesmo usuário. | Alta (1) | Ao cadastrar um novo medicamento, o sistema identifica e exibe alerta caso haja interação conhecida com outro medicamento já cadastrado. |
| **RF02** | O sistema deve emitir alertas sobre a dose correta de cada medicamento, sinalizando quantidades divergentes da recomendada. | Alta (2) | O sistema compara a dose registrada com a dose prescrita e alerta o usuário em caso de divergência. |
| **RF03** | O sistema deve permitir o cadastro de condições de saúde/restrições do paciente e alertar sobre medicamentos contraindicados. | Alta (3) | Ao cadastrar uma condição de saúde, o sistema passa a alertar sobre medicamentos incompatíveis com essa condição. |
| **RF04** | O sistema deve permitir o cadastro de alergias e alertar quando um medicamento contiver substância potencialmente alergênica. | Alta (4) | Ao tentar cadastrar um medicamento com substância alergênica informada, o sistema exibe alerta antes da confirmação. |
| **RF05** | O sistema deve enviar lembretes nos horários programados para cada medicamento. | Alta (5) | O usuário recebe uma notificação no horário definido para cada medicamento cadastrado. |
| **RF06** | O sistema deve informar o início e o término previsto de cada tratamento medicamentoso. | Média (6) | Ao cadastrar um tratamento com duração definida, o sistema notifica o usuário próximo à data de término. |
| **RF07** | O sistema deve disponibilizar orientações simplificadas sobre a forma correta de utilização de cada medicamento. | Média (7) | O usuário consegue acessar, a partir do cadastro do medicamento, uma orientação de uso em linguagem simplificada. |
| **RF08** | O sistema deve permitir cadastrar e identificar cada medicamento pelo nome, dosagem e finalidade. | Média (8) | O cadastro exige o preenchimento de nome, dosagem e finalidade antes de ser salvo. |
| **RF09** | O sistema deve controlar a quantidade de medicamento disponível (estoque) e alertar quando estiver próxima do fim. | Média (9) | O sistema decrementa o estoque a cada dose registrada e emite alerta ao atingir um limite mínimo. |
| **RF10** | O sistema deve manter um histórico dos medicamentos utilizados pelo paciente. | Média (10) | O usuário consegue consultar um histórico com as doses tomadas, esquecidas ou adiadas em um período. |
| **RF11** | O sistema deve permitir o registro do status de cada dose (tomada, esquecida ou adiada) com o mínimo de toques possível. | Alta | O paciente consegue registrar o status de uma dose em poucos toques na interface, sem etapas adicionais. |
| **RF12** | O sistema deve permitir que o paciente autorize o compartilhamento de sua rotina de medicamentos com um familiar/cuidador. | Alta | O compartilhamento de dados com o cuidador só é ativado mediante autorização explícita do paciente. |
| **RF13** | O sistema deve notificar o cuidador quando uma dose importante não for registrada no horário previsto ou houver esquecimentos recorrentes. | Alta | O cuidador autorizado recebe uma notificação quando uma dose não é registrada dentro de um intervalo definido. |
| **RF14** | O sistema deve possibilitar uma forma de comunicação entre paciente e cuidador relacionada à rotina de medicamentos. | Média | O cuidador consegue enviar uma mensagem ou lembrete ao paciente a partir do sistema. |
| **RF15** | O sistema deve apresentar uma interface simplificada, com poucos passos, voltada a usuários com baixa familiaridade tecnológica. | Alta | As principais tarefas do paciente são realizadas em poucas telas/etapas. |

## 3. Requisitos Não Funcionais (RNF)

| Código | Categoria | Descrição |
| :---: | :--- | :--- |
| **RNF01** | Usabilidade | A interface deve usar linguagem simples, poucos botões e elementos visuais de fácil compreensão. |
| **RNF02** | Acessibilidade | O sistema deve contar com recursos como letras maiores, contraste adequado e diferenciação clara entre medicamentos. |
| **RNF03** | Segurança e privacidade | As informações do paciente só devem ser compartilhadas com o cuidador mediante autorização explícita. |
| **RNF04** | Confiabilidade | Lembretes e alertas devem ser entregues de forma consistente, sem falhas de disparo. |
| **RNF05** | Desempenho | O registro do status de uma dose deve ser processado com resposta rápida. |
| **RNF06** | Disponibilidade | O sistema deve estar disponível continuamente para garantir a entrega de lembretes. |
| **RNF07** | Portabilidade | O sistema deve poder ser usado em dispositivo móvel (smartphone). |

## 4. Regras de Negócio e Restrições
* **RN01:** Todo alerta relacionado a interação medicamentosa, contraindicação ou alergia deve orientar o usuário a procurar um profissional de saúde, sem substituir o aconselhamento médico.
* **RN02:** O compartilhamento de informações exige autorização prévia e explícita do paciente.
* **RN03:** Um cadastro de medicamento só é válido quando contém nome, dosagem e finalidade.
* **RN04:** O cuidador deve ser notificado apenas em situações relevantes, evitando notificações desnecessárias.
* **Restrição:** O sistema não fornece diagnósticos médicos.

## 5. Requisitos de Dados (Entidades)

| Entidade | Atributos / Informações associadas |
| :--- | :--- |
| **Medicamento** | Nome, dosagem, finalidade, horário(s) de uso, quantidade em estoque, substâncias. |
| **Tratamento** | Medicamento associado, data de início, data prevista de término. |
| **Paciente** | Condições de saúde/restrições, alergias cadastradas, histórico de doses. |
| **Registro de dose** | Medicamento, horário previsto, status (tomada, esquecida, adiada), data/hora do registro. |
| **Cuidador** | Dados de contato, vínculo com o paciente, permissões de acesso autorizadas. |
