# Sofia Anthropic Plugin

Plugin [Claude Code](https://code.claude.com/docs/en/plugins) com a skill **Sofia Fin System API** — documentação estruturada da API de gestão financeira da Sofia (contas bancárias, lançamentos, notas fiscais, conciliação, relatórios e mais).

## Estrutura

```
sofia-anthropic-plugin/
├── .claude-plugin/
│   └── plugin.json          # manifest do plugin
├── skills/
│   └── sofia-fin-system-api/
│       ├── SKILL.md         # skill principal
│       └── references/      # recursos, operações, schemas e workflows
└── README.md
```

A skill é invocada como:

```text
/sofia-anthropic-plugin:sofia-fin-system-api
```

## Instalação

### Desenvolvimento local

```bash
git clone git@github.com:sofia-open-source/sofia-anthropic-plugin.git
claude --plugin-dir ./sofia-anthropic-plugin
```

### Instalação permanente

```bash
/plugin install sofia-anthropic-plugin@<marketplace-ou-caminho-local>
```

Ou adicione este repositório a um marketplace da equipe e instale via `/plugin`.

## Autenticação

A API usa bearer token no header. Configure a variável de ambiente antes de chamar endpoints:

```bash
export SOFIA_API_TOKEN="seu-token"
```

Base URL de produção: `https://app-proxy-public-prod.sofia-fin-system.com`
