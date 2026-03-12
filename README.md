<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Inter&weight=600&size=34&duration=2500&pause=500&color=38BDF8&center=true&vCenter=true&width=800&lines=Hi%2C+I'm+Canberk+Beren" />
</p>

<p align="center">
  <a href="https://tr.linkedin.com/in/canberk-beren" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:canberkberen@icloud.com">
    <img src="https://img.shields.io/badge/Email-111111?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=highpriv&style=for-the-badge&color=38bdf8" />
</p>

---

## 🧠 About Me

Software Developer focused on building scalable, cloud-native, distributed systems.

**Focus areas**
- Product engineering  
- System architecture  
- Distributed systems  
- Event-driven design  
- Cloud-native infrastructure  

**Core stack**
- Backend: Node.js, Express, GraphQL, RabbitMQ  
- Frontend: React, Next.js  
- Mobile: React Native, Expo  
- Cloud: AWS, Docker, Nginx  

🌍 Open to global opportunities.

---

## ⚡ Tech Arsenal

<p align="center">
  <img src="https://skillicons.dev/icons?i=react,nextjs,ts,js,html,css,tailwind,redux" />
  <br/>
  <img src="https://skillicons.dev/icons?i=expo,nodejs,express,graphql,rabbitmq" />
  <br/>
  <img src="https://skillicons.dev/icons?i=aws,docker,nginx,linux,redis,postgres,mysql,mongodb" />
</p>

---

## 🏗 System Architecture Focus

<p align="center">
  <img src="https://img.shields.io/badge/Microfrontend-111111?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Monorepo-111111?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Event_Driven-111111?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Distributed_Systems-111111?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/System_Design-111111?style=for-the-badge"/>
</p>

---

## 🏆 Featured Projects

- 🧠 Scalable Social Media Platform  
  Web + Mobile + Realtime + Event-driven architecture  
  React • React Native • GraphQL • RabbitMQ • AWS  

- ⚡ Event-Driven Backend Architecture  
  Node.js • GraphQL • RabbitMQ • Redis • Docker  

- 🏗 Microfrontend Monorepo System  
  Next.js • Module Federation • Nx  

(Pinned repositories below 👇)

---

## 📊 Metrics

<p align="center">
  <img height="170" src="https://github-readme-streak-stats.herokuapp.com/?user=highpriv&theme=transparent&hide_border=true" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/highpriv/highpriv/output/github-snake-dark.svg" />
</p>

---

## 🧬 Engineering Philosophy

“Clean code is not written by following rules.  
Clean code is written by caring.”

- System-first thinking  
- Scalable foundations  
- Product-driven engineering  
- Performance obsession  
- Automation mindset  

---

## 🤝 Connect

- LinkedIn → https://tr.linkedin.com/in/canberk-beren  
- Mail → canberkberen@icloud.com  

## Wuubi - Project Architecture Mermaid

- Full Preview → https://mermaid.ai/d/62af7a04-b1b3-4e06-8f69-aea59d72c61a

```mermaid
%%{init: {
  "theme": "base",
  "themeVariables": {
    "background": "#ffffff",
    "primaryColor": "#FFF7E6",
    "primaryTextColor": "#172033",
    "primaryBorderColor": "#F59E0B",
    "lineColor": "#6B7280",
    "secondaryColor": "#ECFEFF",
    "secondaryTextColor": "#0F172A",
    "secondaryBorderColor": "#14B8A6",
    "tertiaryColor": "#F8FAFC",
    "tertiaryBorderColor": "#CBD5E1",
    "fontFamily": "Inter, Segoe UI, Arial"
  }
}}%%

flowchart TB

%% =========================================================
%% CLIENT CHANNELS
%% =========================================================
subgraph CLIENTS["Client Channels"]
  WEB["Consumer Web<br/>Next.js"]
  MOB["Consumer Mobile<br/>Expo / React Native"]
  DASH["Admin Dashboard<br/>Vue"]
  OPS["Ops / Moderation Console"]
end

%% =========================================================
%% GLOBAL EDGE
%% =========================================================
subgraph EDGE["Global Edge & Delivery"]
  DNS["Global DNS / Traffic Manager"]
  CDN["CDN / Edge Cache"]
  WAF["WAF / Bot Protection"]
  DDOS["DDoS Protection"]
  TLS["TLS Termination"]
  RL["Global Rate Limiting"]
  ROUTER["Geo / Regional Router"]
end

WEB --> DNS
MOB --> DNS
DASH --> DNS
OPS --> DNS

DNS --> CDN --> WAF --> DDOS --> TLS --> RL --> ROUTER

%% =========================================================
%% ENTRY SPLIT
%% =========================================================
subgraph ENTRY["Environment Routing"]
  TESTIN["Private Test Ingress<br/>VPN Only / Noindex"]
  PRODIN["Public Production Ingress"]
end

ROUTER --> TESTIN
ROUTER --> PRODIN

%% =========================================================
%% PRIMARY REGION
%% =========================================================
subgraph PRIMARY["Primary Region"]
  
  subgraph ING["Ingress Layer"]
    ALB["ALB / API Gateway / Ingress"]
    BFF["Unified API / BFF"]
  end

  subgraph APPS["Application Services"]
    UI["Web UI Service"]
    MBFF["Mobile BFF"]
    CORE["Core API"]
    DAPI["Dashboard API"]
    ADMIN["Admin / Moderation API"]

    AUTH["Auth Service"]
    USER["User Profile Service"]
    CONTENT["Content Service"]
    GROUP["Group Service"]
    STORY["Story Service"]
    MSG["Messaging Service"]
    NOTIF["Notification Service"]
    MEDIA["Media Service"]
    SEARCH["Search API"]
    EXPLORE["Explore Feed API"]
  end

  subgraph RT["Realtime Layer"]
    SOCK["Socket Gateway"]
    PRES["Presence Service"]
    ROOM["Room Router"]
    DELIV["Delivery Tracker"]
  end

  subgraph EVENT["Event Mesh & Async Workers"]
    EX["RabbitMQ Topic Exchange"]
    WMSG["Message Worker"]
    WNOT["Notification Worker"]
    WST["Story Worker"]
    WFEED["Feed Projection Worker"]
    WMEDIA["Media Worker"]
    WAUD["Audit Worker"]
    WINDEX["Index Worker"]
  end

  subgraph PIPE["Content & Policy Pipeline"]
    UP["Upload Endpoint"]
    SCAN["Malware / File Validation"]
    TRANS["Media Transform"]
    THUMB["Thumbnail / Preview"]
    META["Metadata Extractor"]
    PUB["Publish Coordinator"]

    POLICY["Policy Engine"]
    TXT["Text Classification"]
    IMG["Media Moderation"]
    SPAM["Spam / Abuse Detection"]
    TRUST["Trust / Risk Score"]
    REVIEW["Manual Review Queue"]
    ENF["Enforcement Actions"]
  end

  subgraph DISC["Discovery, Search & Ranking"]
    BEHAV["Behavior Events"]
    FEAT["Feature Pipeline"]
    FS["Feature Store"]
    TIDX["Text Index"]
    VIDX["Vector Index"]
    CAND["Candidate Generation"]
    RULE["Eligibility / Filtering"]
    RANK["Ranking Service"]
    FRESH["Freshness / Diversity Adjuster"]
  end

  subgraph DATA["Operational Data Stores"]
    MONGO["MongoDB Cluster"]
    PG["PostgreSQL Cluster"]
    REDIS["Redis Cache"]
    S3["Object Storage"]
    SESS["Session / Token Store"]
    AUDIT["Audit Log Store"]
  end

  subgraph ANALYTICS["Analytics & Intelligence"]
    CDC["CDC / Change Streams"]
    LAKE["Data Lake"]
    WH["Warehouse / Lakehouse"]
    BI["BI / Product Analytics"]
    ML["Batch Feature / ML Jobs"]
    REP["Operational Reporting"]
  end

  subgraph OBS["Observability, Security & Platform"]
    OTEL["OpenTelemetry"]
    LOG["Central Logging"]
    MET["Metrics Platform"]
    TRACE["Distributed Tracing"]
    ALERT["Alerting / On-call"]
    SIEM["Security SIEM"]
    SECRET["Secrets Manager"]
    IAM["Service Identity / IAM"]
    CONF["Config / Parameter Store"]
  end

  subgraph RUN["Runtime Platform"]
    REG["Container Registry"]
    ECS["ECS / Fargate Runtime"]
    SMOKE["Smoke / Synthetic Tests"]
    GATE["Release Gate / Rollback Control"]
  end

  %% entry
  ALB --> BFF

  %% edge to app
  BFF --> UI
  BFF --> MBFF
  BFF --> CORE
  BFF --> DAPI
  BFF --> ADMIN

  %% orchestration
  MBFF --> CORE
  CORE --> AUTH
  CORE --> USER
  CORE --> CONTENT
  CORE --> GROUP
  CORE --> STORY
  CORE --> MSG
  CORE --> NOTIF
  CORE --> MEDIA
  CORE --> SEARCH
  CORE --> EXPLORE
  CORE --> SOCK

  %% dashboard/admin
  DAPI --> MONGO
  DAPI --> PG
  DAPI --> S3
  ADMIN --> MONGO
  ADMIN --> PG
  ADMIN --> AUDIT

  %% realtime
  SOCK --> PRES
  SOCK --> ROOM
  SOCK --> DELIV
  MSG --> SOCK
  NOTIF --> SOCK

  %% operational data
  AUTH --> SESS
  AUTH --> REDIS
  USER --> MONGO
  CONTENT --> MONGO
  GROUP --> MONGO
  STORY --> MONGO
  MSG --> MONGO
  MSG --> REDIS
  NOTIF --> MONGO
  NOTIF --> REDIS
  MEDIA --> S3
  MEDIA --> MONGO
  SEARCH --> TIDX
  SEARCH --> VIDX
  EXPLORE --> RANK
  EXPLORE --> REDIS

  %% event publishing
  CORE --> EX
  MSG --> EX
  STORY --> EX
  NOTIF --> EX
  MEDIA --> EX
  SOCK --> EX
  ADMIN --> EX

  %% workers
  EX --> WMSG
  EX --> WNOT
  EX --> WST
  EX --> WFEED
  EX --> WMEDIA
  EX --> WAUD
  EX --> WINDEX

  WMSG --> MONGO
  WMSG --> DELIV
  WMSG --> SOCK

  WNOT --> MONGO
  WNOT --> REDIS
  WNOT --> SOCK

  WST --> MONGO
  WST --> REDIS

  WFEED --> REDIS
  WFEED --> BEHAV

  WMEDIA --> TRANS
  WMEDIA --> THUMB
  WMEDIA --> META

  WAUD --> AUDIT
  WAUD --> SIEM

  WINDEX --> TIDX
  WINDEX --> VIDX

  %% content pipeline
  MEDIA --> UP --> SCAN --> TRANS --> THUMB --> META --> PUB
  PUB --> S3
  PUB --> MONGO
  PUB --> POLICY

  %% policy pipeline
  CONTENT --> POLICY
  STORY --> POLICY
  MSG --> POLICY
  POLICY --> TXT
  POLICY --> IMG
  POLICY --> SPAM
  POLICY --> TRUST
  TXT --> REVIEW
  IMG --> REVIEW
  SPAM --> REVIEW
  TRUST --> ENF
  REVIEW --> ENF
  ENF --> MONGO
  ENF --> AUDIT
  ENF --> EX

  %% ranking
  USER --> BEHAV
  CONTENT --> BEHAV
  GROUP --> BEHAV
  STORY --> BEHAV
  MSG --> BEHAV
  BEHAV --> FEAT --> FS
  MONGO --> TIDX
  MONGO --> VIDX
  FS --> CAND
  TIDX --> CAND
  VIDX --> CAND
  CAND --> RULE --> RANK --> FRESH --> EXPLORE

  %% analytics
  MONGO --> CDC
  PG --> CDC
  AUDIT --> CDC
  CDC --> LAKE --> WH
  WH --> BI
  WH --> ML
  WH --> REP
  ML --> FS

  %% platform / runtime
  REG --> ECS
  ECS --> ALB
  ECS --> UI
  ECS --> MBFF
  ECS --> CORE
  ECS --> DAPI
  ECS --> ADMIN
  ECS --> SOCK
  ECS --> WMSG
  ECS --> WNOT
  ECS --> WST
  ECS --> WFEED
  ECS --> WMEDIA
  ECS --> WAUD
  ECS --> WINDEX
  ECS --> SMOKE --> GATE

  %% observability
  UI --> OTEL
  MBFF --> OTEL
  CORE --> OTEL
  DAPI --> OTEL
  SOCK --> OTEL
  WMSG --> OTEL
  WNOT --> OTEL
  WMEDIA --> OTEL
  OTEL --> LOG
  OTEL --> MET
  OTEL --> TRACE
  MET --> ALERT
  TRACE --> ALERT
  LOG --> SIEM

  %% security dependencies
  CORE --> SECRET
  DAPI --> SECRET
  ADMIN --> SECRET
  ECS --> IAM
  ECS --> CONF
  AUTH --> IAM
end

%% =========================================================
%% SECONDARY REGION
%% =========================================================
subgraph SECONDARY["Secondary Region / Disaster Recovery"]
  ALB2["Regional Ingress"]
  CORE2["Core Services Replica"]
  SOCK2["Realtime Replica"]
  MONGO2["MongoDB Replica"]
  PG2["PostgreSQL Replica"]
  REDIS2["Redis Replica"]
  S32["Object Storage Replica"]
  EX2["Regional Event Broker"]
  FAIL["Failover / Recovery Control"]

  ALB2 --> CORE2
  CORE2 --> SOCK2
  CORE2 --> MONGO2
  CORE2 --> PG2
  CORE2 --> REDIS2
  CORE2 --> S32
  CORE2 --> EX2
  FAIL --> ALB2
end

%% =========================================================
%% TEST ENVIRONMENT
%% =========================================================
subgraph TEST["Test Environment"]
  TING["Test Ingress"]
  TAPP["Test Services"]
  TDB["Test Datastores"]
end

TESTIN --> TING --> TAPP --> TDB

%% =========================================================
%% CI/CD
%% =========================================================
subgraph CICD["CI / CD & Release Management"]
  DEV["Developer Push"]
  GHA["GitHub Actions"]
  BUILD["Build / Lint / Typecheck / Test"]
  IMGSCAN["Container Build + Security Scan"]
  DEPLOY["Deployment Orchestrator"]
  APPROVE["Manual Production Approval"]
  ROLL["Automatic Rollback Policy"]
end

DEV --> GHA --> BUILD --> IMGSCAN --> REG
REG --> DEPLOY --> APPROVE --> ECS
GATE --> ROLL

%% =========================================================
%% REGION LINKS
%% =========================================================
PRODIN --> ALB
PRODIN --> ALB2

MONGO --> MONGO2
PG --> PG2
REDIS --> REDIS2
S3 --> S32
EX --> EX2
ALERT --> FAIL
```


---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:38bdf8,100:2563eb&height=150&section=footer"/>
</p>
