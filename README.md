# mc-server-mods

Mody dla serwera Star Technology 1.20.1 (Forge 47.4.20) — mirror z Modrinth dla łatwego pobierania.

## BandwidthOptimizer 5.10.33.156 (Forge 1.20.1)

Redukuje ruch sieciowy serwera do ~5-16% (Zstd, batching, chunk cache) i dodaje taryfe ulgowa dla keepalive — fix na "connection reset" / "Timed out" przy wolnych laczach graczy.

**WYMOG: ta sama wersja na serwerze I u kazdego klienta.**

### Serwer (LXC MC-3M)

```bash
cd /opt/start/mods
curl -fL -A "Mozilla/5.0" -o BandwidthOptimizer-5.10.33.156-forge-1.20.1.jar "https://raw.githubusercontent.com/Rezurmas/mc-server-mods/master/mods/BandwidthOptimizer-5.10.33.156-forge-1.20.1.jar"
ls -l BandwidthOptimizer-5.10.33.156-forge-1.20.1.jar
systemctl restart start-mc
```

Albo z hosta Proxmox: `pct push 100 <jar> /opt/start/mods/`

### Klient

Pobierz ten sam jar i wrzuc do folderu `mods/` instancji Star Technology w swoim launcherze.

### Test

Jako op na serwerze: `/bandwidthoptimizer stats` (raport oszczednosci) i `/bandwidthoptimizer hud` u klienta.

## Uwagi

- Mirror, nie fork. Zrodlo: https://modrinth.com/mod/bandwidthoptimizer (LGPL-2.1-or-later, autor duckgun13476).
- Wersja paka: Star Technology 1.20.1 THETA 2 HOTFIX 4 (Forge 47.4.20).
