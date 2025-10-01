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

# 📘 Documentação do Sistema

## Visão Geral
O **SentiMais** é um aplicativo Android dedicado ao bem-estar mental e emocional.  
Ele permite o **monitoramento e acompanhamento das emoções** ao longo do tempo, além de oferecer avaliações, artigos e exercícios para promoção da saúde mental.

## Proposta
O sistema busca funcionar como um **assistente pessoal de bem-estar emocional**, permitindo que o usuário:
1. Registre suas emoções diárias (check-ins)  
2. Realize avaliações psicossociais periódicas  
3. Acesse conteúdos sobre saúde mental  
4. Pratique exercícios para redução de estresse e ansiedade  
5. Visualize progresso e tendências emocionais ao longo do tempo  

## Arquitetura do Sistema
- **Linguagem:** Kotlin  
- **UI:** Jetpack Compose (declarativa)  
- **Arquitetura:** MVVM (Model-View-ViewModel)  
- **Navegação:** Jetpack Navigation Compose  
- **Persistência:** Room Database (SQLite)  

## Principais Componentes
1. **Sistema de Check-in Emocional** → Registro de emoções + notas opcionais  
2. **Avaliação de Bem-estar** → Questionários com escala de frequência e resultados detalhados  
3. **Seção de Apoio** → Artigos, exercícios e opções de suporte  
4. **Sistema de Navegação** → Tabs principais e navegação interna com Jetpack Compose  

## Fluxo de Funcionamento
1. Entrada no app → saudação e pergunta inicial  
2. Check-in → emoção + nota → registro no banco  
3. Avaliação → questionário → resultado + recomendações  
4. Apoio → artigos, exercícios e suporte adicional  
5. Progresso → histórico de check-ins e avaliações com gráficos  

## Telas Principais
- **MainActivity** → Tabs principais e navegação  
- **CheckInScreen** → Seleção de emoções + histórico  
- **AssessmentScreen** → Questionário estruturado  
- **ResultScreen** → Resultados e recomendações  
- **ApoioScreen** → Artigos e exercícios  
- **ArticlesScreen** → Lista e detalhes de artigos  

## Considerações Futuras
- Integração com wearables  
- Notificações e lembretes  
- Expansão do banco de dados para avaliações  
- Sistema de recomendações com IA  
- Funcionalidades sociais  

---

# 🗃️ Estrutura de Banco de Dados

## 💻 Tecnologia Utilizada
O aplicativo utiliza o **Room** como ORM sobre **SQLite**, garantindo abstração e segurança nas operações.

## 📌 Entidades

### CheckIn
- **Arquivo:** `CheckIn.kt`  
- **Tabela:** `checkin`  

**Campos:**
- `id` (Long) → chave primária  
- `emotion` (String) → emoção do usuário  
- `date` (Long) → timestamp  
- `note` (String, nullable) → observação opcional  

---

## 📂 DAOs (Data Access Objects)

### CheckInDao
- **Arquivo:** `CheckInDao.kt`  

**Métodos:**
- `insert(checkIn: CheckIn): Long` → Insere um novo check-in  
- `getAll(): List<CheckIn>` → Lista todos os check-ins  
- `getById(id: Long): CheckIn?` → Busca por ID  

---

## ⚙️ Configuração do Banco
- **Arquivo:** `AppDatabase.kt`  
- Versão: **1**  
- Entidades: `[CheckIn]`  
- DAO: `CheckInDao`  

---

## 📑 Dados Mock (Não Persistentes)
- **MockArticles.kt** → artigos pré-definidos com id, título, descrição, categoria, tempo de leitura e URL.  
- Usados em memória, não persistidos em banco.  

---

## 🔗 Relacionamentos
- Estrutura atual simples (apenas `CheckIn`)  
- Preparado para expansão futura  

---

## 📝 Observações
1. Estrutura atual foca em **registro e acompanhamento de emoções**  
2. Avaliações psicossociais ainda não são persistidas no banco local  
3. Fácil expansão para novas entidades  

---

# 📄 Modelagem NoSQL (Prisma + MongoDB)

O SentiMais também possui uma **modelagem não relacional** baseada em **MongoDB**, gerenciada com **Prisma ORM**.

## 🔧 Configuração
- ORM: Prisma Client (`prisma-client-js`)  
- Banco: MongoDB  
- Arquivo: `prisma/schema.prisma`  

Conexão definida via variável de ambiente:
```env
DATABASE_URL="mongodb+srv://usuario:senha@cluster.mongodb.net/sentimais"
```

## 📌 Principais Entidades
- **User** → informações do usuário, check-ins, avaliações e pedidos de suporte  
- **CheckIn** → registros de humor/emocionais (relacionado a User)  
- **Article** → artigos informativos (com tags e tempo de leitura)  
- **Exercise** → exercícios práticos  
- **AssessmentTemplate / Question / Submission / Response** → estrutura de avaliações psicossociais  
- **SupportRequest** → pedidos de contato/apoio com status de acompanhamento  

## 🎭 Enums Utilizados
- **Emotion** → HAPPY, SAD, CALM, ANXIOUS, STRESSED, ANGRY, NEUTRAL, OTHER  
- **ArticleTag** → Burnout, Anxiety, Stress, Wellness, Other  
- **SupportRequestType** → CONTACT, SUPPORT  
- **SupportRequestStatus** → PENDING, IN_PROGRESS, RESOLVED, CANCELED  

## ▶️ Uso no Código
Exemplo de criação de usuário e check-in:
```ts
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

const user = await prisma.user.create({
  data: { email: "teste@email.com", name: "Andriel" }
});

await prisma.checkIn.create({
  data: {
    userId: user.id,
    emotion: "HAPPY",
    date: new Date(),
    note: "Dia incrível!"
  }
});
```

## 📝 Observações
- Prisma gera tipagem automática para consultas seguras  
- Relacionamentos definidos no schema (`@relation`) permitem queries encadeadas  
- Modelagem pronta para expansão (IA, notificações, histórico detalhado)  
