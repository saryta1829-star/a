
# Axiom Core // Autonomous Distributed Expert System & P2P Mesh Observatory

[![Build Status](https://img.shields.io/badge/build-passing-00f2fe?style=flat-square&logo=github-actions)](https://github.com/)
[![Android API](https://img.shields.io/badge/Android-API%2034%20(UpsideDownCake)-3ddc84?style=flat-square&logo=android)](https://developer.android.com/)
[![Inference Engine](https://img.shields.io/badge/engine-Compiled%20Rete-00f2fe?style=flat-square)](https://github.com/)
[![Latency](https://img.shields.io/badge/latency-1.2ms%20avg-00f2fe?style=flat-square)](https://github.com/)
[![Cryptography](https://img.shields.io/badge/crypto-Ed25519%20%7C%20Zero--RTT-ff007f?style=flat-square)](https://github.com/)
[![Mesh Transport](https://img.shields.io/badge/mesh-QUIC%20%2B%20LoRa%20Sub--GHz-00f2fe?style=flat-square)](https://github.com/)
[![Memory Footprint](https://img.shields.io/badge/RAM-%3C%2012%20MB-success?style=flat-square)](https://github.com/)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue?style=flat-square)](LICENSE)

> **Axiom Core** traslada la capacidad analÃ­tica y deductiva de misiÃ³n crÃ­tica directamente al borde operativo (*edge*). Integra un motor de inferencia formal de alto rendimiento basado en el algoritmo **Rete**, ejecutÃ¡ndose de forma determinista y 100% *offline-first* sobre una red en malla descentralizada P2P (QUIC, Wi-Fi Direct y LoRa Sub-GHz).

---

## âš¡ CaracterÃ­sticas Principales

- **Motor de Inferencia Rete Compilado**:
  - EvaluaciÃ³n de patrones lÃ³gicos en microsegundos (<1.2 ms latencia promedio).
  - Trazabilidad y explicabilidad en caliente (*Explainable AI / "Why?" justification*).
  - Factores de certidumbre formalizados ($CF \in [-1.0, 1.0]$) y desempate por *Salience / Recency*.
- **Arquitectura de Memoria de Trabajo**:
  - Hechos dinÃ¡micos con linaje causal inmutable y verificaciÃ³n criptogrÃ¡fica.
  - ResoluciÃ³n determinista de conflictos en la agenda de disparos.
- **Enlace de Comunicaciones Mesh & P2P**:
  - Protocolo Gossip de auto-descubrimiento y enrutamiento ad-hoc *zero-configuration*.
  - ModulaciÃ³n multi-capa: paquetes binarios compactos sobre **LoRa (868/915 MHz)** y **QUIC / TLS 1.3**.
  - AutenticaciÃ³n criptogrÃ¡fica asimÃ©trica **Ed25519** y cifrado simÃ©trico ChaCha20-Poly1305.
- **Cliente Nativo Android**:
  - Arquitectura desacoplada empaquetada vÃ­a Capacitor / Android Native API 34.
  - Huella de memoria mÃ­nima (<12 MB RAM), ideal para dispositivos embebidos o terminales tÃ¡cticos de campo.
  - Despliegue *air-gapped* mediante cÃ³digos QR y manifiestos de auditorÃ­a en JSON/YAML.

---

## ðŸ›ï¸ Arquitectura del Sistema

```
  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
  â”‚                 AXIOM CORE RUNTIME KERNEL                   â”‚
  â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
                                 â”‚
         â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”´â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
         â–¼                                               â–¼
â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”                           â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
â”‚ KNOWLEDGE BASE   â”‚                           â”‚ WORKING MEMORY   â”‚
â”‚ - SI-ENTONCES    â”‚                           â”‚ - Hechos WME     â”‚
â”‚ - Certidumbre CF â”‚                           â”‚ - Linaje Causal  â”‚
â””â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜                           â””â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
         â”‚                                              â”‚
         â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
                                 â–¼
                    â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
                    â”‚    INFERENCE ENGINE     â”‚
                    â”‚   (Alpha & Beta Rete)   â”‚
                    â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
                                 â”‚
                                 â–¼
                    â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
                    â”‚     AGENDA & CONFLICT   â”‚
                    â”‚       RESOLUTION        â”‚
                    â”‚  (Salience / Recency)   â”‚
                    â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
                                 â”‚
         â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”´â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
         â–¼                                               â–¼
â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”                           â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
â”‚ P2P GOSSIP MESH  â”‚                           â”‚ AUDIT & EXPORT   â”‚
â”‚ - LoRa Sub-GHz   â”‚                           â”‚ - JSON / YAML    â”‚
â”‚ - QUIC / TLS 1.3 â”‚                           â”‚ - Firma Ed25519  â”‚
â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜                           â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
```

---

## ðŸ“‚ Estructura del Repositorio

```bash
axiom-core/
â”œâ”€â”€ android/                   # Proyecto nativo Gradle / Android API 34
â”‚   â”œâ”€â”€ app/src/main/
â”‚   â”‚   â”œâ”€â”€ AndroidManifest.xml
â”‚   â”‚   â””â”€â”€ java/org/axiom/core/
â”œâ”€â”€ engine/                    # NÃºcleo del Motor de Inferencia (Rete)
â”‚   â”œâ”€â”€ compiler/              # Compilador de reglas y grafos de decisiÃ³n
â”‚   â”œâ”€â”€ memory/                # Hechos WME y gestiÃ³n de memoria de trabajo
â”‚   â””â”€â”€ agenda/                # PriorizaciÃ³n por Salience / Recency
â”œâ”€â”€ mesh/                      # Capa de Telecomunicaciones P2P
â”‚   â”œâ”€â”€ gossip/                # Protocolo de sincronizaciÃ³n de estado
â”‚   â”œâ”€â”€ crypto/                # Firmas Ed25519 y envelopes ChaCha20
â”‚   â””â”€â”€ drivers/               # Adaptadores LoRa PHY y sockets QUIC
â”œâ”€â”€ knowledge-base/            # DefiniciÃ³n formal de ontologÃ­as y axiomas
â”‚   â”œâ”€â”€ rules/                 # Reglas declarativas en formato YAML/JSON
â”‚   â””â”€â”€ schema/                # ValidaciÃ³n formal de esquemas
â”œâ”€â”€ web-ui/                    # Interfaz tÃ¡ctica (Deep Observatory UI)
â”‚   â”œâ”€â”€ src/
â”‚   â””â”€â”€ capacitor.config.json
â”œâ”€â”€ docs/                      # EspecificaciÃ³n tÃ©cnica y diagramas
â”œâ”€â”€ README.md                  # Este documento
â””â”€â”€ LICENSE
```

---

## ðŸš€ Inicio RÃ¡pido (Quickstart)

### Prerrequisitos
- Node.js >= 18.x
- JDK 17 (OpenJDK recomendado)
- Android SDK (API Level 34)

### 1. Clonar e Instalar Dependencias
```bash
git clone https://github.com/axiom-core/axiom-core.git
cd axiom-core
npm install
```

### 2. Ejecutar SimulaciÃ³n del Motor en Modo Desarrollo
```bash
npm run dev
# Acceso en http://localhost:5173 para el simulador y la consola de inferencia
```

### 3. Compilar y Sincronizar para Android
```bash
npm run build
npx cap sync android
```

### 4. Generar APK Firmado para Despliegue de Campo
```bash
cd android
./gradlew assembleRelease
# El artefacto se genera en: android/app/build/outputs/apk/release/axiom-core-v4.8.apk
```

---

## ðŸ“œ Formato de Reglas (JSON / YAML)

Las reglas del sistema experto se definen bajo un esquema declarativo estricto:

```yaml
rule_id: "RULE_TEMP_PRESSURE_EMERGENCY"
salience: 90
certainty_factor: 0.98
conditions:
  - fact: "sensor.temperature"
    operator: ">"
    threshold: 85.0
    unit: "celsius"
  - fact: "sensor.hydraulic_pressure"
    operator: ">"
    threshold: 4.2
    unit: "bar"
actions:
  - assert: "state.isolation_valve_04 = ISOLATED"
  - emit_gossip:
      topic: "emergency.containment"
      priority: "CRITICAL"
explanation: "Riesgo inminente de sobrepresiÃ³n tÃ©rmica; se activa aislamiento automÃ¡tico."
```

---

## ðŸ›¡ï¸ Seguridad y Air-Gapped Operation

Axiom Core estÃ¡ diseÃ±ado para entornos electromagnÃ©ticamente adversos y redes sin salida a Internet (*air-gapped*):
- **Cero telemetrÃ­a a la nube**: NingÃºn dato sensible sale del enjambre local.
- **Anti-tamper**: Cada deducciÃ³n registrada en el historial incluye el hash SHA-256 de los hechos de entrada y la firma del nodo emisor.

---

## ðŸ“„ Licencia

Este proyecto estÃ¡ licenciado bajo los tÃ©rminos de la Licencia **Apache 2.0**. Consulte el archivo [LICENSE](LICENSE) para mÃ¡s detalles.