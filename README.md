# Visor de mesas observadas 2026

Mapa interactivo de mesas de votación observadas en la primera vuelta presidencial, Perú 2026.

## Archivos

- `index.html`: entrada principal; redirige al mapa.
- `mapa_estado_actual_mesas.html`: visor Leaflet/Folium.
- `staticwebapp.config.json`: configuración de Azure Static Web Apps con autenticación Microsoft Entra ID.

## Configuración sugerida en Azure Static Web Apps

Crear una Static Web App nueva desde Azure Portal con GitHub como origen.

- `Resource group`: `DA_Site`
- `Plan`: `Standard`
- `Region`: `East US 2`
- `Repository`: este repositorio
- `Branch`: `main`
- `App location`: `/`
- `Api location`: dejar vacío
- `Output location`: dejar vacío

La autenticación usa el tenant:

```text
d33c0234-bf45-4278-a57e-807267d3b90d
```

Si Azure crea una App Registration nueva, configurar el redirect URI:

```text
https://<tu-static-web-app>.azurestaticapps.net/.auth/login/aad/callback
```
