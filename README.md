flowchart TD
    A([Início]) --> B[Paciente acessa a plataforma]
    B --> C{Possui cadastro?}

    C -- Sim --> D[Login]
    C -- Não --> E[Cadastro]

    E --> F[Informar dados pessoais]
    F --> G[Informar dados de contato]
    G --> H[Definir senha]
    H --> I[Aceitar Termos e Política de Privacidade]

    I --> J{Dados válidos?}

    J -- Não --> K[Exibir erros]
    K --> F

    J -- Sim --> L[Enviar código de confirmação]
    L --> M{Código válido?}

    M -- Não --> N[Solicitar novo código]
    N --> L

    M -- Sim --> O[Ativar cadastro]

    D --> P{Credenciais válidas?}
    P -- Não --> Q[Informar erro de autenticação]
    Q --> D

    P -- Sim --> O

    O --> R[Painel do paciente]

    R --> S{Primeiro acesso?}

    S -- Sim --> T[Completar informações do paciente]
    T --> U[Informar contato de emergência]
    U --> V[Preencher questionário inicial]
    V --> W[Salvar informações]

    S -- Não --> W

    W --> X{Deseja agendar consulta?}

    X -- Não --> Y[Painel do paciente]
    X -- Sim --> Z[Consultar profissionais disponíveis]

    Z --> AA[Selecionar psicólogo]
    AA --> AB[Consultar agenda]
    AB --> AC[Selecionar data e horário]
    AC --> AD[Confirmar agendamento]

    AD --> AE{Pagamento necessário?}

    AE -- Sim --> AF[Realizar pagamento]
    AF --> AG{Pagamento aprovado?}

    AG -- Não --> AH[Informar falha no pagamento]
    AH --> AF

    AG -- Sim --> AI[Confirmar consulta]

    AE -- Não --> AI

    AI --> AJ[Enviar confirmação por e-mail/SMS]
    AJ --> AK([Fim])

    Y --> AK
