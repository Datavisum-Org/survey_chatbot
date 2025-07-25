# Sistema de Análise Multidimensional - Chatbot IA

## Visão Geral

O sistema v2 implementa uma análise em **5 dimensões** para avaliar o perfil do cliente e determinar o esforço de desenvolvimento necessário para implementação de um chatbot com IA.

## As 5 Dimensões

### 1. **Maturidade Organizacional** (Peso: 25%)

**Objetivo:** Avaliar o nível de maturidade em processos, tecnologia e gestão da empresa.

**Perguntas:**

- Processos de atendimento (0-3 pts)
- Maturidade tecnológica (0-3 pts)
- Organização e qualidade dos dados (0-3 pts)

**Lógica:** Empresas mais maduras = menor esforço de implementação

### 2. **Capacidade de Investimento** (Peso: 20%)

**Objetivo:** Avaliar o orçamento disponível e prioridade do projeto.

**Perguntas:**

- Faixa de investimento (0-3 pts)
- Prioridade do projeto (0-3 pts)
- Urgência de implementação (0-3 pts)

**Lógica:** Maior capacidade = projetos mais robustos

### 3. **Complexidade Técnica** (Peso: 25%)

**Objetivo:** Avaliar a complexidade de integrações e funcionalidades.

**Perguntas:**

- Número de integrações necessárias (0-3 pts)
- Escopo de funcionalidades (0-3 pts)
- Volume de dados a processar (0-3 pts)

**Lógica:** Maior complexidade = maior esforço técnico

### 4. **Esforço de Implementação** (Peso: 20%)

**Objetivo:** Avaliar o esforço necessário para implementação e mudança organizacional.

**Perguntas:**

- Preparação da equipe (0-3 pts)
- Necessidade de redesenho de processos (0-3 pts)
- Nível de gestão de mudança (0-3 pts)

**Lógica:** Maior resistência = maior esforço de implementação

### 5. **Tempo de Execução** (Peso: 10%)

**Objetivo:** Avaliar o tempo necessário para implementação.

**Perguntas:**

- Escopo total do projeto (0-3 pts)
- Disponibilidade de recursos internos (0-3 pts)
- Dependências externas (0-3 pts)

**Lógica:** Maior escopo = mais tempo necessário

## Cálculo do Score Final

### Fórmula de Pontuação Ponderada

```text
Score Final = Σ(Dimensão_i × Peso_i) / Σ(Pesos)
```

### Multiplicadores de Preço

- **Score ≤ 25%:** 1.1x (Baixa Complexidade)
- **Score ≤ 50%:** 1.4x (Complexidade Média)
- **Score ≤ 75%:** 1.8x (Alta Complexidade)
- **Score > 75%:** 2.2x (Muito Alta Complexidade)

## Cálculo do Orçamento

### Orçamento Base

```text
Orçamento Base = R$ 15.000 × Multiplicador_Porte × Multiplicador_Faturamento
```

**Multiplicadores por Porte:**

- Micro (até 9 func.): 0.5x
- Pequena (10-49 func.): 1.0x
- Média (50-249 func.): 2.0x
- Grande (250+ func.): 4.0x

**Multiplicadores por Faturamento:**

- Até R$ 360k: 0.7x
- R$ 360k - R$ 4,8M: 1.0x
- R$ 4,8M - R$ 50M: 1.5x
- Acima de R$ 50M: 2.0x

### Orçamento Final

```text
Orçamento Final = Orçamento Base × Multiplicador_Complexidade
```

## Cálculo do Tempo Estimado

### Base de Cálculo

- **Tempo base:** 4 semanas
- **Ajustes por dimensão:**
  - Complexidade > 50%: +2 semanas
  - Esforço > 50%: +2 semanas
  - Execução > 50%: +1 semana
- **Ajuste final por score:**
  - Score > 75%: +2 semanas
  - Score > 50%: +1 semana

**Limite:** Entre 4 e 12 semanas

## Vantagens do Sistema Multidimensional

### 1. **Precisão Aprimorada**

- Considera múltiplos fatores que impactam o esforço
- Evita simplificações excessivas

### 2. **Transparência**

- Cada dimensão é avaliada independentemente
- Cliente entende os fatores que influenciam o preço

### 3. **Flexibilidade**

- Sistema pode ser ajustado alterando pesos
- Novas dimensões podem ser adicionadas

### 4. **Justificativa Técnica**

- Baseado em métricas objetivas
- Facilita a comunicação com o cliente

## Comparação com Sistema Anterior

| Aspecto       | Sistema V1           | Sistema V2                                                 |
| ------------- | -------------------- | ---------------------------------------------------------- |
| Dimensões     | 1 (maturidade geral) | 5 (maturidade, investimento, complexidade, esforço, tempo) |
| Pesos         | Não aplicável        | Ponderados por importância                                 |
| Precisão      | Baixa                | Alta                                                       |
| Transparência | Limitada             | Completa                                                   |
| Flexibilidade | Baixa                | Alta                                                       |

## Implementação

### Arquivos

- `index_v2.html` - Survey principal
- `email_template_v2.html` - Template de email
- `SISTEMA_MULTIDIMENSIONAL.md` - Esta documentação

### Configuração EmailJS

- Service ID: `service_dwa4r9k`
- Template ID: `template_jo2ayso`
- Variáveis: Todas as dimensões + score final + orçamento + timeline

## Próximos Passos

1. **Teste do Sistema:** Validar com casos reais
2. **Ajuste de Pesos:** Otimizar baseado em feedback
3. **Expansão:** Adicionar mais perguntas por dimensão se necessário
4. **Integração:** Conectar com sistema de CRM para follow-up
