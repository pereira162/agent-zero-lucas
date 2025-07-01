
![Agent Zero Logo](res/header.png)
# Agent Zero Documentation

## Índice

- [Instalação](installation.md)
- [Guia de Uso](usage.md)
- [Arquitetura](architecture.md)
- [Contribuição](contribution.md)
- [Troubleshooting](troubleshooting.md)

## Visão Geral

Agent Zero é um framework de IA open-source para automação, pesquisa, desenvolvimento e integração de agentes inteligentes. Ele oferece arquitetura modular baseada em agentes, ferramentas, memória, prompts, extensões e integração com MCP.

## Instalação Rápida

```bash
docker pull frdel/agent-zero-run
docker run -p 50001:80 frdel/agent-zero-run
# Acesse http://localhost:50001
```

## Estrutura do Projeto

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

## Componentes Centrais

- **Agents**: Núcleo de decisão, raciocínio e execução
- **Tools**: Ferramentas para busca, execução, memória, etc.
- **Memory**: Sistema híbrido de memória e sumarização
- **Prompts**: Controle de comportamento e comunicação
- **Knowledge**: Base de dados e arquivos do usuário
- **Instruments**: Scripts e integrações customizadas
- **Extensions**: Modularidade e expansão de funcionalidades

## Funcionalidades

- Execução de agentes hierárquicos e delegação de tarefas
- Ferramentas integradas: execução de código, busca, memória, resposta, ajuste de comportamento, análise web
- Memória persistente e sistema de sumarização de contexto
- Suporte a extensões e integração com MCP (Model Context Protocol)
- Interface Web UI moderna e interativa
- Backup/restore, browser agent, TTS/STT, file browser, KaTeX, anexos em chat

## Segurança

- Recomenda-se rodar em ambiente isolado (Docker)
- Suporte a autenticação e configuração de senha

## Atualização

```bash
docker stop agent-zero
docker rm agent-zero
docker rmi frdel/agent-zero-run
docker pull frdel/agent-zero-run
docker run -p $PORT:80 -v /path/to/your/data:/a0 frdel/agent-zero-run
```

## Comunidade e Suporte

- [Discord](https://discord.gg/B8KZKNsPpj)
- [Skool](https://www.skool.com/agent-zero)
- [YouTube](https://www.youtube.com/@AgentZeroFW)
- [GitHub Issues](https://github.com/frdel/agent-zero/issues)

---
Consulte a documentação detalhada em cada arquivo acima.

- **Download Agent Zero:** Follow the [installation guide](installation.md) to download and run Agent Zero.
- **Join the Community:** Join the Agent Zero [Skool](https://www.skool.com/agent-zero) or [Discord](https://discord.gg/Z2tun2N3) community to discuss ideas, ask questions, and collaborate with other contributors.
- **Share your Work:** Share your Agent Zero creations, workflows and discoverings on our [Show and Tell](https://github.com/frdel/agent-zero/discussions/categories/show-and-tell) area on GitHub.
- **Report Issues:** Use the [GitHub issue tracker](https://github.com/frdel/agent-zero/issues) to report framework-relative bugs or suggest new features.

## Table of Contents

- [Welcome to the Agent Zero Documentation](#agent-zero-documentation)
  - [Your Experience with Agent Zero](#your-experience-with-agent-zero-starts-now)
  - [Table of Contents](#table-of-contents)
- [Installation Guide](installation.md)
  - [Windows, macOS and Linux Setup](installation.md#windows-macos-and-linux-setup-guide)
  - [Settings Configuration](installation.md#settings-configuration)
  - [Choosing Your LLMs](installation.md#choosing-your-llms)
  - [Installing and Using Ollama](installation.md#installing-and-using-ollama-local-models)
  - [Using Agent Zero on Mobile](installation.md#using-agent-zero-on-your-mobile-device)
  - [How to Update Agent Zero](installation.md#how-to-update-agent-zero)
  - [Full Binaries Installation](installation.md#in-depth-guide-for-full-binaries-installation)
- [Usage Guide](usage.md)
  - [Basic Operations](usage.md#basic-operations)
    - [Restart Framework](usage.md#restart-framework)
    - [Action Buttons](usage.md#action-buttons)
    - [File Attachments](usage.md#file-attachments)
  - [Tool Usage](usage.md#tool-usage)
  - [Example of Tools Usage](usage.md#example-of-tools-usage-web-search-and-code-execution)
  - [Multi-Agent Cooperation](usage.md#multi-agent-cooperation)
  - [Prompt Engineering](usage.md#prompt-engineering)
  - [Voice Interface](usage.md#voice-interface)
  - [Mathematical Expressions](usage.md#mathematical-expressions)
  - [File Browser](usage.md#file-browser)
  - [Backup & Restore](usage.md#backup--restore)
- [Architecture Overview](architecture.md)
  - [System Architecture](architecture.md#system-architecture)
  - [Runtime Architecture](architecture.md#runtime-architecture)
  - [Implementation Details](architecture.md#implementation-details)
  - [Core Components](architecture.md#core-components)
    - [Agents](architecture.md#1-agents)
    - [Tools](architecture.md#2-tools)
    - [SearXNG Integration](architecture.md#searxng-integration)
    - [Memory System](architecture.md#3-memory-system)
    - [Messages History and Summarization](archicture.md#messages-history-and-summarization)
    - [Prompts](architecture.md#4-prompts)
    - [Knowledge](architecture.md#5-knowledge)
    - [Instruments](architecture.md#6-instruments)
    - [Extensions](architecture.md#7-extensions)
  - [Contributing](contribution.md)
  - [Getting Started](contribution.md#getting-started)
  - [Making Changes](contribution.md#making-changes)
  - [Submitting a Pull Request](contribution.md#submitting-a-pull-request)
  - [Documentation Stack](contribution.md#documentation-stack)
- [Troubleshooting and FAQ](troubleshooting.md)
  - [Frequently Asked Questions](troubleshooting.md#frequently-asked-questions)
  - [Troubleshooting](troubleshooting.md#troubleshooting)
