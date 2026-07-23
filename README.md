<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=gradient&customColorList=6,11,20,29&text=Hi%20There,%20I'm%20Ishan%20%F0%9F%91%8B&fontSize=42&fontColor=fff&animation=twinkling&fontAlignY=35&desc=Full%20Stack%20Java%20Developer%20%7C%20AI%20Integrations%20%7C%20Spring%20Boot%20%2B%20React&descSize=17&descAlignY=55&textBg=false" />

<a href="https://www.linkedin.com/in/ishan-maharwade-635475250" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>
<a href="mailto:ishanmaharwade01@gmail.com">
  <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
</a>
<a href="https://github.com/Ishan4580">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

<br/>

<img src="https://komarev.com/ghpvc/?username=Ishan4580&label=Profile%20Views&color=00FFFF&style=flat-square" />
<img src="https://img.shields.io/github/followers/Ishan4580?label=Followers&style=flat-square&color=6f42c1" />
<img src="https://img.shields.io/badge/Open%20to-Work-brightgreen?style=flat-square" />

</div>

<br/>

### 👨‍💻 A little about me

```yaml
name: Ishan Maharwade
role: Full Stack Java Developer (AI)
focus: Scalable microservices + Generative AI integrations (RAG, LLMs, semantic search)
currently_learning: [Reactive Spring, Advanced Prompt Engineering, Spring AI]
ask_me_about: [Java REST APIs, Spring Security (JWT/OAuth2), React state management, Spring AI]
fun_fact: I enjoy turning enterprise backends into AI-powered products 🚀
```

<br/>

## 🏗️ How I Build AI-Integrated Platforms

```mermaid
graph TD
  A[ReactJS SPA] -->|REST / WebSockets| B[Spring Boot Gateway]
  B -->|JWT / OAuth2| C{Core Microservices}
  C -->|Spring Data JPA| D[(PostgreSQL / MySQL)]
  C -->|Cache & Sessions| E[(Redis)]
  C -->|Spring AI| F[LLM APIs: Gemini / OpenAI]

  subgraph Deployment
    G[Docker] --- H[Kubernetes]
  end
  C --- G

  classDef default fill:#111927,stroke:#00FFFF,stroke-width:1px,color:#fff;
  classDef database fill:#1a103c,stroke:#bf4df0,stroke-width:1px,color:#fff;
  classDef outer fill:#0c221f,stroke:#10b981,stroke-width:1px,color:#fff;

  class A,B,C,F default;
  class D,E database;
  class G,H outer;
```

<br/>

## 🧰 Tech Stack

<div align="center">

**Languages**

<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
<img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" />

**Backend**

<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" />
<img src="https://img.shields.io/badge/Spring_AI-6DB33F?style=for-the-badge&logo=spring&logoColor=white" />
<img src="https://img.shields.io/badge/REST_APIs-0052CC?style=for-the-badge&logo=postman&logoColor=white" />

**Frontend**

<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
<img src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />

**Databases**

<img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-00758F?style=for-the-badge&logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
<img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" />

**DevOps & Tools**

<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" />
<img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" />

</div>

<br/>

<details>
<summary><b>🤖 Sample: Spring AI Controller</b></summary>
<br/>

```java
@RestController
@RequestMapping("/api/ai")
public class GeminiController {

    private final ChatClient chatClient;

    public GeminiController(ChatClient.Builder builder) {
        this.chatClient = builder.build();
    }

    @GetMapping("/generate")
    public ResponseEntity<String> generateResponse(@RequestParam String prompt) {
        String response = chatClient.prompt()
                .user(prompt)
                .call()
                .content();
        return ResponseEntity.ok(response);
    }
}
```

</details>

<br/>

## 📊 GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats-eight-theta.vercel.app/api?username=Ishan4580&cache_seconds=7200&show_icons=true&theme=dark&border_radius=10&hide_border=true" />
<img height="165" src="https://streak-stats.demolab.com/?user=Ishan4580&theme=dark&hide_border=true&cache_seconds=86400" />

<img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=Ishan4580&langs_count=8&layout=compact&theme=dark&border_radius=10&hide_border=true" />

<img src="https://trophy.ryglcloud.net/?username=Ishan4580&theme=dark&no-frame=true&no-bg=true&margin-w=4&cache_seconds=86400" />

<img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=Ishan4580&theme=react-dark&radius=10&hide_border=true" />

</div>

<br/>

## 📅 Contribution Graph

<div align="center">
<img width="100%" src="https://ghchart.rshah.org/00FFFF/Ishan4580" alt="Ishan Maharwade's GitHub Contributions Chart" />
</div>

<br/>

## 🤝 Let's Connect

<div align="center">

<a href="https://www.linkedin.com/in/ishan-maharwade-635475250" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>
<a href="mailto:ishanmaharwade01@gmail.com">
  <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
</a>
<a href="https://www.buymeacoffee.com/chamidudili" target="_blank">
  <img src="https://img.shields.io/badge/Buy_Me_A_Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black" />
</a>

<br/><br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tobiasmeyhoefer/tobiasmeyhoefer/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tobiasmeyhoefer/tobiasmeyhoefer/output/github-snake.svg" />
  <img alt="github-snake" src="https://raw.githubusercontent.com/tobiasmeyhoefer/tobiasmeyhoefer/output/github-snake.svg" width="70%" />
</picture>

</div>
