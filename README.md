# 🌊 Sistema Inteligente de Monitoramento Hídrico e Previsão de Enchentes 
![Python](https://shields.io) 
![Scikit-Learn](https://shields.io) 
![YOLOv8](https://shields.io) 
![IoT ESP32](https://shields.io) 

## 📝 Visão Geral do Projeto
Esta é uma solução integrada de **Inteligência Artificial (IA)** e **Internet das Coisas (IoT)** desenvolvida para a gestão ambiental inteligente e mitigação de desastres naturais.
O sistema realiza a supervisão autônoma e remota de corpos d'água e efluentes através de estações de campo autônomas (ESP32) com telemetria via sinal celular (GPRS/4G), aplicando modelos preditivos e de visão computacional na nuvem ou em servidores locais. > 

 > 💡 **Impacto Real:** O projeto resolve a dependência de redes Wi-Fi domésticas em campo e automatiza a triagem de qualidade, reduzindo custos operacionais e acelerando o tempo de resposta contra enchentes.
--- 

## 🛠️ Status do Ecossistema e Funcionalidades ### 🔹

### 🔹 Módulo 1: Análise de Qualidade e Integridade (Concluído)
Gerenciado pelo script principal `meu_projeto.py`, o pipeline processa fluxos contínuos de dados físico-químicos (pH, Temperatura e Turbidez):
* **Filtro de Integridade:** Algoritmo **Isolation Forest** focado em detectar anomalias nos dados.
* **Classificação de Risco:** Modelo **Random Forest Classifier** avaliando se os parâmetros estão em conformidade.
* **Despacho Logístico:** Sistema interno automatizado que gera status em tempo real (`SUCESSO`, `ATENÇÃO` ou `CRÍTICO`).

### 🔹 Módulo 2: Visão Computacional Avançada (Concluído)
Desenvolvido no ambiente `Untitled0.ipynb`, adiciona inteligência visual por meio de imagens aéreas (Drones ou câmeras fixas):
* **Arquitetura:** Modelo **YOLOv8** (`yolov8n.pt`) otimizado para cenários em tempo real.
* **Alvos de Detecção:** Identificação e segmentação de poluentes superficiais críticos: **`Lixo_Plastico`** e **`Mancha_Oleo`**.

### 🚀 Módulo 3: Controle e Previsão de Enchentes (Em Desenvolvimento 🛠️)
A terceira camada preditiva está sendo estruturada no arquivo `LinhaAgua.ipynb`:
* **Objetivo:** Implementar modelos matemáticos de séries temporais para antecipar cheias com base no histórico de nível dos rios.

## 📂 Organização do Repositório
* 📂 `meu_projeto.py` — Pipeline de produção e lógica dos modelos scikit-learn.
* 📂 `Untitled0.ipynb` — Treinamento, validação e inferência visual da rede YOLOv8.
* 📂 `LinhaAgua.ipynb` — Ambiente de pesquisa ativa para o módulo de previsão de enchentes.
* 📂 `requirements.txt` — Arquivo de dependências para replicação do ambiente de IA.

---

## ⚙️ Como Executar o Projeto

1. **Clonar o Repositório:**
```bash
git clone https://github.com
```

2. **Instalar Dependências:**
```bash
pip install -r requirements.txt
```

3. **Rodar o Pipeline de Sensores:**
```bash
python meu_projeto.py
```
