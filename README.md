# DM TV — Releases

APKs firmadas y configuración remota de **DM TV** (el código fuente vive en un repo privado).

- **Última APK**: en [Releases](https://github.com/gutieduisma-hue/dm-tv-releases/releases).
- **`dmtv_config.json`**: config remota que la app consulta al abrir — dominios de las fuentes y aviso de nueva versión (`latest_version_code` + `update_url`).

## Publicar una actualización

1. Compilar la APK firmada (`flutter build apk --release`) con `version:` nuevo en el pubspec.
2. Crear un release `vX.Y.Z` acá con la APK como asset (`dm-tv-vX.Y.Z.apk`).
3. Actualizar `dmtv_config.json`: `latest_version_code` (el número tras el `+` del pubspec), `latest_version_name` y `update_url`.

Las apps instaladas comparan su build contra `latest_version_code` y muestran el aviso con el link.