
# Agent Zero

Agent Zero é um framework de IA open-source dinâmico, modular e transparente, projetado para automação, pesquisa, desenvolvimento e integração de agentes inteligentes. Ele oferece uma arquitetura flexível baseada em agentes, ferramentas, memória, prompts, extensões e integração com protocolos MCP.

## 🚀 Instalação Rápida (Docker)

```bash
docker pull frdel/agent-zero-run
docker run -p 50001:80 frdel/agent-zero-run
# Acesse http://localhost:50001
```

## 📚 Documentação

| Página | Descrição |
|--------|-----------|
| [Instalação](./docs/installation.md) | Instalação, setup e configuração |
| [Uso](./docs/usage.md) | Uso básico e avançado |
| [Arquitetura](./docs/architecture.md) | Design do sistema e componentes |
| [Contribuição](./docs/contribution.md) | Como contribuir |
| [Troubleshooting](./docs/troubleshooting.md) | Problemas comuns e soluções |

## 💡 Principais Funcionalidades

- Execução de agentes hierárquicos e delegação de tarefas
- Ferramentas integradas: execução de código, busca, memória, resposta, ajuste de comportamento, análise web
- Memória persistente e sistema de sumarização de contexto
- Suporte a extensões e integração com MCP (Model Context Protocol)
- Interface Web UI moderna e interativa
- Backup/restore, browser agent, TTS/STT, file browser, KaTeX, anexos em chat

## 🛠️ Estrutura do Projeto

| Diretório | Descrição |
|-----------|-----------|
| /docker   | Arquivos Docker e runtime |
| /docs     | Documentação e guias |
| /instruments | Scripts customizados |
| /knowledge | Base de conhecimento |
| /logs     | Logs de chat e sistema |
| /memory   | Memória persistente |
| /prompts  | Prompts do sistema e ferramentas |
| /python   | Código principal Python |
| /webui    | Interface web |

## 🧩 Componentes Centrais

- **Agents**: Núcleo de decisão, raciocínio e execução
- **Tools**: Ferramentas para busca, execução, memória, etc.
- **Memory**: Sistema híbrido de memória e sumarização
- **Prompts**: Controle de comportamento e comunicação
- **Knowledge**: Base de dados e arquivos do usuário
- **Instruments**: Scripts e integrações customizadas
- **Extensions**: Modularidade e expansão de funcionalidades

## 🔒 Segurança

- Recomenda-se rodar em ambiente isolado (Docker)
- Suporte a autenticação e configuração de senha

## 📝 Atualização

```bash
docker stop agent-zero
docker rm agent-zero
docker rmi frdel/agent-zero-run
docker pull frdel/agent-zero-run
docker run -p $PORT:80 -v /path/to/your/data:/a0 frdel/agent-zero-run
```

## 🤝 Comunidade e Suporte

- [Discord](https://discord.gg/B8KZKNsPpj)
- [Skool](https://www.skool.com/agent-zero)
- [YouTube](https://www.youtube.com/@AgentZeroFW)
- [GitHub Issues](https://github.com/frdel/agent-zero/issues)

---
Consulte a documentação completa em [docs/](./docs/README.md).
- Every agent can create its subordinate agent to help break down and solve subtasks. This helps all agents keep their context clean and focused.

![Multi-agent](docs/res/physics.png)
![Multi-agent 2](docs/res/physics-2.png)

4. **Completely Customizable and Extensible**

- Almost nothing in this framework is hard-coded. Nothing is hidden. Everything can be extended or changed by the user.
- The whole behavior is defined by a system prompt in the **prompts/default/agent.system.md** file. Change this prompt and change the framework dramatically.
- The framework does not guide or limit the agent in any way. There are no hard-coded rails that agents have to follow.
- Every prompt, every small message template sent to the agent in its communication loop can be found in the **prompts/** folder and changed.
- Every default tool can be found in the **python/tools/** folder and changed or copied to create new predefined tools.

![Prompts](/docs/res/prompts.png)

5. **Communication is Key**

- Give your agent a proper system prompt and instructions, and it can do miracles.
- Agents can communicate with their superiors and subordinates, asking questions, giving instructions, and providing guidance. Instruct your agents in the system prompt on how to communicate effectively.
- The terminal interface is real-time streamed and interactive. You can stop and intervene at any point. If you see your agent heading in the wrong direction, just stop and tell it right away.
- There is a lot of freedom in this framework. You can instruct your agents to regularly report back to superiors asking for permission to continue. You can instruct them to use point-scoring systems when deciding when to delegate subtasks. Superiors can double-check subordinates' results and dispute. The possibilities are endless.

## 🚀 Things you can build with Agent Zero

- **Development Projects** - `"Create a React dashboard with real-time data visualization"`

- **Data Analysis** - `"Analyze last quarter's NVIDIA sales data and create trend reports"`

- **Content Creation** - `"Write a technical blog post about microservices"`

- **System Admin** - `"Set up a monitoring system for our web servers"`

- **Research** - `"Gather and summarize five recent AI papers about CoT prompting"`

# Hacking Edition
- Agent Zero also offers a Hacking Edition based on Kali linux with modified prompts for cybersecurity tasks
- The setup is the same as the regular version, just use the frdel/agent-zero-run:hacking image instead of frdel/agent-zero-run
> **Note:** The Hacking Edition and all its prompts and features will be merged into the main branch in the following release.


# ⚙️ Installation

Click to open a video to learn how to install Agent Zero:

[![Easy Installation guide](/docs/res/easy_ins_vid.png)](https://www.youtube.com/watch?v=L1_peV8szf8)

A detailed setup guide for Windows, macOS, and Linux with a video can be found in the Agent Zero Documentation at [this page](./docs/installation.md).

### ⚡ Quick Start

```bash
# Pull and run with Docker

docker pull frdel/agent-zero-run
docker run -p 50001:80 frdel/agent-zero-run

# Visit http://localhost:50001 to start
```

## 🐳 Fully Dockerized, with Speech-to-Text and TTS

![Settings](docs/res/settings-page-ui.png)

- Customizable settings allow users to tailor the agent's behavior and responses to their needs.
- The Web UI output is very clean, fluid, colorful, readable, and interactive; nothing is hidden.
- You can load or save chats directly within the Web UI.
- The same output you see in the terminal is automatically saved to an HTML file in **logs/** folder for every session.

![Time example](/docs/res/time_example.jpg)

- Agent output is streamed in real-time, allowing users to read along and intervene at any time.
- No coding is required; only prompting and communication skills are necessary.
- With a solid system prompt, the framework is reliable even with small models, including precise tool usage.

## 👀 Keep in Mind

1. **Agent Zero Can Be Dangerous!**

- With proper instruction, Agent Zero is capable of many things, even potentially dangerous actions concerning your computer, data, or accounts. Always run Agent Zero in an isolated environment (like Docker) and be careful what you wish for.

2. **Agent Zero Is Prompt-based.**

- The whole framework is guided by the **prompts/** folder. Agent guidelines, tool instructions, messages, utility AI functions, it's all there.


## 📚 Read the Documentation

| Page | Description |
|-------|-------------|
| [Installation](./docs/installation.md) | Installation, setup and configuration |
| [Usage](./docs/usage.md) | Basic and advanced usage |
| [Architecture](./docs/architecture.md) | System design and components |
| [Contributing](./docs/contribution.md) | How to contribute |
| [Troubleshooting](./docs/troubleshooting.md) | Common issues and their solutions |

## Coming soon

- **MCP**
- **Knowledge and RAG Tools**

## 🎯 Changelog

### v0.8.7 - Formatting, Document RAG Latest
[Release video](https://youtu.be/OQJkfofYbus)
- markdown rendering in responses
- live response rendering
- document Q&A tool

### v0.8.6 - Merge and update
[Release video](https://youtu.be/l0qpK3Wt65A)
- Merge with Hacking Edition
- browser-use upgrade and integration re-work
- tunnel provider switch

### v0.8.5 - **MCP Server + Client**
[Release video](https://youtu.be/pM5f4Vz3_IQ)

- Agent Zero can now act as MCP Server
- Agent Zero can use external MCP servers as tools

### v0.8.4.1 - 2
Default models set to gpt-4.1
- Code execution tool improvements
- Browser agent improvements
- Memory improvements
- Various bugfixes related to context management
- Message formatting improvements
- Scheduler improvements
- New model provider
- Input tool fix
- Compatibility and stability improvements

### v0.8.4
[Release video](https://youtu.be/QBh_h_D_E24)

- **Remote access (mobile)**

### v0.8.3.1
[Release video](https://youtu.be/AGNpQ3_GxFQ)

- **Automatic embedding**


### v0.8.3
[Release video](https://youtu.be/bPIZo0poalY)

- ***Planning and scheduling***

### v0.8.2
[Release video](https://youtu.be/xMUNynQ9x6Y)

- **Multitasking in terminal**
- **Chat names**

### v0.8.1
[Release video](https://youtu.be/quv145buW74)

- **Browser Agent**
- **UX Improvements**

### v0.8
[Release video](https://youtu.be/cHDCCSr1YRI)

- **Docker Runtime**
- **New Messages History and Summarization System**
- **Agent Behavior Change and Management**
- **Text-to-Speech (TTS) and Speech-to-Text (STT)**
- **Settings Page in Web UI**
- **SearXNG Integration Replacing Perplexity + DuckDuckGo**
- **File Browser Functionality**
- **KaTeX Math Visualization Support**
- **In-chat File Attachments**

### v0.7
[Release video](https://youtu.be/U_Gl0NPalKA)

- **Automatic Memory**
- **UI Improvements**
- **Instruments**
- **Extensions Framework**
- **Reflection Prompts**
- **Bug Fixes**

## 🤝 Community and Support

- [Join our Discord](https://discord.gg/B8KZKNsPpj) for live discussions or [visit our Skool Community](https://www.skool.com/agent-zero).
- [Follow our YouTube channel](https://www.youtube.com/@AgentZeroFW) for hands-on explanations and tutorials
- [Report Issues](https://github.com/frdel/agent-zero/issues) for bug fixes and features
