# claude-marketplace

Marketplace di plugin per [Claude Code](https://code.claude.com) di Stefano Frontini.

## Installazione

```
/plugin marketplace add StefanoFrontini/claude-marketplace
/plugin install esempio@stefanofrontini-plugins
/plugin install commit-commands@stefanofrontini-plugins
```

Per aggiornare: `/plugin marketplace update stefanofrontini-plugins`.

## Plugin disponibili

| Plugin | Descrizione |
|---|---|
| [esempio](plugins/esempio) | Skill e comando slash di esempio |
| [commit-commands](https://github.com/anthropics/claude-plugins-official/tree/main/plugins/commit-commands) | `/commit`, `/commit-push-pr`, `/clean_gone` per il workflow git (di Anthropic, Apache-2.0, referenziato dalla sorgente originale) |

## Aggiungere un plugin

1. Crea `plugins/<nome>/.claude-plugin/plugin.json`.
2. Aggiungi le componenti: `skills/<skill>/SKILL.md`, `commands/*.md`, `agents/*.md`, `hooks/hooks.json`, `.mcp.json`.
3. Registra il plugin in `.claude-plugin/marketplace.json`.
4. Verifica con `claude plugin validate .`, poi commit e push.
5. Incrementa `version` a ogni rilascio, altrimenti gli utenti non ricevono l'aggiornamento.
