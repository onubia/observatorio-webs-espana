# Observatorio de las webs de los negocios de España

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24424244.svg)](https://doi.org/10.5281/zenodo.24424244)

**377.113 webs de negocios medidas una a una, desde fuera (noviembre de 2026).** El mayor estudio público sobre el
estado de las webs y el correo de los negocios de España: 696 ciudades, 51 provincias y todos los sectores.

Web con las páginas por ciudad, imágenes y metodología: **https://onubia.com/observatorio/espana/**

## Resultados para España (20/11/2026)

| Qué | Resultado |
|---|---|
| Webs que no cargan (comprobado en dos pasadas) | **25,6 %** (96.379) |
| Negocios que anuncian un dominio que ya no existe | **15,9 %** (60.053) |
| Webs con HTTPS y el certificado mal | **9,3 %** (26.014 de 279.083) |
| Dominios con correo propio que se pueden suplantar (sin DMARC o en «solo vigilar») | **80,7 %** (222.881 de 276.128) |

## Cómo se midió
- 3,58 millones de fichas de mapas públicos (Overture Maps Foundation, con apoyo de OpenStreetMap); se quedan los
  negocios que anuncian una web propia y cada una se sitúa en uno de 8.273 municipios.
- 1,1 millones de comprobaciones en 26 horas (19 y 20 de noviembre de 2026): carga de la web en dos pasadas separadas,
  existencia del dominio (DNS), certificado HTTPS y registros públicos de correo (MX, SPF y DMARC).
- Todo desde fuera, como lo vería un cliente: no se entra en ningún sistema.
- **No se publican nombres de negocios**, solo agregados por ámbito, ciudad (con 80 webs medidas o más), provincia y
  sector.

## Ficheros (`datos/`)
| Fichero | Contenido |
|---|---|
| `observatorio-espana.csv` | España, total y por sectores |
| `observatorio-ciudades.csv` | 696 ciudades |
| `observatorio-provincias.csv` | 51 provincias |
| `observatorio-espana-cruces.json` | Por qué no carga cada web caída, candado y correo por dentro, proveedores de correo, tamaño de ciudad, islas y terminaciones de dominio |

Campos: `webs` (medidas), `caidas` / `pctCaidas` (no cargan en dos pasadas), `dominioPerdido` / `pctDominioPerdido`,
`tlsMal` / `conTls` / `pctTlsMal` (certificado mal sobre las que tienen HTTPS), `conCorreo` (dominios con correo
propio), `suplantables` / `pctSuplantables`.

## Licencia y cita
Datos bajo **Creative Commons Atribución 4.0 (CC BY 4.0)**: se pueden usar, también en prensa e informes, citando
la fuente.

> Rodríguez, J. (2026). *Observatorio de las webs de los negocios de España: 377.113 webs medidas una a una
> (noviembre de 2026)*. Onubia. https://onubia.com/observatorio/espana/

La medición se repite cada mes. Contacto: info@onubia.com · WhatsApp 677 444 395.

---

**English summary.** Outside-in measurement of the websites of 377,113 Spanish businesses listed on public maps
(November 2026): 25.6 % do not load, 15.9 % advertise a domain that no longer exists, 9.3 % of HTTPS sites have a
broken certificate and 80.7 % of businesses with their own email domain can be spoofed (no DMARC or `p=none`).
Aggregates only (no business names), by Spanish city, province and sector. CC BY 4.0.


## DOI
Archivado en Zenodo (CERN): **https://doi.org/10.5281/zenodo.24424244** (apunta siempre a la última versión; noviembre de 2026: 10.5281/zenodo.24424245).

Rodríguez, J. (2026). *Observatorio de las webs de los negocios de España: 377.113 webs medidas una a una (noviembre de 2026)* [Conjunto de datos]. Onubia. Zenodo. https://doi.org/10.5281/zenodo.24424244
