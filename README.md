# 📱 Senti Mais – Aplicativo de Bem-Estar Emocional

## 👥 Integrantes
- RM556546 - Samuel Camargo Lirio  
- RM556584 - Victor Miyamoto Ramos  
- RM558563 - Gabriel Stoppa de Freitas  
- RM556806 - Bruno Santos de Moura  
- RM557574 - Andriel Felipe Gomes da Silva  

---

## 📖 Resumo do Projeto
O **Senti Mais** é um aplicativo voltado à **saúde mental e ao equilíbrio emocional**.  
Ele oferece recursos interativos como:
- Check-ins de humor
- Testes psicossociais
- Exercícios de respiração
- Práticas de mindfulness
- Leituras terapêuticas
- Suporte imediato  

🎯 **Missão:** oferecer apoio prático, sigiloso e empático, prevenindo estresse, burnout e promovendo qualidade de vida.

---

## 🧑‍🤝‍🧑 Público-Alvo
- Adolescentes e adultos  
- Pessoas em situações de estresse, luto ou exaustão  
- Funcionários de empresas (com suporte corporativo)  
- Qualquer pessoa que deseje cuidar da saúde mental  

---

## 🌍 Justificativa e Contexto Social
- Mais de **970 milhões** de pessoas no mundo vivem com transtornos mentais (OMS, 2023).  
- O Brasil lidera no índice de ansiedade, com **9,3% da população afetada** (OMS).  
- A cada **40 segundos**, uma pessoa comete suicídio no mundo.  
- No Brasil, há **13 mil suicídios por ano**, sendo a **2ª maior causa de morte** entre jovens de 15 a 29 anos.  
- Para cada suicídio, há pelo menos **20 tentativas**.  
- Em 2022, a OMS reconheceu o **burnout** como síndrome ocupacional.  
- **30%** dos trabalhadores brasileiros já sofreram burnout (ISMA-BR).  
- O **estresse** está entre as 10 principais causas de afastamento do trabalho no Brasil.  

---

## 🛠️ Tecnologias Utilizadas
- **Linguagem:** Kotlin  
- **UI:** Jetpack Compose  
- **Arquitetura:** MVVM (Model-View-ViewModel)  
- **Navegação:** Jetpack Navigation Compose  
- **Persistência local:** Room Database  
- **Banco de Dados:** Oracle SQL e MongoDB  

---

## ⚙️ Funcionalidades Principais
1. Check-in de Humor  
2. Avaliação de Bem-Estar  
3. Dashboard de Humor  
4. Exercícios Terapêuticos  
5. Artigos Terapêuticos  
6. Suporte Emocional  

---

## 🚀 Potencial para Expansão
- Integração com **wearables** para coleta de dados biométricos  
- Notificações e lembretes personalizados  
- Expansão do banco de dados para armazenar resultados  
- Sistema de **recomendações com IA**  
- Funcionalidades sociais para **suporte entre usuários**  

---

## 🔄 Fluxo de Navegação
```
Check-in → Dashboard → Exercícios / Artigos / Suporte → Avaliação → Resultado → Recomendações
```

---

## 🎨 Estrutura Visual
- Visual **acolhedor** com ícones amigáveis  
- Cores **suaves** que transmitam calma  
- Navegação clara com botões grandes e textos curtos  
- Linguagem **empática e acessível** (com opções de acessibilidade)  

---

## 🗄️ Implementação Técnica e Banco de Dados
O banco de dados passou por diferentes etapas de desenvolvimento:

1. **CSV Inicial**  
   - Organização dos primeiros registros de humor, avaliações e exercícios.  
   - Base para testes iniciais.  

2. **Migração para Oracle SQL**  
   - Criação de tabelas normalizadas (usuários, check-ins, exercícios, artigos, suporte).  
   - Maior controle, consistência e escalabilidade.  

3. **Modelagem Relacional (DER)**  
   - Definição de chaves primárias e estrangeiras.  
   - Garantia de integridade referencial.  

4. **Modelagem Não Relacional (NoSQL – MongoDB)**  
   - Estrutura em documentos para registros dinâmicos.  
   - Flexibilidade para integração futura com **Big Data** e nuvem.  

---

## 📌 Como Executar o Projeto
### Pré-requisitos
- Android Studio **Arctic Fox ou superior**  
- JDK 17+  
- MongoDB ou Oracle XE configurado localmente  

### Passo a Passo
```bash
# Clonar o repositório
git clone https://github.com/seu-repo/sentimais.git

# Abrir no Android Studio
# Rodar em um emulador ou dispositivo físico
```

---

## 🧪 Testes
- Implementação planejada de testes unitários com **JUnit**  
- Testes de interface utilizando **Espresso**  

---

## 📜 Licença
Este projeto é acadêmico e não possui licença comercial até o momento.
