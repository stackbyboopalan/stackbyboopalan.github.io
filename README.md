<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0e1a,50:2563eb,100:38bdf8&height=180&section=header&text=Boopalan%20Pichandi&fontSize=44&fontColor=ffffff&fontAlignY=36&desc=Full-Stack%20FinTech%20Architect%20%C2%B7%20AI%20Agent%20Developer&descAlignY=58&descSize=16" alt="Boopalan Pichandi banner" width="100%"/>

<a href="https://stackbyboopalan.github.io">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2600&pause=900&color=38BDF8&center=true&vCenter=true&width=560&lines=Full-Stack+FinTech+Architect;AI+Agent+Developer;MCP+Algo-Trading+Builder;Secure+Systems+Designer;Platform+Architect+%40+RhoFi" alt="Typing roles"/>
</a>

[![Portfolio](https://img.shields.io/badge/Portfolio-stackbyboopalan.github.io-2563eb?style=for-the-badge&logo=googlechrome&logoColor=white)](https://stackbyboopalan.github.io)
[![RhoFi](https://img.shields.io/badge/Building-RhoFi-10b981?style=for-the-badge&logo=bitcoin-cash&logoColor=white)](https://rhofi.com)
[![MCP](https://img.shields.io/badge/Now%20building-MCP%20Algo%20Trading-f59e0b?style=for-the-badge&logo=probot&logoColor=white)](https://stackbyboopalan.github.io/#mcp)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/boopalanpichandi)
[![Resume](https://img.shields.io/badge/Resume-PDF-f59e0b?style=for-the-badge&logo=readdotcv&logoColor=white)](https://stackbyboopalan.github.io/assets/Boopalan_Pichandi_Resume.pdf)
[![Email](https://img.shields.io/badge/Email-proton.me-6d4aff?style=for-the-badge&logo=protonmail&logoColor=white)](mailto:boopalanpichandi@proton.me)

</div>

---

## 👋 About me

I'm **Boopalan Pichandi**, a **Full-Stack FinTech Architect** and **AI Agent Developer** based in Bengaluru with **5+ years** building regulated financial platforms. I design the architecture, implement the security and ship the product end-to-end, from React UI to Kubernetes, and the AI agents that turn market research into answers.

## 🏦 Currently: Architecting [RhoFi](https://rhofi.com)

**RhoFi Financial Technologies** · *Full-Stack FinTech Architect & AI Agent Developer* · Mar 2024 – Present

RhoFi is a **SEBI-registered research analyst platform** (`INH000025090`) for **stocks, F&O, mutual funds, IPOs and bonds**, with backtested strategies, AI-driven screeners and real-time market insights.

- 🏗️ **Architecture design**: event-driven microservices on AWS & GCP, Kafka / Pub/Sub market-data pipelines, PostgreSQL (RDS) + Redis, Kubernetes with zero-downtime releases
- 🛡️ **Security implementation**: OAuth2/JWT, RBAC, encryption in transit & at rest, managed secrets, WAF & rate limiting, audit logging, SAST and dependency scans in CI
- 💳 **Secure payments**: Razorpay, PhonePe and PayU behind one payment service, with server-side orders, signature/hash verification, verified idempotent webhooks and reconciliation
- 🚢 **End-to-end delivery**: React.js product UI, Python/Node services, Zerodha/Kite broker integration, CI/CD with **60% shorter** deployment cycles
- 🤖 **AI agents**: LLM research assistants with scoped read-only tools, retrieval and compliance guardrails

## 📡 Now building: MCP algo-trading agent *(in progress)*

An **MCP (Model Context Protocol) server** for algorithmic trading. It gives an AI agent typed, permissioned tools to read trade signals, validate entries and place orders through the broker API. Every order passes a risk gate that runs in code, outside the model.

| MCP tool | What it does |
|---|---|
| `get_signals` | Strategy signals per instrument and timeframe |
| `get_market_data` | Live quotes, OHLC candles and indicators |
| `validate_entry` | Confirms entry price, trend and volume before acting |
| `check_risk` | Position size, max loss and exposure limits |
| `place_order` | Order with stop-loss and target via Zerodha Kite (needs explicit permission) |
| `get_positions` | Open positions, P&L and order status |

```mermaid
flowchart LR
    A["Signal intake<br/>strategies · indicators"] --> B["AI agent<br/>via MCP tools"]
    B --> C["Entry validation<br/>price · trend · volume"]
    C --> D["Risk gate (code)<br/>size · max loss · kill switch"]
    D --> E["Place & track<br/>broker API · SL / target · audit log"]
```

Safety: separate read and order tools, server-side risk limits and a kill switch, paper-trading mode before live capital, broker tokens in a vault, and a full audit log.

## 🏗️ Platform architecture

```mermaid
flowchart TB
    C["Clients<br/>React web · React Native · WhatsApp / push / email · AI chat"]
    E["Edge<br/>CDN · WAF · TLS · rate limiting"]
    G["API gateway<br/>OAuth2 / JWT · RBAC · input validation"]
    subgraph K["Kubernetes services (AWS + GCP)"]
      S1[Research & signals]
      S2[Portfolio]
      S3[Backtesting]
      S4[MF · IPO · Bonds]
      S5[AI agent service]
      S6[Payments · Razorpay / PhonePe / PayU]
      S7[Notifications]
      S8[Broker API · Kite]
    end
    B["Event bus<br/>Apache Kafka · GCP Pub/Sub · Apache Beam"]
    D[("Data<br/>PostgreSQL RDS · Redis · Elasticsearch · S3 · vector index")]
    O["Observability<br/>ELK · Grafana · Prometheus · audit logs"]
    P["DevSecOps<br/>GitHub Actions · SonarQube · Docker · Terraform"]

    C --> E --> G --> K
    K <--> B
    B --> D
    K --> D
    K -.-> O
    P -.-> K
```

## 🛡️ Secure system design

| Layer | Controls I implement |
|---|---|
| Identity | OAuth2/JWT, short-lived tokens with refresh rotation, role-based access |
| Data | TLS in transit; databases, backups and storage encrypted at rest |
| Secrets | Managed vault, runtime injection, rotation, secret scanning |
| Edge | WAF rules, rate limiting, request validation |
| Pipeline | SAST, dependency and container scans gating every merge |
| Compliance | Immutable audit trails and centralized logging that support SEBI obligations |
| AI | Read-only tools, scoped data access, prompt-injection filtering, disclaimers |

## 💳 Secure payment integrations

<p align="center">
  <img src="https://stackbyboopalan.github.io/assets/logos/razorpay.png" height="32" alt="Razorpay"/>
  &nbsp;&nbsp;&nbsp;
  <img src="https://stackbyboopalan.github.io/assets/logos/phonepe.png" height="40" alt="PhonePe"/>
  &nbsp;&nbsp;&nbsp;
  <img src="https://stackbyboopalan.github.io/assets/logos/payu.png" height="40" alt="PayU"/>
</p>

| Gateway | How I integrated it securely |
|---|---|
| **Razorpay** | Orders created server-side, checkout signature verified with HMAC-SHA256, webhooks verified via `X-Razorpay-Signature`, subscriptions and refunds |
| **PhonePe** | Server-to-server initiation, SHA-256 checksum on signed requests, callbacks verified, final state from the status-check API |
| **PayU** | SHA-512 request hash generated server-side, reverse-hash check on every response, verify-payment API for reconciliation |

```mermaid
flowchart LR
    A["Create order<br/>server-side · idempotency key"] --> B["Hosted checkout<br/>no card data on our servers"]
    B --> C["Verify<br/>signature / hash · amount"]
    C --> D["Webhook → Kafka<br/>idempotent processing"]
    D --> E["Reconcile & activate<br/>status API · audit log"]
```

Keys and salts live in a secrets vault, every transaction has an audit trail, and gateways can fail over without changing the product.

## 🤖 AI agent development

`intent detection → retrieval (RAG) → tool calls → guardrails → grounded response`

- Investor-facing research agent for portfolios, market mood and strategies
- LLM automation that speeds up analyst research workflows
- 📡 Now building an MCP server that exposes trading tools to an agent ([see above](#-now-building-mcp-algo-trading-agent-in-progress))
- 💬 **Try the live agent** on my portfolio: **[stackbyboopalan.github.io/#agent](https://stackbyboopalan.github.io/#agent)**

## 📈 Impact

| 60% | 50% | 99.9% | 40% | 35% |
|:---:|:---:|:---:|:---:|:---:|
| shorter deploy cycles (RhoFi) | faster releases (HawkMonk) | uptime SLA | lower MTTR | faster app responses |

## 🧭 Experience

- **RhoFi Financial Technologies**: Full-Stack FinTech Architect & AI Agent Developer *(Mar 2024 – Present)*
- **HawkMonk FinTech**: DevSecOps Engineer *(Nov 2022 – Feb 2024)*
- **HawkMonk FinTech**: Full Stack Developer *(May 2021 – Nov 2022)*
- 🎓 MCA, College of Engineering Guindy (Anna University) · B.Sc. Mathematics, Thiruvalluvar University

---

## 💻 Tech stack

**Architecture & Security**
![Microservices](https://img.shields.io/badge/Microservices-0a0e1a?style=for-the-badge&logo=serverless&logoColor=38bdf8)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)
![OAuth2](https://img.shields.io/badge/OAuth2-EB5424?style=for-the-badge&logo=auth0&logoColor=white)
![SonarQube](https://img.shields.io/badge/SonarQube-black?style=for-the-badge&logo=sonarqube&logoColor=4E9BCD)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)

**Payments**
![Razorpay](https://img.shields.io/badge/Razorpay-0C2451?style=for-the-badge&logo=razorpay&logoColor=3395FF)
![PhonePe](https://img.shields.io/badge/PhonePe-5F259F?style=for-the-badge&logo=phonepe&logoColor=white)
![PayU](https://img.shields.io/badge/PayU-A6C307?style=for-the-badge&logoColor=white)
![UPI](https://img.shields.io/badge/UPI-097939?style=for-the-badge&logo=googlepay&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)

**Backend**
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![GraphQL](https://img.shields.io/badge/-GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)

**Cloud & DevSecOps**
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![GitLab CI](https://img.shields.io/badge/gitlab%20CI-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)

**Data, Streaming & Observability**
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![ElasticSearch](https://img.shields.io/badge/-ElasticSearch-005571?style=for-the-badge&logo=elasticsearch)
![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)

**AI / ML**
![LLM Agents](https://img.shields.io/badge/LLM%20Agents-a78bfa?style=for-the-badge&logo=openaigym&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-Model%20Context%20Protocol-0a0e1a?style=for-the-badge&logo=probot&logoColor=white)
![Kite Connect](https://img.shields.io/badge/Kite%20Connect-387ED1?style=for-the-badge&logo=zerodha&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

---

## 📊 GitHub activity

<div align="center">

<img src="assets/github-activity.svg" width="100%" alt="GitHub activity: 98% contribution rate, active 51 of 52 weeks, RhoFi organization"/>

<sub>Most of my work is in private repositories of the RhoFi organization. My contribution graph counts that work without showing any code, repository names or details. Only my public repositories are visible here.</sub>

</div>

---

<div align="center">

[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://discord.gg/J2NUrnDt)
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/boopalanpichandi)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/boopalanpichandi)
[![Medium](https://img.shields.io/badge/Medium-12100E?logo=medium&logoColor=white)](https://medium.com/@boopalanpichandi)
[![Reddit](https://img.shields.io/badge/Reddit-%23FF4500.svg?logo=Reddit&logoColor=white)](https://reddit.com/user/boopalan-pichandi)

[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/boopalanpichandi)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:38bdf8,50:2563eb,100:0a0e1a&height=100&section=footer" width="100%" alt=""/>

</div>
