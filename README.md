# scoop-bucket

Bucket personal de [Scoop](https://scoop.sh/) con apps mantenidas por
[@ShizukaJiku](https://github.com/ShizukaJiku).

## Uso

```powershell
scoop bucket add shizuka https://github.com/ShizukaJiku/scoop-bucket
scoop install <app>
```

## Apps

| App | Descripción |
|-----|-------------|
| [`sftp-sync`](bucket/sftp-sync.json) | Sincronizador de carpetas multi-PC sobre SFTP, estilo Git. Repo: [sftp-sync](https://github.com/ShizukaJiku/sftp-sync). |

### sftp-sync

```powershell
scoop install sftp-sync
sftp-sync --help
```

> **Requisito de CPU**: el binario está compilado con `-march=x86-64-v3`. Requiere
> CPU Intel Haswell (2013+) o AMD Excavator (2015+).

## Cómo se mantiene el bucket

- Cada manifest está en `bucket/<app>.json` con formato estándar de Scoop.
- `checkver` y `autoupdate` están configurados — `scoop bucket known` y
  `scoop status` detectan releases nuevas automáticamente.
- Los SHA-256 se actualizan después de cada release del proyecto upstream.

## Licencia

Los manifests están bajo [MIT](./LICENSE). Las apps que instalan tienen sus
propias licencias (ver el campo `license` en cada manifest).
