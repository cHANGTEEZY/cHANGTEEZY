<div align="center">

# Sushank Gurung

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=2800&pause=900&color=22D3EE&center=true&vCenter=true&width=680&lines=Architecting+scalable+systems;Building+interfaces+that+feel+fast;Event-driven+backends+%26+APIs;PostgreSQL+performance;Cross-platform+apps+with+Expo" alt="Typing headline" />

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/sushank-gurung)
[![Website](https://img.shields.io/badge/Website-0f172a?style=for-the-badge&logo=vercel&logoColor=white)](https://sushankgurung.com)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vbee-studio@sushankgurung.com)
[![Studio](https://img.shields.io/badge/VBEE_Studio-14b8a6?style=for-the-badge)](https://vbee.studio)

<img src="https://komarev.com/ghpvc/?username=cHANGTEEZY&label=Profile%20views&color=22d3ee&style=for-the-badge" alt="Profile views" />

</div>

<p align="center">
  <img src="./assets/divider.svg" width="100%" alt="" />
</p>

## About

<table>
  <tr>
    <td width="62%" valign="top">
      Full-stack developer at <a href="https://vbee.studio"><strong>VBEE Studio</strong></a>, based in Lalitpur, Nepal. I build scalable systems and thoughtful interfaces — event-driven backends, data-intensive apps, and UIs that feel fast and intentional.
      <br /><br />
      Currently focused on backend architecture, PostgreSQL optimization, and cross-platform mobile with React Native and Expo.
      <br /><br />
      <table>
        <tr>
          <td><strong>Role</strong></td>
          <td>Full-stack · VBEE Studio</td>
        </tr>
        <tr>
          <td><strong>Location</strong></td>
          <td>Lalitpur, Nepal</td>
        </tr>
        <tr>
          <td><strong>Learning</strong></td>
          <td>Event-driven systems, backend architecture</td>
        </tr>
        <tr>
          <td><strong>Interests</strong></td>
          <td>Data-intensive apps, podcasts, performance</td>
        </tr>
      </table>
    </td>
    <td width="38%" align="center" valign="middle">
      <img src="./assets/coding.gif" width="280" alt="Developer at a dual-monitor desk" />
    </td>
  </tr>
</table>

<p align="center">
  <img src="./assets/divider.svg" width="100%" alt="" />
</p>

## Stack

How a product is wired end to end — clients at the edge, typed APIs in the middle, and a data plane that can take load.

```mermaid
flowchart TB
  subgraph clients["Client layer"]
    WEB["Next.js / TanStack Start<br>TanStack Query · Zustand"]
    MOB["Expo / React Native"]
    ADMIN["Admin / internal tools"]
  end

  subgraph edge["Edge and ingress"]
    CDN["CDN · Vercel Edge<br>TLS · cache · WAF"]
    PROXY["Caddy / Nginx<br>load balancer"]
  end

  subgraph identity["Identity"]
    AUTH["Sessions · JWT · OAuth<br>Firebase / Supabase Auth"]
    RL["Rate limits · API keys"]
  end

  subgraph app["Application"]
    GW["API gateway"]
    BFF["tRPC BFF"]
    REST["Hono · NestJS · Fastify"]
    RT["Convex / WebSockets"]
    WORK["Workers · cron · queues"]
    EVT["Event bus / pub-sub"]
  end

  subgraph data["Data plane"]
    ORM["Prisma / Drizzle"]
    PG[("PostgreSQL primary")]
    REPL[("Read replica")]
    REDIS[("Redis<br>cache · sessions · jobs")]
    BLOB["Object storage"]
  end

  subgraph platform["Platform"]
    CI["GitHub Actions"]
    DOCKER["Docker"]
    CLOUD["AWS · GCP · Vercel<br>DigitalOcean · Hetzner"]
    OBS["Logs · metrics · traces"]
  end

  WEB --> CDN
  MOB --> CDN
  ADMIN --> CDN
  CDN --> PROXY --> GW
  GW --> AUTH
  AUTH --> RL
  RL --> BFF
  RL --> REST
  RL --> RT
  BFF --> ORM
  REST --> ORM
  REST --> EVT
  BFF --> EVT
  EVT --> WORK
  RT --> REDIS
  ORM --> PG
  PG --> REPL
  BFF --> REDIS
  REST --> REDIS
  WORK --> REDIS
  WORK --> PG
  REST --> BLOB
  CI --> DOCKER --> CLOUD
  REST -.-> OBS
  WORK -.-> OBS
  GW -.-> OBS
```

| Layer | What lives here |
| --- | --- |
| **Clients** | Next.js and TanStack Start on the web, Expo on mobile, TanStack Query and Zustand for server/client state |
| **Edge** | CDN and Vercel Edge for TLS, caching, and geo routing; Caddy or Nginx as reverse proxy and load balancer |
| **Identity** | Sessions, JWT, OAuth; Firebase or Supabase Auth when a hosted identity layer is the right call |
| **APIs** | tRPC for first-party typed RPCs; Hono, NestJS, and Fastify for REST; Convex and WebSockets for realtime |
| **Async** | Redis-backed queues, cron, and a pub/sub event bus so writes can fan out without blocking the request path |
| **Data** | PostgreSQL as source of truth with a read replica; Redis for cache, sessions, and jobs; object storage for media; Prisma or Drizzle as the ORM |
| **Platform** | Dockerized services on AWS, GCP, DigitalOcean, or Hetzner; Vercel for the web surface; GitHub Actions for CI/CD |
| **Observability** | Structured logs, metrics, and traces on the gateway, APIs, and workers |

<div align="center">

**Frontend**

<img src="https://skillicons.dev/icons?i=react,nextjs,ts,tailwind,vite" alt="Frontend" />

**Backend**

<img src="https://skillicons.dev/icons?i=nodejs,express,nestjs,go,firebase,supabase" alt="Backend" />

**Data**

<img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb,sqlite,redis,prisma" alt="Data" />

**Mobile, cloud, tooling**

<img src="https://skillicons.dev/icons?i=docker,nginx,aws,gcp,vercel,linux,git,githubactions" alt="Infrastructure and tooling" />

<br />

![TanStack Start](https://img.shields.io/badge/TanStack_Start-FF4154?style=flat-square&logo=tanstack&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-443E38?style=flat-square)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat-square&logo=fastify&logoColor=white)
![Hono](https://img.shields.io/badge/Hono-E36002?style=flat-square&logo=hono&logoColor=white)
![tRPC](https://img.shields.io/badge/tRPC-2596BE?style=flat-square&logo=trpc&logoColor=white)
![Convex](https://img.shields.io/badge/Convex-F45A43?style=flat-square)
![Drizzle](https://img.shields.io/badge/Drizzle-C5F74F?style=flat-square&logo=drizzle&logoColor=black)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?style=flat-square&logo=caddy&logoColor=white)
![DigitalOcean](https://img.shields.io/badge/DigitalOcean-0080FF?style=flat-square&logo=digitalocean&logoColor=white)
![Hetzner](https://img.shields.io/badge/Hetzner-D50C2D?style=flat-square&logo=hetzner&logoColor=white)
![pnpm](https://img.shields.io/badge/pnpm-F69220?style=flat-square&logo=pnpm&logoColor=white)
![tmux](https://img.shields.io/badge/tmux-1BB91F?style=flat-square&logo=tmux&logoColor=white)

</div>

<p align="center">
  <img src="./assets/divider.svg" width="100%" alt="" />
</p>

## Analytics

<div align="center">
  <img height="170" src="https://github-stats-extended.vercel.app/api?username=cHANGTEEZY&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=22D3EE&icon_color=818CF8&text_color=C9D1D9&include_all_commits=true&count_private=true" alt="GitHub stats" />
  <img height="170" src="https://streak-stats.demolab.com?user=cHANGTEEZY&theme=tokyonight&hide_border=true&background=0D1117&ring=22D3EE&fire=818CF8&currStreakLabel=22D3EE" alt="Contribution streak" />
</div>

<div align="center">
  <img height="175" src="https://github-stats-extended.vercel.app/api/top-langs/?username=cHANGTEEZY&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=22D3EE&text_color=C9D1D9" alt="Top languages" />
  <img height="175" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=cHANGTEEZY&theme=github_dark&utcOffset=5.75" alt="Productive time chart" />
</div>

<div align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=cHANGTEEZY&theme=github_dark" alt="Repos per language" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=cHANGTEEZY&theme=github_dark" alt="Most committed language" />
</div>

<div align="center">
  <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=cHANGTEEZY&theme=react-dark&hide_border=true&bg_color=0D1117&color=818CF8&line=22D3EE&point=14B8A6&area=true&custom_title=Contribution%20activity" alt="Contribution activity graph" />
</div>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cHANGTEEZY/cHANGTEEZY/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cHANGTEEZY/cHANGTEEZY/output/github-contribution-grid-snake.svg" />
    <img alt="GitHub contribution snake" width="100%" src="https://raw.githubusercontent.com/cHANGTEEZY/cHANGTEEZY/output/github-contribution-grid-snake-dark.svg" />
  </picture>
</div>

<p align="center">
  <img src="./assets/divider.svg" width="100%" alt="" />
</p>

## Freelance

I take on freelance work alongside studio projects, especially with early-stage teams on clear, high-impact problems.

Full-stack web apps · Frontend development · Cross-platform mobile · MVP builds · API design

<div align="center">
  <a href="mailto:vbee-studio@sushankgurung.com">
    <img src="https://img.shields.io/badge/Get_in_touch-22D3EE?style=for-the-badge&logo=gmail&logoColor=0D1117" alt="Get in touch" />
  </a>
</div>

<p align="center">
  <img src="./assets/divider.svg" width="100%" alt="" />
</p>

## Reading

| Writer | Why |
|--------|-----|
| [Dan Abramov](https://overreacted.io) | Honest writing on React internals and how to think about software |
| [Josh Comeau](https://www.joshwcomeau.com) | Interactive explanations of CSS and React |
| [Dominik Dorfmeister](https://tkdodo.eu/blog) | Practical insights from the React Query maintainer |
| [Lee Robinson](https://leerob.io) | Next.js, developer experience, and product thinking |
| [Kent C. Dodds](https://kentcdodds.com/blog) | Testing philosophy and React patterns |
| [Theodorus Clarence](https://theodorusclarence.com/blog) | Production-ready TypeScript and Next.js patterns |

<div align="center">
  <img width="100%" src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight&quote=Build%20simple%20things%20that%20scale%2C%20not%20complex%20things%20that%20break.&author=Sushank%20Gurung" alt="Build simple things that scale, not complex things that break." />
</div>
