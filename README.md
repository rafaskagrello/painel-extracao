# Painel de Extração

App web para acompanhar extrações de espresso com a balança Timemore Dot via Bluetooth (Web Bluetooth).

- Ponteiro com o peso, tempo total, tempo até o alvo e vazão (g/s)
- Curva da extração (peso e vazão) e histórico com comparação
- Simulador quando não há balança conectada

Protocolo: serviço `FFF0`, característica `FFF1` (notify); pacote `A5 5A …` com o peso em décimos de grama nos bytes 8–9 (int16 big-endian).

Uso no iPhone: abrir pelo app Bluefy. No computador: Chrome ou Edge (a balança precisa estar pareada no Windows).

## Versões

- **v1.3** — número da versão no topo; mensagens de erro do Bluetooth detalhadas; busca alternativa mostrando todos os aparelhos.
- **v1.2** — tenta outra característica ou leitura direta quando as notificações são recusadas.
- **v1.1** — conexão Bluetooth com a Timemore Dot (protocolo do BalancaService.cs).
- **v1.0** — ponteiro, curva da extração, histórico em aba separada, simulador.
