## 🛠️ Modelagem de Inteligência Artificial e Algoritmos
O sistema utiliza uma abordagem híbrida de Machine Learning para garantir a confiabilidade dos dados coletados em campo:
* **Detecção de Falhas e Anomalias (Passo 2):** Implementação do algoritmo **Isolation Forest** (`scikit-learn`) focado em identificar anomalias físicas nos sensores (leituras corrompidas, picos impossíveis ou falhas de hardware).
* **Classificação de Qualidade (Passo 3):** Algoritmo **Random Forest Classifier** treinado para segmentar as condições da água a partir dos recursos preditivos analisados.
* **Métricas Analisadas em Tempo Real (Passo 4):** Processamento matemático instantâneo das variáveis de **pH**, **Temperatura** e **Turbidez**.

## 🚀 Pipeline de Decisão Automatizado
A função principal `analisar_leitura(ph, temp, turb)` executa o seguinte fluxo lógico:
1. **Verificação de Integridade:** O modelo de anomalia testa o dado bruto. Se for detectado erro de leitura, emite alerta imediato: `CRITICO: Sensor quebrado ou leitura impossível!`.
2. **Análise de Conformidade:** Caso o dado seja íntegro, o classificador valida os parâmetros de qualidade hídrica.
3. **Despacho de Alerta:** Emite status de `SUCESSO` para água em conformidade ou `ATENCAO` caso os efluentes estejam fora dos padrões ambientais exigidos.
# 🌊 Monitoramento de Efluentes e Previsão de Enchentes com IA e IoT

## 📝 Descrição do Projeto
Este é um projeto de nível industrial que integra Internet das Coisas (IoT), Visão Computacional e Machine Learning para a gestão ambiental inteligente. O sistema realiza o monitoramento remoto de corpos d'água, o controle de nível de rios e efluentes, e utiliza inteligência artificial para prever enchentes, emitindo sinais de alerta automatizados para mitigação de riscos.

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Hardware / IoT:** ESP32 (captura de imagens, sensores de nível e transmissão remota)
* **Visão Computacional:** YOLOv8 (detecção de elementos e análise visual de vazão)
* **Linguagem Principal:** Python 3.x
* **Ambiente de Desenvolvimento:** Jupyter Notebook (`.ipynb`) e Scripts Python (`.py`)

## 🚀 Funcionalidades Chave
* **Controle de Nível Remoto:** Monitoramento contínuo de rios e efluentes integrado ao ESP32.
* **Previsão de Enchentes:** Modelos preditivos de Machine Learning voltados para a antecipação de cheias e transbordamentos.
* **Sistema de Alerta Inteligente:** Emissão automatizada de sinais e notificações para todos os níveis críticos detectados.
* **Visão Computacional:** Algoritmo YOLOv8 aplicado à análise de cenários hídricos em tempo real.

## 📂 Estrutura do Repositório
* `LinhaAgua.ipynb`: Notebook contendo a análise exploratória, o treinamento do modelo e validações.
* `meu_projeto.py`: Script principal estruturado para rodar o pipeline completo de monitoramento e alertas.
* `projeto iaaa.txt`: Notas de desenvolvimento e especificações técnicas de hardware/software.

## ⚙️ Como Executar o Projeto
1. Clone o repositório:
```bash
git clone https://github.com
```
2. Instale as dependências essenciais:
```bash
pip install ultralytics opencv-python jupyter
```
3. Execute o notebook `LinhaAgua.ipynb` para conferir a modelagem ou o script `meu_projeto.py` para iniciar o sistema produtivo de alertas.
