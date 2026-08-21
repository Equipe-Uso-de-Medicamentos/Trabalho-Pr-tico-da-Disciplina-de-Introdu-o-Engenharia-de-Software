# Prototipação Visual (Alta Fidelidade)

> **Documentação referente à Tarefa 5**  
> **Responsável:** Gledson (Gledsons7)  
> **Tema:** 7 - Saúde: Uso de Medicamentos  

---

## 1. Visão Geral dos Protótipos
Foram desenvolvidos três protótipos de alta fidelidade em formato HTML/CSS interativo para demonstrar os principais fluxos do aplicativo **IMED**. O design foi concebido com foco em acessibilidade visual, utilizando tipografia legível, botões de toque amplo e cores semânticas fortes para auxiliar o público idoso.

*O arquivo executável do protótipo encontra-se na raiz deste repositório como `prototipo.html`.*

## 2. Telas Desenvolvidas

### Tela 1: Dashboard Diário
Painel principal focado na organização da rotina do paciente.
* **Funcionalidades:** Exibe a data atual, os pontos de gamificação (incentivo à adesão) e o próximo medicamento a ser tomado.
* **Lista de Medicamentos:** Apresenta os remédios do dia com status visuais claros ("Tomado" em verde, "Pendente" em amarelo e "Atrasado" em vermelho).
* **Interação:** Botões amplos para "Marcar como tomado", garantindo uma experiência com poucos toques.

### Tela 2: Alerta de Interação
Tela de aviso crítico exibida ao detectar risco na combinação de medicamentos cadastrados.
* **Funcionalidades:** Demonstra o alerta visual de risco moderado/alto (ex: Varfarina + Ibuprofeno).
* **Segurança:** Explica as possíveis consequências da interação e orienta a busca por um profissional de saúde (RF01).
* **Validação:** Exige que o usuário marque uma caixa de seleção de ciência ("Confirmo que li e entendi este alerta") antes de permitir a continuação do uso.

### Tela 3: Pessoa de Confiança
Painel de acompanhamento remoto para familiares e cuidadores.
* **Funcionalidades:** Apresenta um resumo de adesão (porcentagem de acerto semanal) e estatísticas de doses tomadas vs. esquecidas.
* **Controle de Acesso:** Lista as pessoas autorizadas (ex: Filha, Cuidadora) e permite ao paciente gerenciar permissões (acesso completo, apenas leitura ou revogar acesso).
* **Comunicação:** O sistema indica visualmente quem será notificado em caso de atrasos.
