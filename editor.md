graph TD
    %% Níveis
    subgraph "Níveis do Projeto"
        P[Problema]
        O[Oportunidade]
        Obj[Objetivo]
        E[Entregáveis]
    end

    %% Ligações
    P -- GERA --> O
    O -- LEVA A --> Obj
    Obj -- RESULTA EM --> E

    %% Problema: Detalhamento
    subgraph "Problema: Sobreposição e falta de critério"
        P_Sob["Sobreposição de áreas protegidas com mineração"]
        P_Escolha["Mesma área escolhida por diferentes unidades"]
        P_Criterio["Escolha de áreas sem critérios de conservação"]
    end

    %% Oportunidade: Detalhamento
    subgraph "Oportunidade: Otimização e Tecnologia"
        O_Criterios["Escolher locais com critérios quantitativos"]
        O_Agrupar["Agrupar áreas para maximizar conservação"]
        O_Metas["Conectar metas ambientais e estratégicas"]
        O_Decisao["Apoiar a tomada de decisão"]
        O_Gestao["Agilizar processos e facilitar a gestão"]
    end

    %% Objetivo: Detalhamento
    subgraph "Objetivo: Otimizar alocação"
        Obj_Alocacao["Otimizar a alocação de áreas protegidas"]
        Obj_Algoritmo["Desenvolver algoritmo de análise espacial"]
    end

    %% Entregáveis: Detalhamento
    subgraph "Entregáveis: Produtos da solução"
        E_Algoritmo["Algoritmo para sugestão de áreas"]
        E_Mapa["Mapa com áreas recomendadas"]
        E_Relatorio["Relatório com critérios, lógica e resultados"]
    end

    %% Fluxo lógico
    P --> P_Sob & P_Escolha & P_Criterio
    O --> O_Criterios & O_Agrupar & O_Metas & O_Decisao & O_Gestao
    Obj --> Obj_Alocacao & Obj_Algoritmo
    E --> E_Algoritmo & E_Mapa & E_Relatorio

    P_Sob -- Solução --> Obj_Alocacao
    P_Criterio -- Resposta --> Obj_Algoritmo
    Obj_Algoritmo -- Produz --> E_Algoritmo & E_Mapa & E_Relatorio
