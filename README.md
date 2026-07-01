# Sofia Anthropic

Plugin [Claude Code](https://code.claude.com/docs/en/plugins) com a skill **Sofia Fin System API** — documentação estruturada da API de gestão financeira da Sofia (contas bancárias, lançamentos, notas fiscais, conciliação, relatórios e mais).

## Estrutura

```
sofia-anthropic/
├── .claude-plugin/
│   ├── plugin.json          # manifest do plugin
│   └── marketplace.json     # catálogo para distribuição
├── skills/
│   └── sofia-fin-system-api/
│       ├── SKILL.md         # skill principal
│       └── references/      # recursos, operações, schemas e workflows
├── scripts/
│   └── sync-skill.sh        # sincroniza a skill a partir do fin-system-2
└── README.md
```

A skill é invocada como:

```text
/sofia-anthropic:sofia-fin-system-api
```

## Instalação

### Desenvolvimento local

```bash
git clone git@github.com:sofia-open-source/sofia-anthropic.git
claude --plugin-dir ./sofia-anthropic
```

### Instalação via marketplace

```bash
/plugin marketplace add sofia-open-source/sofia-anthropic
/plugin install sofia-anthropic@sofia-plugins
```

Para testar o marketplace localmente antes de publicar:

```bash
/plugin marketplace add ./sofia-anthropic
/plugin install sofia-anthropic@sofia-plugins
```

Validar o manifest:

```bash
claude plugin validate .
```

## Autenticação

A API usa bearer token no header. Configure a variável de ambiente antes de chamar endpoints:

```bash
export SOFIA_API_TOKEN="seu-token"
```

Base URL de produção: `https://app-proxy-public-prod.sofia-fin-system.com`
