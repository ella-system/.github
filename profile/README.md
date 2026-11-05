# Ella

**Ella** é uma plataforma de saúde e telemedicina que conecta pacientes e médicos, com foco em agendamento, acompanhamento e jornada do paciente, apoiada por inteligência artificial.

---

## 🩺 Visão Geral

O Ella nasceu como um app mobile de telemedicina e vem evoluindo para um ecossistema completo, incluindo vínculo paciente-médico, pagamentos integrados, IA conversacional para triagem/atendimento e uma camada de dados/analytics para suportar decisões de negócio.

O roadmap do produto está organizado em três ondas (Validar → Crescer → Expandir), priorizando primeiro a estabilização e o modelo de negócio, depois engajamento/crescimento, e por fim expansão de plataforma e ecossistema (CRM, marketplace, novos modelos de receita).

---

## 📱 Aplicação

- **Mobile:** Flutter (iOS/Android)
- **Vínculo paciente-médico:** deep linking via QR Code
- **IA de atendimento:** triagem inicial de pacientes com Dialogflow (fase inicial do produto), com evolução planejada para a "Ella IA" usando Vertex AI
- **Deploy:** publicação nas lojas (App Store / Google Play)

---

## ⚙️ Backend

- **Framework:** Dart Frog
- **Autenticação:** Firebase Auth, com validação de token via `dart_firebase_admin`
- **Tratamento de erros:** `TaskEither` do pacote `fpdart` (programação funcional)
- **ORM (quando aplicável):** Drift, com `json_serializable` para serialização dos modelos de domínio
- **Testes de API:** Bruno como cliente HTTP

---

## 💳 Pagamentos

- **Stripe Hosted Checkout** para pagamentos internacionais/cartão
- **Pix** como meio de pagamento nacional
- Modelo de monetização evoluindo de pagamento avulso/assinatura (Onda 1) para meios adicionais como cupons e planos mensais (Onda 2)

---

## ☁️ Infraestrutura (Google Cloud Platform)

Ambientes: `ellaproject-495122` (produção/principal) e `ella-app-dev` (desenvolvimento)

| Serviço | Uso |
|---|---|
| Cloud Run | Hospedagem do backend |
| Cloud SQL (PostgreSQL) | Banco de dados relacional — região `northamerica-south1` |
| Firestore | Dados NoSQL / tempo real |
| Cloud Functions | Funções serverless |
| Firebase Storage | Armazenamento de arquivos/imagens |
| Vertex AI | `gemini-2.5-flash-lite` + `text-multilingual-embedding-002` para IA e busca semântica (RAG) |

---

## 🔒 Segurança e Compliance

- Aderência à LGPD (exclusão de dados, retenção/expurgo de documentos)
- Auditoria e gestão de documentos planejadas para a Onda 3

---

## 📂 Repositórios

| Repositório | Descrição |
|---|---|
| `ella-app` | Aplicativo Flutter (mobile) |
| `ella-backend` | API Dart Frog |
| `ella-infra` | Infraestrutura GCP (IaC) |

*(ajuste os nomes acima conforme os repositórios reais da organização)*

---

## 📄 Licença

Uso interno / proprietário — *(ajustar conforme a licença real do projeto)*
