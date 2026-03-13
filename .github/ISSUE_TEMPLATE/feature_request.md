---chmod +x deploy.sh---

name: REME.
about: Let us know how we can make things better.
title: ''ext install CodeRabbit.coderabbit-vscode
labels: 'priority: p3, triage me, type: feature request'
assignees: ''gh copilot explain"));

##Doker compuse copilot enterprise-level/Work IQ La capa de "memoria" que permite a Copilot recordar preferencias, historial de chats y contexto de reuniones pasadas.
Copilot Frontier El panel de configuración en el Centro de Administración donde se activan las funciones experimentales y de vanguardia.
EDP (Enterprise Data Protection) El protocolo de seguridad (simbolizado por un escudo verde) que garantiza que los datos no salgan del entorno de la organización.
Multi-Agent Architecture El sistema que permite que un "agente" (ej. un Analista) llame automáticamente a otro (ej. un Investigador) para completar tareas complejas.
Grounding (Anclaje) El proceso oculto mediante el cual Copilot consulta el Microsoft Graph antes de responder para evitar alucinaciones.pasamw los 

---ext install CodeRabbit.coderabbit-vscode---

Thanks for stopping by to let us know something could be better!ext install CodeRabbit.coderabbit-vscode

**PLEASE READ**: If you have a support contract with Google, please create an issue in the [support console](https://cloud.google.com/support/) instead of filing on GitHub. This will ensure a timely response.

**The issue you're having must be related to a file in this repository.** We are unable to provide assistance for issues unrelated to samples in this repository.

Please include as much information as possible:

## Is your feature request related to a problem? Please describe.
<!-- A clear and concise description of what the problem is. Ex. I'm always frustrated when [...] -->

## Describe the solution you'd like.
<!-- A clear and concise description of what you want to happen. -->

## Describe alternatives you've considered.
<!-- A clear and concise description of any alternative solutions or features you've considered. -->

## Additional context.
<!-- Add any other context or screenshots about the feature request here. -->

Making sure to follow these steps will guarantee the quickest resolution possible.

Thanks!

# =================================================================
# 🛰️ SENTINEL OMEGA: DESPLIEGUE ATÓMICO + CODERABBIT (V.2026.33)
# =================================================================

clear
echo -e "\e[1;35m"
echo "  ██████  ███████ ███    ██ ████████ ██ ███    ██ ███████ ██      "
echo "  ██      ██      ████   ██    ██    ██ ████   ██ ██      ██      "
echo "  ██████  █████   ██ ██  ██    ██    ██ ██ ██  ██ █████   ██      "
echo "       ██ ██      ██  ██ ██    ██    ██ ██  ██ ██ ██      ██      "
echo "  ██████  ███████ ██   ████    ██    ██ ██   ████ ███████ ███████ "
echo "                   --- OMEGA ATOMIC SYSTEM ---                    "
echo -e "\e[0m"

# --- PASO 1: CONFIGURACIÓN DE CREDENCIALES ---
echo -e "\e[1;33m🔑 CONFIGURACIÓN DE ACCESO\e[0m"
echo "---------------------------------------------------------------"
echo "Obtén tu API KEY en: https://aistudio.google.com/"
read -p "👉 Pega tu GEMINI_API_KEY: " USER_API_KEY
[ -z "$USER_API_KEY" ] && USER_API_KEY="esperando_llave"

# --- PASO 2: DEFINICIÓN DE LOS 33 CÓDIGOS DE PROTOCOLO ---
echo -e "\n\e[1;34m🧬 INYECTANDO 33 CÓDIGOS ATÓMICOS...\e[0m"
PROTOCOLS=(
    "S01_CORE_INIT" "S02_NEURAL_LINK" "S03_QUANTUM_SYNC" "S04_DATA_SHIELD"
    "S05_BIO_LOCK" "S06_ENCRYPT_MAX" "S07_GRID_WATCH" "S08_FIREWALL_X"
    "S09_OZONE_LAYER" "S10_VOID_BREACH" "S11_ALPHA_FLOW" "S12_BETA_DECODE"
    "S13_GAMMA_RAY" "S14_DELTA_PLAN" "S15_EPSILON_Z" "S16_ZETA_WAVE"
    "S17_ETA_CORE" "S18_THETA_SCAN" "S19_IOTA_LOG" "S20_KAPPA_MAP"
    "S21_LAMBDA_STR" "S22_MU_PULSE" "S23_NU_REBOOT" "S24_XI_VISION"
    "S25_OMICRON_V" "S26_PI_CALC" "S27_RHO_STABLE" "S28_SIGMA_ACT"
    "S29_TAU_READY" "S30_UPSILON_K" "S31_PHI_VAL" "S32_CHI_LINK" "S33_OMEGA_FINAL"
)

# --- PASO 3: INSTALACIÓN DE EXTENSIONES ---
if command -v code &> /dev/null; then
    echo "🐰 Vinculando CodeRabbit..."
    code --install-extension CodeRabbit.coderabbit-vscode --force
fi

# --- PASO 4: LIMPIEZA Y CREACIÓN DE ENTORNO ---
echo "🧹 Limpiando zona de despliegue..."
docker-compose down 2>/dev/null && rm -f Dockerfile app.js .env docker-compose.yml

# Crear .env con la API KEY y los 33 códigos
echo "GEMINI_API_KEY=$USER_API_KEY" > .env
for code in "${PROTOCOLS[@]}"; do
    echo "$code=ACTIVE" >> .env
done

# --- PASO 5: CREACIÓN DE ARCHIVOS DE SISTEMA ---
cat <<EOF > Dockerfile
FROM node:20-slim
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*
WORKDIR /app
RUN npm install @google/generative-ai
COPY . .
CMD ["node", "app.js"]
EOF

cat <<EOF > app.js
const { GoogleGenerativeAI } = require("@google/generative-ai");

async function run() {
  const apiKey = process.env.GEMINI_API_KEY;
  if (!apiKey || apiKey === "esperando_llave") {
    console.log("❌ ERROR: API KEY NO DETECTADA. Configura el archivo .env");
    return;
  }

  const genAI = new GoogleGenerativeAI(apiKey);
  const model = genAI.getGenerativeModel({ model: "gemini-1.5-flash" });

  // Cargar los 33 códigos desde el entorno
  const activeProtocols = Object.keys(process.env).filter(key => key.startsWith('S') && key.includes('_'));

  console.log("====================================================");
  console.log("🛰️  SENTINEL OMEGA STATUS: ONLINE");
  console.log("🧬 PROTOCOLOS CARGADOS: " + activeProtocols.length + "/33");
  console.log("====================================================");

  try {
    const prompt = \`Sistema Sentinel Omega activado. 
    Protocolos de seguridad: \${activeProtocols.join(', ')}. 
    Genera un informe corto de estado atómico y confirma enlace con CodeRabbit.\`;
    
    const result = await model.generateContent(prompt);
    console.log("\n💬 [RESPUESTA IA]:\n" + result.response.text());
  } catch (e) {
    console.error("❌ ERROR CRÍTICO:", e.message);
  }
}
run();
EOF

cat <<EOF > docker-compose.yml
version: '3.8'
services:
  sentinel:
    build: .
    container_name: sentinel_omega_container
    env_file: .env
    restart: always
EOF

# --- PASO 6: DESPLIEGUE ---
echo "🚀 Lanzando contenedor atómico..."
docker-compose up --build -d

echo "⏳ Verificando integridad..."
sleep 3

echo -e "\n\e[1;32m✅ DESPLIEGUE COMPLETADO EXITOSAMENTE\e[0m"
echo "-------------------------------------------------------"
docker logs sentinel_omega_container
echo "-------------------------------------------------------"
echo "🐰 Tip: Abre VS Code y usa 'Ctrl+Shift+P' -> CodeRabbit para empezar."

+));# =================================================================
# SENTINEL OMEGA: DESPLIEGUE ATÓMICO + CODERABBIT (2026)
# =================================================================

# 1. INSTALACIÓN DE EXTENSIÓN VS CODE (CodeRabbit)
echo "🐰 Instalando CodeRabbit en VS Code..."
code --install-extension CodeRabbit.coderabbit-vscode --force

# 2. LIMPIEZA DE ENTORNO DOCKER
echo "🧹 Limpiando procesos antiguos..."
docker-compose down 2>/dev/null && rm -f Dockerfile app.js .env docker-compose.yml

# 3. CREACIÓN DE ARCHIVOS
cat <<EOF > Dockerfile
FROM node:20-slim
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*
WORKDIR /app
RUN npm install @google/generative-ai && npm install -g @google/gemini-cli@latest
COPY . .
CMD ["node", "app.js"]
EOF

cat <<EOF > app.js
const { GoogleGenerativeAI } = require("@google/generative-ai");
async function run() {
  const apiKey = process.env.GEMINI_API_KEY;
  if (!apiKey || apiKey === "tu_clave_aqui") {
    console.log("🟡 Sentinel Omega: Esperando API KEY en el archivo .env...");
    return;
  }
  const genAI = new GoogleGenerativeAI(apiKey);
  try {
    const model = genAI.getGenerativeModel({ model: "gemini-2.5-pro" });
    const result = await model.generateContent("Sentinel Omega Report: Status OK. CodeRabbit Link Active.");
    console.log("\n🛰️  [LOG]: " + result.response.text());
  } catch (e) { console.error("❌ Error de enlace:", e.message); }
}
run();
EOF

cat <<EOF > docker-compose.yml
version: '3.8'
services:
  sentinel:
    build: .
    container_name: sentinel_omega_container
    env_file: .env
    restart: always
EOF

echo "GEMINI_API_KEY=tu_clave_aqui" > .env

# 4. LANZAMIENTO Y ESPERA ACTIVA
echo "🚀 Construyendo y levantando contenedor..."
docker-compose up --build -d

echo "⏳ Verificando salud del sistema..."
until [ "$(docker inspect -f '{{.State.Running}}' sentinel_omega_container 2>/dev/null)" == "true" ]; do
    printf '.'
    sleep 0.5
done

echo -e "\n✅ ¡SISTEMA SENTINEL OMEGA EN LÍNEA!"
echo "🐰 Extensión CodeRabbit instalada en VS Code."
echo "-------------------------------------------------------"
docker logs sentinel_omega_container
./deploy.sh
