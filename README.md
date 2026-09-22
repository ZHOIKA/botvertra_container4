# BotVertra Container 4

Quarto container VertraCloud, com 20 workers locais conectados ao controller externo por WebSocket.

Variáveis na VertraCloud:

- `CONTROLLER_URL=wss://botvertra-controller.onrender.com/ws/agent`
- `CONTROLLER_TOKEN=<mesmo token do controller Render>`
- `CONTAINER_NAME=container4`

Start:

```bash
python3 start.py
```

Comandos remotos permitidos: `ping`, `status`, `uptime`, `hostname`, `disk`,
`memory`, `echo`, `logs`, `internet`, `public_ip`, `exec`, `shell`.

O comando `exec` (ou `shell`) executa shell livre no bot — `ls -la`,
`curl -s ifconfig.me`, `cat arquivo`, `ps aux` — herdando a rota de IP do bot
(proxy/Tor), então `curl` sai pelo IP daquele bot. Campos extras:
`command_line`, `timeout` (default 30s, teto 300s), `cwd`, `stdin`, `shell`.
Implementado em `shell_exec.py`.
