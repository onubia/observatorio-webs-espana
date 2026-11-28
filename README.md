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

<!-- por-dentro -->
## Por dentro de las webs (2026-11-22 a 2026-11-24)

Además de si cargan, se leyó la portada de 266.854 webs y 106.407 avisos legales. Cada cifra se calcula sobre las webs en las que se puede medir (entre paréntesis) y solo se publica con 80 webs o más detrás. Cada medida se revisó a mano antes de publicarla (al menos 20 webs al azar, 90 % de aciertos o más).

- 33,4 % con WordPress 6 o anterior (30.856 de las 92.352 webs en WordPress que enseñan su versión)
- 40,4 % con una versión de PHP sin soporte (14.105 de las 34.918 webs que enseñan su versión de PHP)
- 14,4 % miden visitas sin aviso de cookies (17.347 de las 120.657 webs con alguna herramienta de seguimiento)
- 8,2 % con estadísticas que no miden nada desde 2023 (21.817 de las 266.854 webs leídas)
- 22,2 % sin ningún enlace a sus textos legales (53.322 de las 240.522 portadas que se pudieron leer)
- 14,8 % sin NIF en el aviso legal (15.759 de los 106.407 avisos legales leídos)
- 51,8 % sociedades sin sus datos del Registro Mercantil (29.974 de los 57.829 avisos legales de sociedades (S.L., S.A.))
- 27,1 % con imágenes sin texto alternativo (63.707 de las 235.497 portadas con imágenes)
- 21,4 % bloquean el zoom en el móvil (51.389 de las 240.522 portadas que se pudieron leer)
- 27,3 % sin descripción para Google (65.726 de las 240.522 portadas que se pudieron leer)
- 1,8 % piden a Google que no las enseñe (4.437 de las 240.522 portadas que se pudieron leer)
- 7,2 % con el dominio a punto de caducar (13.810 de los 192.665 dominios .com y .net con fecha de caducidad pública)
- En el móvil, una web tarda de mediana 6,7 s en enseñar su contenido principal; solo el 19,4 % pasa el límite de Google (2,5 s) y el 34,4 % tarda más de 10 s (iPhone 13 con 4G lenta (1,6 Mbps, 150 ms) y procesador 4 veces más lento, como PageSpeed de Google en móvil; muestra de 28.307 webs ponderada por provincia).

No pasaron la revisión a mano y no se publican: año del pie, etiquetas de los formularios.

Fichero: `datos/observatorio-por-dentro.csv` (España, provincias y ciudades).
<!-- /por-dentro -->

## El correo según el proveedor (MX del 26/11/2026)

267.797 dominios de negocios con correo, agrupados por el proveedor que dice su registro MX. «Suplantable» = sin DMARC o
con `p=none`. No es un fallo del proveedor: la protección la activa quien lleva cada dominio.

| Proveedor | Dominios | Suplantables | Sin DMARC | DMARC solo en «vigilar» |
|---|---|---|---|---|
| IONOS | 32.991 | 97,6 % | 6,7 % | 90,9 % |
| Google Workspace | 24.563 | 84,8 % | 44,6 % | 40,2 % |
| Microsoft 365 | 21.831 | 72,3 % | 37,6 % | 34,8 % |
| Arsys | 16.709 | 86,4 % | 76,6 % | 9,9 % |
| Hostinger | 8.250 | 98,3 % | 11,2 % | 87,2 % |
| OVHcloud | 5.517 | 96,2 % | 83,4 % | 12,8 % |
| SiteGround | 5.070 | 96,0 % | 1,6 % | 94,4 % |
| DonDominio | 4.349 | 95,6 % | 82,5 % | 13,1 % |
| Nominalia | 3.454 | 97,8 % | 82,3 % | 15,5 % |
| Zoho Mail | 1.549 | 85,2 % | 42,1 % | 43,1 % |
| GoDaddy | 436 | 64,7 % | 57,1 % | 7,6 % |
| Otros o servidor propio | 143.078 | 74,7 % | 41,6 % | 33,2 % |

Cómo arreglarlo en cada proveedor: **https://onubia.com/blog/configurar-spf-dkim-dmarc-paso-a-paso/** · Comprueba tu dominio:
https://onubia.com/comprobar-spf-dmarc/

<!-- respuestas -->
## ¿Cuántas webs no cargan y cuántos correos se pueden suplantar en cada provincia?

| Dónde | Webs medidas | No cargan | Dominio perdido | Correo suplantable |
|---|---|---|---|---|
| [A Coruña](https://onubia.com/observatorio/provincia-de-a-coruna/) | 8.926 | 21,6 % | 13,7 % | 78,3 % (5.289 de 6.751) |
| [Albacete](https://onubia.com/observatorio/provincia-de-albacete/) | 2.686 | 23,4 % | 15,8 % | 76,8 % (1.509 de 1.966) |
| [Alicante](https://onubia.com/observatorio/provincia-de-alicante/) | 20.937 | 23,0 % | 15,0 % | 79,5 % (12.353 de 15.535) |
| [Almería](https://onubia.com/observatorio/provincia-de-almeria/) | 4.864 | 26,8 % | 16,9 % | 80,4 % (2.803 de 3.485) |
| [Asturias](https://onubia.com/observatorio/provincia-de-asturias/) | 8.716 | 25,5 % | 16,1 % | 82,2 % (5.150 de 6.267) |
| [Álava](https://onubia.com/observatorio/provincia-de-alava/) | 2.221 | 23,4 % | 14,6 % | 83,7 % (1.401 de 1.674) |
| [Ávila](https://onubia.com/observatorio/provincia-de-avila/) | 1.456 | 28,0 % | 18,6 % | 83,0 % (847 de 1.020) |
| [Badajoz](https://onubia.com/observatorio/provincia-de-badajoz/) | 4.010 | 24,8 % | 16,1 % | 78,6 % (2.348 de 2.988) |
| [Barcelona](https://onubia.com/observatorio/provincia-de-barcelona/) | 45.569 | 28,4 % | 16,5 % | 77,6 % (25.601 de 33.004) |
| [Bizkaia](https://onubia.com/observatorio/provincia-de-bizkaia/) | 6.863 | 27,4 % | 15,9 % | 80,9 % (4.066 de 5.027) |
| [Burgos](https://onubia.com/observatorio/provincia-de-burgos/) | 3.037 | 23,8 % | 13,9 % | 79,9 % (1.826 de 2.286) |
| [Cantabria](https://onubia.com/observatorio/provincia-de-cantabria/) | 5.459 | 27,9 % | 17,2 % | 81,3 % (3.172 de 3.900) |
| [Castellón](https://onubia.com/observatorio/provincia-de-castellon/) | 4.919 | 23,4 % | 14,7 % | 79,9 % (2.944 de 3.683) |
| [Cáceres](https://onubia.com/observatorio/provincia-de-caceres/) | 2.766 | 25,2 % | 14,3 % | 79,3 % (1.652 de 2.084) |
| [Cádiz](https://onubia.com/observatorio/provincia-de-cadiz/) | 8.666 | 26,6 % | 17,2 % | 83,3 % (5.185 de 6.222) |
| [Ciudad Real](https://onubia.com/observatorio/provincia-de-ciudad-real/) | 2.997 | 23,7 % | 16,4 % | 81,8 % (1.845 de 2.256) |
| [Córdoba](https://onubia.com/observatorio/provincia-de-cordoba/) | 5.171 | 23,8 % | 15,6 % | 79,0 % (3.088 de 3.910) |
| [Cuenca](https://onubia.com/observatorio/provincia-de-cuenca/) | 1.389 | 24,4 % | 17,4 % | 80,7 % (803 de 995) |
| [Gipuzkoa](https://onubia.com/observatorio/provincia-de-gipuzkoa/) | 5.104 | 25,6 % | 14,5 % | 81,1 % (3.042 de 3.752) |
| [Girona](https://onubia.com/observatorio/provincia-de-girona/) | 8.515 | 26,0 % | 14,6 % | 76,4 % (4.887 de 6.398) |
| [Granada](https://onubia.com/observatorio/provincia-de-granada/) | 7.929 | 25,1 % | 16,4 % | 82,0 % (4.685 de 5.712) |
| [Guadalajara](https://onubia.com/observatorio/provincia-de-guadalajara/) | 1.649 | 25,8 % | 16,7 % | 83,2 % (981 de 1.179) |
| [Huelva](https://onubia.com/observatorio/provincia-de-huelva/) | 4.189 | 23,0 % | 15,0 % | 81,6 % (2.498 de 3.063) |
| [Huesca](https://onubia.com/observatorio/provincia-de-huesca/) | 2.554 | 21,7 % | 12,9 % | 80,1 % (1.595 de 1.992) |
| [Illes Balears](https://onubia.com/observatorio/provincia-de-illes-balears/) | 14.697 | 24,5 % | 14,9 % | 85,1 % (9.234 de 10.855) |
| [Jaén](https://onubia.com/observatorio/provincia-de-jaen/) | 3.674 | 27,7 % | 16,5 % | 79,9 % (2.176 de 2.722) |
| [La Rioja](https://onubia.com/observatorio/provincia-de-la-rioja/) | 2.664 | 24,6 % | 15,0 % | 82,3 % (1.664 de 2.021) |
| [Las Palmas](https://onubia.com/observatorio/provincia-de-las-palmas/) | 8.519 | 27,1 % | 16,6 % | 84,9 % (5.138 de 6.053) |
| [León](https://onubia.com/observatorio/provincia-de-leon/) | 3.455 | 24,5 % | 15,2 % | 85,3 % (2.189 de 2.566) |
| [Lleida](https://onubia.com/observatorio/provincia-de-lleida/) | 3.834 | 24,9 % | 13,8 % | 74,7 % (2.209 de 2.958) |
| [Lugo](https://onubia.com/observatorio/provincia-de-lugo/) | 2.759 | 20,7 % | 13,0 % | 78,2 % (1.611 de 2.060) |
| [Madrid](https://onubia.com/observatorio/provincia-de-madrid/) | 49.077 | 26,4 % | 16,6 % | 82,8 % (29.115 de 35.178) |
| [Málaga](https://onubia.com/observatorio/provincia-de-malaga/) | 19.531 | 25,4 % | 16,1 % | 82,1 % (11.665 de 14.213) |
| [Melilla](https://onubia.com/observatorio/provincia-de-melilla/) | 230 | 30,4 % | 18,7 % | 81,0 % (124 de 153) |
| [Murcia](https://onubia.com/observatorio/provincia-de-murcia/) | 10.645 | 25,3 % | 16,4 % | 80,2 % (6.242 de 7.783) |
| [Navarra](https://onubia.com/observatorio/provincia-de-navarra/) | 4.713 | 20,6 % | 12,8 % | 80,1 % (2.913 de 3.636) |
| [Ourense](https://onubia.com/observatorio/provincia-de-ourense/) | 2.037 | 24,5 % | 16,8 % | 75,9 % (1.112 de 1.466) |
| [Palencia](https://onubia.com/observatorio/provincia-de-palencia/) | 1.066 | 28,0 % | 18,2 % | 83,6 % (641 de 767) |
| [Pontevedra](https://onubia.com/observatorio/provincia-de-pontevedra/) | 7.509 | 21,4 % | 14,3 % | 77,1 % (4.431 de 5.748) |
| [Salamanca](https://onubia.com/observatorio/provincia-de-salamanca/) | 2.974 | 24,7 % | 16,6 % | 77,6 % (1.684 de 2.170) |
| [Santa Cruz de Tenerife](https://onubia.com/observatorio/provincia-de-santa-cruz-de-tenerife/) | 8.550 | 27,8 % | 18,0 % | 84,2 % (5.049 de 5.998) |
| [Segovia](https://onubia.com/observatorio/provincia-de-segovia/) | 1.587 | 25,8 % | 17,7 % | 86,3 % (994 de 1.152) |
| [Sevilla](https://onubia.com/observatorio/provincia-de-sevilla/) | 12.793 | 26,7 % | 17,1 % | 81,7 % (7.604 de 9.304) |
| [Soria](https://onubia.com/observatorio/provincia-de-soria/) | 884 | 20,1 % | 16,0 % | 72,8 % (472 de 648) |
| [Tarragona](https://onubia.com/observatorio/provincia-de-tarragona/) | 6.643 | 26,6 % | 16,3 % | 79,5 % (3.874 de 4.873) |
| [Teruel](https://onubia.com/observatorio/provincia-de-teruel/) | 1.341 | 22,4 % | 13,0 % | 81,6 % (854 de 1.047) |
| [Toledo](https://onubia.com/observatorio/provincia-de-toledo/) | 4.561 | 26,2 % | 17,8 % | 83,6 % (2.749 de 3.288) |
| [Valencia](https://onubia.com/observatorio/provincia-de-valencia/) | 21.140 | 25,7 % | 16,0 % | 81,6 % (12.706 de 15.578) |
| [Valladolid](https://onubia.com/observatorio/provincia-de-valladolid/) | 3.879 | 22,6 % | 13,8 % | 81,0 % (2.417 de 2.984) |
| [Zamora](https://onubia.com/observatorio/provincia-de-zamora/) | 1.318 | 23,7 % | 15,7 % | 75,1 % (714 de 951) |
| [Zaragoza](https://onubia.com/observatorio/provincia-de-zaragoza/) | 6.418 | 24,9 % | 15,5 % | 77,6 % (3.716 de 4.789) |

### Las 30 ciudades con más webs medidas

| Dónde | Webs medidas | No cargan | Dominio perdido | Correo suplantable |
|---|---|---|---|---|
| [Madrid](https://onubia.com/observatorio/madrid/) | 27.740 | 25,9 % | 15,7 % | 82,4 % (16.447 de 19.958) |
| [Barcelona](https://onubia.com/observatorio/barcelona/) | 19.910 | 28,5 % | 16,1 % | 78,4 % (11.219 de 14.318) |
| [Valencia](https://onubia.com/observatorio/valencia/) | 9.154 | 26,7 % | 16,7 % | 82,2 % (5.463 de 6.650) |
| [Sevilla](https://onubia.com/observatorio/sevilla/) | 6.216 | 26,9 % | 16,9 % | 81,4 % (3.664 de 4.503) |
| [Málaga](https://onubia.com/observatorio/malaga/) | 5.272 | 25,6 % | 16,0 % | 78,7 % (3.056 de 3.881) |
| [Palma](https://onubia.com/observatorio/palma/) | 4.714 | 26,1 % | 15,9 % | 83,8 % (2.894 de 3.452) |
| [Zaragoza](https://onubia.com/observatorio/zaragoza/) | 4.655 | 24,7 % | 15,3 % | 76,8 % (2.669 de 3.474) |
| [Marbella](https://onubia.com/observatorio/marbella/) | 3.820 | 24,6 % | 15,3 % | 83,5 % (2.347 de 2.811) |
| [Alicante](https://onubia.com/observatorio/alicante/) | 3.690 | 24,1 % | 16,6 % | 81,8 % (2.179 de 2.664) |
| [Murcia](https://onubia.com/observatorio/murcia/) | 3.671 | 26,0 % | 17,6 % | 80,4 % (2.119 de 2.636) |
| [Granada](https://onubia.com/observatorio/granada/) | 3.143 | 24,8 % | 16,1 % | 81,5 % (1.838 de 2.256) |
| [Bilbao](https://onubia.com/observatorio/bilbao/) | 3.028 | 25,9 % | 15,8 % | 82,2 % (1.844 de 2.244) |
| [Córdoba](https://onubia.com/observatorio/cordoba/) | 2.712 | 23,9 % | 16,0 % | 77,8 % (1.595 de 2.051) |
| [Las Palmas de Gran Canaria](https://onubia.com/observatorio/las-palmas-de-gran-canaria/) | 2.649 | 27,3 % | 16,7 % | 83,9 % (1.618 de 1.928) |
| [Vigo](https://onubia.com/observatorio/vigo/) | 2.499 | 22,0 % | 14,4 % | 76,2 % (1.459 de 1.915) |
| [Valladolid](https://onubia.com/observatorio/valladolid/) | 2.437 | 22,7 % | 13,8 % | 82,5 % (1.554 de 1.883) |
| [A Coruña](https://onubia.com/observatorio/a-coruna/) | 2.421 | 24,3 % | 16,2 % | 81,8 % (1.452 de 1.774) |
| [Gijón](https://onubia.com/observatorio/gijon/) | 2.181 | 25,7 % | 16,0 % | 80,8 % (1.270 de 1.572) |
| [Elche](https://onubia.com/observatorio/elche/) | 2.006 | 24,0 % | 16,0 % | 77,6 % (1.159 de 1.493) |
| [Oviedo](https://onubia.com/observatorio/oviedo/) | 1.965 | 27,4 % | 18,3 % | 81,8 % (1.152 de 1.408) |
| [San Sebastián](https://onubia.com/observatorio/san-sebastian/) | 1.864 | 24,6 % | 13,9 % | 83,2 % (1.142 de 1.373) |
| [Santander](https://onubia.com/observatorio/santander/) | 1.831 | 29,1 % | 19,1 % | 81,5 % (1.033 de 1.268) |
| [Santa Cruz de Tenerife](https://onubia.com/observatorio/santa-cruz-de-tenerife/) | 1.695 | 27,0 % | 17,9 % | 83,2 % (1.007 de 1.211) |
| [Vitoria-Gasteiz](https://onubia.com/observatorio/vitoria-gasteiz/) | 1.676 | 24,0 % | 15,7 % | 84,0 % (1.055 de 1.256) |
| [Pamplona](https://onubia.com/observatorio/pamplona/) | 1.641 | 23,0 % | 15,1 % | 81,9 % (1.006 de 1.228) |
| [Salamanca](https://onubia.com/observatorio/salamanca/) | 1.623 | 25,1 % | 17,4 % | 75,9 % (890 de 1.173) |
| [Castellón de la Plana](https://onubia.com/observatorio/castellon-de-la-plana/) | 1.608 | 24,1 % | 14,7 % | 81,7 % (996 de 1.219) |
| [Burgos](https://onubia.com/observatorio/burgos/) | 1.564 | 22,9 % | 13,7 % | 79,9 % (956 de 1.197) |
| [Almería](https://onubia.com/observatorio/almeria/) | 1.478 | 26,9 % | 17,5 % | 78,9 % (844 de 1.070) |
| [Jerez de la Frontera](https://onubia.com/observatorio/jerez-de-la-frontera/) | 1.472 | 26,0 % | 17,1 % | 81,4 % (878 de 1.078) |
<!-- /respuestas -->

## Ficheros (`datos/`)
| Fichero | Contenido |
|---|---|
| `observatorio-espana.csv` | España, total y por sectores |
| `observatorio-ciudades.csv` | 696 ciudades |
| `observatorio-provincias.csv` | 51 provincias |
| `observatorio-espana-cruces.json` | Por qué no carga cada web caída, candado y correo por dentro, proveedores de correo, tamaño de ciudad, islas y terminaciones de dominio |
| `observatorio-correo-proveedores.csv` | Suplantación del correo por proveedor |
| `observatorio-por-dentro.csv` | Cada medida «por dentro» (mantenimiento, ley, accesibilidad, Google, dominio y velocidad) de España, provincias y ciudades |

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
