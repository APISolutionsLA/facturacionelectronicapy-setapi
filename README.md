# Facturación Electrónica - Api SET
API de comunicación con la SET - Subsecretaría de estado de Tributación, para envío de los documentos electrónicos y consultas de datos de Facturas electrónicas.

## Instalación

```
$ npm install facturacionelectronicapy-setapi
```

## Envio de Documento de forma Síncrona

TypeScript:
```typescript
import setApi from 'facturacionelectronicapy-setapi';

setApi
.recibe(id, xmlSigned, env = "test" | "prod", cert_path, key)
.then(xml => console.log("XML con QR", xml));

```

## Envio de Documento de forma Asíncrona, por lotes

TypeScript:
```typescript
import setApi from 'facturacionelectronicapy-setapi';

setApi
.recibeLote(id, xmlSigned[], env = "test" | "prod", cert_path, key)
.then(xml => console.log("XML con QR", xml));

```
## Envio de evento a la SET

TypeScript:
```typescript
import setApi from 'facturacionelectronicapy-setapi';

setApi
.evento(id, xmlSigned, env = "test" | "prod", cert_path, key)
.then(xml => console.log("XML con QR", xml));

```
## Consulta de Documentos electrónicos desde la SET

TypeScript:
```typescript
import setApi from 'facturacionelectronicapy-setapi';

setApi
.consulta(id, cdc, env = "test" | "prod", cert_path, key)
.then(xml => console.log("XML con QR", xml));

```
## Consulta de RUC

TypeScript:
```typescript
import setApi from 'facturacionelectronicapy-setapi';

setApi
.consultaRuc(id, ruc, env = "test" | "prod", cert_path, key)
.then(xml => console.log("XML con QR", xml));

```
## Consulta de Lote

TypeScript:
```typescript
import setApi from 'facturacionelectronicapy-setapi';

setApi
.consultaLote(id, numeroLote, env = "test" | "prod", cert_path, key)
.then(xml => console.log("XML con QR", xml));

```

Para saber como generar el Archivo XML visita éste proyecto de Git: 
https://github.com/marcosjara/facturacionelectronicapy-xmlgen
