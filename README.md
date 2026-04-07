# 🎓 Portal do Aluno - Infraestrutura 3DS

Este projeto consiste na infraestrutura e conteúdo do portal de aulas para as turmas de Desenvolvimento de Sistemas (3DS). Ele utiliza uma arquitetura moderna baseada em Containers e Orquestração, servindo como um laboratório prático de DevOps e SRE.

## 🚀 Tecnologias Utilizadas

- Frontend: Nginx (Alpine) servindo conteúdo estático (HTML5/CSS3).

- Containerização: Docker com suporte a Multi-arch (x86_64/Xeon).

- Orquestração: Kubernetes (K3s) utilizando Kustomize para gestão de ambientes.

- Registry Local: Armazenamento privado de imagens em registry.mribeiro.dev.

- Exposição: Cloudflare Tunnel (Zero Trust) para acesso seguro via aulas.mribeiro.dev.

## 🏗️ Estrutura do Projeto

O repositório segue o padrão de Infrastructure as Code (IaC), separando a base (blueprint) das configurações específicas de cada turma (environments).

```text
.
├── blueprints-infrastructure/   # Definições base (Deployment, Service)
│   └── portal-aluno/
│       ├── Dockerfile           # Receita da imagem Nginx
│       └── deployment.yaml      # Manifesto K8s principal
└── environments/                # Overlays por turma
    └── 3ds-aulas/
        └── kustomization.yaml   # Customização (Namespace, Prefixos)
```

## 🌐 Acesso ao Portal

O portal está disponível publicamente através de um túnel seguro, eliminando a necessidade de abertura de portas (Port Forwarding) no roteador doméstico.

### 🔗 Acesse aqui: aulas.mribeiro.dev

# 📚 Conteúdo para Alunos

Dentro deste portal, você encontrará materiais sobre:

- Git & GitHub: Fluxo de trabalho e comandos essenciais.

- Desenvolvimento Mobile: Primeiros passos e estruturação.

- TCC: Exemplos de projetos e templates de documentação.

## 👨‍🏫 Desenvolvido por

Matheus Ribeiro Professor de Tecnologia & Especialista em Infraestrutura - mribeiro.dev
