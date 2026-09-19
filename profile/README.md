# Radiopath

Radio coverage and link planning for amateur radio and beyond. A self-hosted
web application written in Go, inspired by Radio Mobile.

- **Point-to-point links:** terrain profile, path loss, link budget, first
  Fresnel zone clearance
- **Area coverage:** link margin raster around a transmitter, rendered on the map
- **Propagation:** NTIA Irregular Terrain Model (Longley-Rice), ported to Go from
  the public domain reference; optional tree canopy loss after ITU-R P.833
- **Terrain:** Copernicus GLO-30 or SRTM tiles from a directory or an S3 bucket
- **Runs anywhere:** single binary, multi-arch container image, Helm chart

## Repositories

| Repository | What it is |
|---|---|
| [radiopath](https://github.com/radiopath/radiopath) | The application: server, ITM port, web UI, Helm chart |

Container images: `ghcr.io/radiopath/radiopath`

## Getting started

```sh
git clone https://github.com/radiopath/radiopath && cd radiopath
make db-up     # PostGIS and Redis via docker compose
make run       # http://localhost:8080
```

You also need at least one terrain tile, see the
[README](https://github.com/radiopath/radiopath#requirements).

## License

AGPL-3.0-or-later. A commercial license is available for running a modified
Radiopath as a hosted service without publishing the changes, see
[COMMERCIAL-LICENSE.md](https://github.com/radiopath/radiopath/blob/main/COMMERCIAL-LICENSE.md).

Maintained by Fabian Berg, HB9HIL.
