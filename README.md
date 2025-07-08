# Transferencia-al-911
Transferencia911 es un sistema de defensa para usuarios de Bitcoin que, al firmar con una clave de pánico, redirige los fondos a una billetera segura y activa una alerta silenciosa tipo 911. Ideal para situaciones de coacción, secuestro o amenaza, combinando seguridad on-chain con respuestas de emergencia.


📁 Estructura del Repositorio Transferencia911

Transferencia911/
├── README.md
├── Transferencia911.md
├── LICENSE
├── docs/
│   ├── arquitectura.md
│   ├── flujo-de-alerta.png
│   └── caso-de-uso.pdf
├── src/
│   ├── wallet/
│   │   ├── duress_signer.py
│   │   ├── tx_builder.py
│   │   └── bitcoin_script_templates.py
│   ├── backend/
│   │   ├── api.py
│   │   ├── alert_engine.py
│   │   └── geolocation_tools.py
│   └── integrations/
│       ├── sms_twilio.py
│       ├── email_alert.py
│       └── 911_api_stub.py
├── config/
│   └── settings.env
├── tests/
│   ├── test_signer.py
│   ├── test_alert_trigger.py
│   └── test_integration.py
└── .gitignore


---

📝 README.md

# 🚨 Transferencia911 – Protocolo de Emergencia Criptográfica

**Transferencia911** es una solución de seguridad extrema que integra **Bitcoin**, **claves de coacción (duress keys)** y **alertas automatizadas a servicios de emergencia (911)**. Está diseñada para situaciones en las que el usuario es forzado a realizar una transacción bajo amenaza.

---

## 🎯 Objetivo

Permitir que una transacción ejecutada bajo coacción:
1. Redirija automáticamente los fondos a una billetera segura.
2. Active una **alerta silenciosa** hacia entidades como el 911, familiares o nodos guardianes.

---

## ⚙️ ¿Cómo Funciona?

1. El usuario configura una wallet con una clave de pánico.
2. Al usar esta clave, se firma una transacción que:
   - Envía los bitcoins a una dirección de resguardo.
   - Dispara automáticamente una señal a:
     - APIs policiales (911)
     - Nodos descentralizados (Panic DAO)
     - Familiares o guardianes vía SMS/Email/Push
     - Grabaciones o rastreos automáticos

---

## 🧠 Componentes Clave

- `wallet/duress_signer.py`: Firma con lógica de coacción.
- `backend/alert_engine.py`: Generador y despachador de alertas.
- `integrations/911_api_stub.py`: Simula la conexión con centrales reales.
- `sms_twilio.py`: Envío de mensajes SMS de emergencia.
- `geolocation_tools.py`: Determina ubicación aproximada del dispositivo.

---

## 📦 Requisitos

- Python 3.11+
- Node.js (opcional, para UI)
- API Key de Twilio o servidor SMTP
- Red Tor o VPN para proteger tráfico
- Dispositivo con conexión a internet y compatibilidad Bitcoin

---

## 🚀 Cómo Ejecutarlo

```bash
git clone https://github.com/lerryalexanderelizondo/Transferencia911.git
cd Transferencia911
pip install -r requirements.txt
python src/backend/api.py

Prueba local:

curl -X POST http://localhost:5000/alerta \
  -d '{"tipo":"911", "txid":"xyz123", "ubicacion":"auto"}'


---

🧪 Casos de Uso

Coacción física directa

Amenaza digital

Vigilancia gubernamental opresiva

Protección de custodios y líderes cripto



---

🔐 Filosofía

> Si vas a morir por Bitcoin, que al menos sea con estilo y protección.
— LAEV




---

👥 Créditos

Desarrollado por LAEV y el Cartel de Bitcoiners.

Inspirado en la necesidad real de defensa cripto en contextos extremos.



---

📜 Licencia

MIT License — Libre para modificar, usar y mejorar.

