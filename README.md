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

Comandos remotos permitidos: `ping`, `status`, `uptime`, `hostname`, `disk`, `memory`, `echo`, `logs`.
