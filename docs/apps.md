# Configurar Topotresc para aplicaciones

Es posible configurar Topotres como fuente de mapas de muchas aplicaciones móviles y de escritorio que permites fuentes online (WMS).

Instrucciones para configurar Topotres en:

- [QMapShack](#QMapShack)  ( Windows / Mac / Linux )
- [Gurumaps](#Gurumaps) ( IOS: Iphone, IPAD... )
- [Oruxmaps](#Oruxmaps) ( Android )
- [OsmAnd](#OsmAnd) ( Android / IOS: Iphone, IPAD... )
- [MapPlus](#MapPlus) ( Android / IOS: Iphone, IPAD... )
- [MOBAC, SASPlanet, QGIS](#MOBAC) ( Windows / Mac / Linux )
- [TwoNav Land](#Land) ( Windows / Mac )

En general es posible configurar cualquier aplicación que adminta fuentes de mapa online WMS ajustando en la configuración la siguiene URL: ```https://api.topotresc.com/tiles/{z}/{x}/{y}```

## QMapShack {#QMapShack}
Descargar el archivo TMS y copiarlo en la carpeta de mapas de QMapShack: [topotresc_cat_piri.tms](topotresc_cat_piri.tms)

Mas detalles en https://github.com/Maproom/qmapshack/wiki/DocQuickStartSpanish  *Configurar carpetas de mapas*


## Gurumaps {#Gurumaps}
Cargar en la aplicación el siguiente archivo XML: [topotresc_cat_piri.xml](topotresc_cat_piri.xml)

Para enviar o cargar el archivo en la aplicación tenemos varias opciones.
- Al descargar cuando pregunta que hacer con el archivo seleccionar: "enviar a" y seleccionar Gurumaps.
- Enviarnos el archivo por correo a nosotros mismos, abrir el adjunto desde el móvil y seleccionar "enviar a" Gurumaps.

## Oruxmaps {#Oruxmaps}
Copiar el siguiente archivo: [onlinemapsources.xml](onlinemapsources.xml) en la carpeta del móvil:

```Almacenamiento interno compartido\oruxmaps\mapfiles\customonlinemaps\```

En caso de que ya tengas el archivo XML con otros mapas, editarlo y insertar esto justo antes de la ultima linea:
```
<onlinemapsource uid="701">
<name>Topotresc (PIRI)</name>
<url><![CDATA[https://topotresc.com/osm_tiles/{$z}/{$x}/{$y}.png]]></url>
<website><![CDATA[<a href="https://topotresc.com</a>]]></website>
<minzoom>7</minzoom>
<maxzoom>17</maxzoom>
<projection>MERCATORESFERICA</projection>
<servers></servers>
<httpparam name="User-Agent">{om}</httpparam>
<cacheable>1</cacheable>
<downloadable>1</downloadable>
<maxtilesday>0</maxtilesday>
<maxthreads>0</maxthreads>
```

## OsmAnd {#OsmAnd}
Cargar en la aplicación el siguiente archivo XML: [topotresc_cat_piri.xml](topotresc_cat_piri.xml)
En ios (iphone) para enviar o cargar el archivo en la aplicación tenemos varias opciones.
- Al descargar cuando pregunta que hacer con el archivo seleccionar: "enviar a" y seleccionar OsmAnd.
- Enviarnos el archivo por correo a nosotros mismos, abrir el adjunto desde el móvil y seleccionar "enviar a" OsmAnd.

## MapPlus {#MapPlus}
Cargar en la aplicación el siguiente archivo XML: [topotresc_cat_piri.xml](topotresc_cat_piri.xml)
En ios (iphone) para enviar o cargar el archivo en la aplicación tenemos varias opciones.
- Al descargar cuando pregunta que hacer con el archivo seleccionar: "enviar a" y seleccionar MapPlus.
- Enviarnos el archivo por correo a nosotros mismos, abrir el adjunto desde el móvil y seleccionar "enviar a" MapPlus.


## MOBAC, SASPlanet, QGIS {#MOBAC}
Ajustar o añadir en la respectiva configuración de mapas online la siguiente URL: ```https://api.topotresc.com/tiles/{z}/{x}/{y}```

## TwoNav Land {#Land}
Cargar el siguiente archivo de configuración: [Topotresc.cosm](Topotresc.cosm) 