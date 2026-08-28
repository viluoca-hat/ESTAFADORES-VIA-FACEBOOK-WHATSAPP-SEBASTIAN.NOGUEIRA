
## 👤 Perfil del Agresor

### **SEBASTIAN.NOGUEIRA.5**

| Plataforma | Usuario / Perfil | Estado |
|------------|------------------|--------|
| **Facebook** | [SEBASTIAN.NOGUEIRA.5](https://www.facebook.com/sebastian.nogueira.5) | 🔴 ACTIVO |
| **WhatsApp** | [+54 9 375 6446868](https://wa.me/5493756446868) | 🔴 ACTIVO |
| **Mastodon** | [@sebastian.nogueira.5](https://mstdn.social/@sebastian.nogueira.5) | 🟡 ACTIVO |
| **Tistory** | sebastian.nogueira.5.tistory.com | 🟡 ACTIVO |
| **Salon24** | salon24.pl/u/sebastian.nogueira.5 | 🟡 ACTIVO |
| **Phase** | pbase.com/sebastian.nogueira.5 | 🟡 ACTIVO |
| **Championat** | championat.com/user/... | 🟡 ACTIVO |
| **Fixya** | fixya.com/users/... | 🟡 ACTIVO |
| **Wishlistr** | wishlistr.com/... | 🟢 ACTIVO |
| **Joyreactor** | joyreactor.cc/user/... | 🟡 ACTIVO |
| **Mamot** | mamot.fr/@... | 🟡 ACTIVO |
| **Pling** | pling.com/u/... | 🟡 ACTIVO |
| **Framapiaf** | framapiaf.org/@... | 🟡 ACTIVO |

### 📍 Ubicación Geográfica

- **País:** Argentina 🇦🇷
- **Provincia:** Misiones
- **Código de Área:** 375
- **Código Postal:** N3300 (Posadas)
- **Zona Horaria:** UTC-3

### 🏷️ Intereses Detectados (OSINT)

social · art · blog · forum · tech · coding · photo · sharing · sport · shopping · design · discussion · news · mastodon
text


### 🌍 Países Asociados

| País | Código | Evidencia |
|------|--------|-----------|
| 🇦🇷 Argentina | AR | Número de WhatsApp (+54 9 375 6446868) |
| 🇷🇺 Rusia | RU | Championat, Joyreactor |
| 🇫🇷 Francia | FR | Mamot, Framapiaf |
| 🇰🇷 Corea del Sur | KR | Tistory |
| 🇳🇱 Países Bajos | NL | Pling |
| 🇵🇱 Polonia | PL | Salon24 |

---

## 🔬 Metodología del Ataque

    Perfil falso contacta a víctima por WhatsApp
    ↓

    Envía imágenes JPEG manipuladas
    ↓

    Payload oculto en comentario (FF FE)
    ↓

    Payload cifrado (AES-256/ChaCha20)
    ↓

    Al abrir la imagen, explota CVE-2023-41064
    ↓

    Robo de datos sensibles del iPhone

text


### Detalles Técnicos

```bash
# Firmas de WhatsApp encontradas
WA          # WhatsApp
WatsA       # WhatsApp (ofuscado)
wapr        # WhatsApp
WA2;        # WhatsApp (ofuscado)
wAP9:       # WhatsApp (ofuscado)

# Marcadores JPEG sospechosos
FF FE       # Comentario JPEG (payload oculto)
FF D9       # Fin de imagen (datos extra entre marcadores)

# Patrones de ofuscación
UUUU · YYYY · ++++ · ]]]]

🛡️ Vulnerabilidades Explotadas
CVE	Descripción	Versión Afectada	Estado
CVE-2023-41064	Image I/O Vulnerability	iOS 16.6.1 y anteriores	🔴 EXPLOTADO
CVE-2021-30761	Image I/O Vulnerability	iOS 14.5 y anteriores	🟡 POSIBLE
CVE-2020-27932	Image I/O Vulnerability	iOS 14.0 y anteriores	🟡 POSIBLE
Versiones de iOS Afectadas

    🔴 iOS 16.6.1 o anterior (Vulnerable a CVE-2023-41064)

    🟡 iOS 14.5 o anterior

    🟡 iOS 14.0 o anterior

    🟢 iOS 17.0 o superior (Parcheado)

📂 Estructura del Repositorio
text

📁 CyberForensic-WhatsApp-Phishing/
│
├── 📄 README.md                    # Este archivo
├── 📄 index.html                   # Reporte visual (GitHub Pages)
├── 📄 cristian.png                 # Foto del perfil fraudulento
│
├── 📁 evidence/                    # EVIDENCIA PRINCIPAL
│   ├── 📁 images/                  # Imágenes originales (con payload)
│   │   ├── 1.jpeg                  # Imagen maliciosa 1
│   │   └── 2.jpeg                  # Imagen maliciosa 2
│   │
│   ├── 📁 extracted/               # Archivos extraídos
│   │   ├── extracted_1.zip         # ZIP cifrado 1
│   │   ├── extracted_2.zip         # ZIP cifrado 2
│   │   ├── payload_1_real.bin      # Payload cifrado 1
│   │   └── payload_2_real.bin      # Payload cifrado 2
│   │
│   └── 📄 hashes.txt               # Hashes de verificación
│
├── 📁 forensic/                    # ANÁLISIS FORENSE
│   ├── 📄 iocs.txt                 # Indicadores de compromiso
│   └── 📄 mitre_attck.txt          # Mapeo MITRE
│
└── 📁 scripts/                     # HERRAMIENTAS
    ├── 📄 extract_payload.sh       # Script de extracción
    ├── 📄 xor_decrypt.py           # Script de desofuscación
    └── 📄 aes_decrypt.py           # Script de descifrado

📊 Evidencia Técnica
Hashes de Archivos
Archivo	SHA-256
1.jpeg	1b735d07eee0c3cd65efafcfd2c846da91c393a1d7a5fc1c06d0dd33783d9a24
2.jpeg	26ab086f6fb8bb513740e85367a2d29865264f195d4ad676a371d49cc66cedd8
payload_1_real.bin	7d3905931674645efa429e6297ce34135d4cfb1cf9fc50f3ae5c307ee36cd07d
payload_2_real.bin	f703bd3dcae559baf277ab0f11170c6b2cf63b7b10cae2b36e8012328bb92b78
MD5 Hashes
Archivo	MD5
1.jpeg	1cd8636004a400e5ae1d059044f42504
2.jpeg	bd9449b4a7cdbfc7123a7489e169d961
payload_1_real.bin	c97eb5f7e702ba63f47c63cd951691e7
payload_2_real.bin	5b2be0e136db3a1d2707f00414ec1aa0
🔍 Cómo Analizar las Imágenes
1. Clonar el repositorio
bash

git clone https://github.com/CyberForensicTeam/CyberForensic-WhatsApp-Phishing.git
cd CyberForensic-WhatsApp-Phishing

2. Instalar herramientas forenses
bash

# En Debian/Ubuntu/MX Linux
sudo apt update
sudo apt install steghide binwalk exiftool hexdump strings xxd file

# En macOS
brew install steghide binwalk exiftool

# En Windows (WSL)
sudo apt install steghide binwalk exiftool

3. Extraer el payload oculto
bash

# Usar el script incluido
cd evidence/images
bash ../../scripts/extract_payload.sh

# O manualmente:
# Buscar marcador FF FE
hexdump -C 1.jpeg | grep "ff fe"
# Extraer desde la posición encontrada
dd if=1.jpeg bs=1 skip=<POSICION> of=payload_1.bin

4. Analizar con herramientas forenses
bash

# Ver metadatos
exiftool 1.jpeg

# Buscar archivos ocultos
binwalk 1.jpeg

# Intentar extraer con steghide (requiere contraseña)
steghide extract -sf 1.jpeg

# Buscar strings sospechosos
strings -n 10 1.jpeg | grep -E "WA|WatsA|wapr"

5. Intentar crackear los ZIPs
bash

# Generar hash
zip2john extracted_1.zip > hash.txt

# Crackear con diccionario
john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt

# O con SecLists
john --wordlist=./SecLists/Passwords/Common-Credentials/10-million-password-list-top-1000.txt hash.txt

🎯 MITRE ATT&CK Matrix
Táctica	Técnica	ID
Acceso Inicial	Phishing (Ingeniería Social)	T1566
Ejecución	Ejecución por Usuario	T1204
Persistencia	Arranque Automático	T1547
Evasión	Ofuscación de Archivos	T1027
Descubrimiento	Archivos Locales	T1005
Recolección	Captura de Pantalla	T1113
Exfiltración	C2 Channel	T1041
Comando y Control	Protocolo de Aplicación	T1071
🚨 Indicadores de Compromiso (IOCs)
Archivos Maliciosos
bash

1.jpeg (SHA256: 1b735d07eee0c3cd65efafcfd2c846da91c393a1d7a5fc1c06d0dd33783d9a24)
2.jpeg (SHA256: 26ab086f6fb8bb513740e85367a2d29865264f195d4ad676a371d49cc66cedd8)
extracted_1.zip (156 KB - Cifrado)
extracted_2.zip (224 KB - Cifrado)
payload_1_real.bin (92 KB - Cifrado)
payload_2_real.bin (96 KB - Cifrado)

Patrones Detectados
bash

Firmas WhatsApp: WA, WatsA, wapr, WA2;, wAP9:
Marcadores JPEG: FF FE (Comentario), FF D9 (Fin)
Ofuscación: UUUU, YYYY, ++++, ]]]]
Entropía: Alta (datos cifrados)

Perfiles Asociados
bash

Facebook: SEBASTIAN.NOGUEIRA.5 (UID: 1404815593)
WhatsApp: +54 9 375 6446868
Mastodon: @sebastian.nogueira.5
Tistory: sebastian.nogueira.5.tistory.com
Salon24: salon24.pl/u/sebastian.nogueira.5

🛡️ Recomendaciones de Seguridad
Para Usuarios de iPhone

    ✅ ACTUALIZAR iOS a la última versión (17.x o superior)

    ✅ NO ABRIR imágenes de perfiles desconocidos

    ✅ VERIFICAR perfiles antes de interactuar

    ✅ REPORTAR perfiles sospechosos en WhatsApp

    ✅ ACTIVAR autenticación en dos pasos

    ✅ CAMBIAR contraseñas regularmente

Si Has Recibido Imágenes Sospechosas

    🚫 NO ABRIR las imágenes

    🚫 NO HACER CLICK en ningún enlace

    📱 REPORTAR el perfil en WhatsApp

    💾 GUARDAR los archivos como evidencia

    👮 CONTACTAR a la policía cibernética

    📢 COMPARTIR esta alerta con otros

📞 Contactos de Emergencia
🇦🇷 Argentina
Institución	Contacto
Unidad Fiscal de Ciberdelincuencia	(011) 5071-0000
Policía Federal - División Ciberdelitos	0800-666-5082
Gendarmería Nacional	130
Línea de Denuncias	134
🌐 Internacional
Institución	Contacto
INTERPOL - Ciberdelincuencia	https://www.interpol.int
Europol - EC3	https://www.europol.europa.eu
📄 Licencia

Este material está licenciado bajo Creative Commons Attribution-NonCommercial 4.0.
⚠️ ADVERTENCIA LEGAL

Este repositorio y su contenido son de carácter informativo y educativo. La información aquí presentada corresponde a evidencia real de un ataque de phishing documentado. NO se debe utilizar esta información para actividades ilegales.

Toda la información ha sido recopilada con fines de investigación y denuncia ante las autoridades competentes.
📊 Estadísticas del Ataque
yaml

Fecha del Incidente: 2026-08-28
Tiempo de Análisis: 6 horas
Archivos Analizados: 8
Payload Encontrado: SI (92-96 KB)
Nivel de Riesgo: CRÍTICO 🔴
Estado: En Investigación
Víctima: Sebastián Nogueira
Dispositivo: iPhone 11
Sistema Operativo: iOS 16.6.1

🔗 Enlaces Rápidos

    📱 WhatsApp del Agresor

    🌐 Perfil Facebook

    🐘 Mastodon

    📝 Tistory

    📝 Salon24

🤝 Contribuir

Si eres investigador forense, experto en seguridad o tienes información relevante:

    Haz un fork del repositorio

    Crea una rama con tu análisis

    Envía un Pull Request

O contáctanos directamente:

    📧 Email: sebastian.nogueira@protonmail.com

    📱 WhatsApp: +54 9 375 6446868

    🐦 Twitter: @CyberAlert_AR

Última Actualización: 28 de agosto de 2026
Estado: 🔴 ACTIVE INVESTIGATION
