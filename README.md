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
%% CLIENTS
%% =========================================================
subgraph CLIENTS["Client Applications"]
  WEB["Consumer Web<br/>Next.js"]
  MOB["Consumer Mobile<br/>Expo / React Native"]
  DASH["Admin Dashboard<br/>Vue"]
end

%% =========================================================
%% EDGE
%% =========================================================
subgraph EDGE["Edge & Access Layer"]
  DNS["DNS"]
  CDN["CDN"]
  WAF["WAF / DDoS Protection"]
  INGRESS["Ingress / Load Balancer"]
end

WEB --> DNS
MOB --> DNS
DASH --> DNS
DNS --> CDN --> WAF --> INGRESS

%% =========================================================
%% APPLICATION
%% =========================================================
subgraph APP["Application Layer"]
  BFF["API / BFF Layer"]
  AUTH["Authentication & Authorization"]
end

INGRESS --> BFF
BFF --> AUTH

%% =========================================================
%% CORE SERVICES
%% =========================================================
subgraph SERVICES["Core Services"]
  CORE["Core API"]
  ADMINAPI["Admin API"]
  MSG["Realtime / Messaging Service"]
  MEDIA["Media Service"]
  WORKER["Background Worker"]
end

BFF --> CORE
BFF --> ADMINAPI
BFF --> MSG
BFF --> MEDIA

CORE --> WORKER
ADMINAPI --> WORKER
MEDIA --> WORKER
MSG --> WORKER

%% =========================================================
%% DATA
%% =========================================================
subgraph DATA["Data Layer"]
  MONGO["MongoDB"]
  POSTGRES["PostgreSQL"]
  REDIS["Redis"]
  S3["Object Storage"]
  MQ["RabbitMQ / Queue"]
end

CORE --> MONGO
CORE --> POSTGRES
CORE --> REDIS

ADMINAPI --> POSTGRES
ADMINAPI --> MONGO

MSG --> REDIS
MSG --> MONGO

MEDIA --> S3
MEDIA --> MONGO

WORKER --> MQ
CORE --> MQ
ADMINAPI --> MQ
MSG --> MQ
MEDIA --> MQ

WORKER --> MONGO
WORKER --> POSTGRES
WORKER --> REDIS
WORKER --> S3

%% =========================================================
%% PLATFORM
%% =========================================================
subgraph PLATFORM["Platform & Operations"]
  ECS["ECS / Fargate"]
  REG["Container Registry"]
  SECRET["Secrets Manager / Parameter Store"]
  LOG["Central Logging"]
  METRIC["Metrics / Monitoring"]
  ALERT["Alerting"]
end

REG --> ECS
ECS --> BFF
ECS --> AUTH
ECS --> CORE
ECS --> ADMINAPI
ECS --> MSG
ECS --> MEDIA
ECS --> WORKER

BFF --> LOG
CORE --> LOG
ADMINAPI --> LOG
MSG --> LOG
MEDIA --> LOG
WORKER --> LOG

BFF --> METRIC
CORE --> METRIC
ADMINAPI --> METRIC
MSG --> METRIC
MEDIA --> METRIC
WORKER --> METRIC

METRIC --> ALERT

AUTH --> SECRET
CORE --> SECRET
ADMINAPI --> SECRET
MEDIA --> SECRET
WORKER --> SECRET

%% =========================================================
%% CI/CD
%% =========================================================
subgraph CICD["CI / CD"]
  DEV["Developer Push"]
  GHA["GitHub Actions"]
  TEST["Lint / Test / Build"]
  SCAN["Image Scan"]
  DEPLOY["Deploy"]
end

DEV --> GHA --> TEST --> SCAN --> REG
REG --> DEPLOY --> ECS
```


---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:38bdf8,100:2563eb&height=150&section=footer"/>
</p>
