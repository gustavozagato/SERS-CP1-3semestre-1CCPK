# Atividades de Energias Renováveis e Sustentáveis

Este repositório contém a resolução de dois notebooks de análise de dados voltados para o setor de eficiência energética e sustentabilidade. Abaixo está a descrição detalhada do que foi desenvolvido em cada um dos arquivos.

EQUIPE:
Gustavo Zagato Bottechia - RM: 569420  
Davi Q. Zuolo - RM: 571669  
Daniel Vilela Mana - RM: 571632  
Kayo Henderson - RM: 570706  

---

## 1. SERS_Aula02_Exercícios.ipynb

### Sobre a Atividade
Esta atividade é focada na manipulação e análise exploratória de dados utilizando a biblioteca `pandas`. O objetivo principal foi realizar o processamento de diferentes bases de dados do setor energético para extrair *insights* relevantes. As tarefas executadas incluem:
- Carregamento e inspeção inicial dos dados (uso de funções como `head`, `info`, `describe`).
- Renomeação de colunas para facilitar a interpretação.
- Identificação de valores máximos, cálculo de limiares (ex: 70% ou 75% do consumo máximo) e filtragem de DataFrames.
- Cruzamento de critérios ambientais e elétricos (ex: consumo vs. temperatura, consumo vs. fator de potência) para entender a origem das anomalias e picos de demanda.
- Interpretação técnica dos resultados a fim de apoiar a tomada de decisões no gerenciamento energético.

### Datasets Utilizados
Foram utilizados 6 datasets provenientes de repositórios públicos (UCI Machine Learning Repository e Kaggle):
1. **Appliances Energy Prediction (UCI):** Dados do comportamento e consumo energético de eletrodomésticos em uma residência.
2. **Steel Industry Energy Consumption (UCI):** Dados industriais focados na relação entre carga de consumo e fator de potência na siderurgia.
3. **Power Consumption of Tetouan City (UCI):** Dados do consumo distribuído por zonas atrelados a condições climáticas (temperatura, umidade, velocidade do vento).
4. **Solar Power Generation Data (Kaggle):** Registros de geração de potência CC/CA e rendimento de múltiplos inversores em uma usina fotovoltaica.
5. **Wind & Solar Energy Production (Kaggle):** Dados comparativos de produção energética por fontes renováveis (Solar e Eólica).
6. **Individual Household Electric Power Consumption (UCI):** Monitoramento elétrico detalhado de uma residência (potência ativa, reativa e intensidade de corrente).

---

## 2. CP01_SERS_1CCPK.ipynb

### Sobre a Atividade
Trata-se de um desafio final ("Checkpoint") de Análise de Dados de Energia utilizando integrações com a web. O foco foi consumir dados reais, processá-los e analisá-los estatisticamente. As etapas contemplaram:
- Consulta via requisição HTTP (`requests`) a uma API REST pública para obtenção da carga elétrica de uma região.
- Processamento do formato JSON retornado e conversão para um DataFrame Pandas.
- Higienização e organização estrutural (tratamento de colunas, identificação de ausências e formato dos dados).
- Cálculo de indicadores macro-estatísticos da carga elétrica (Mínimo, Máximo, Média, Mediana e Amplitude).
- Definição de recortes de análise, como "Períodos de Alta Demanda" (acima de 90% da carga máxima) e períodos de "Carga Acima da Média", para avaliar quando o sistema sofre maior sobrecarga.
- Orientação para a criação de visualizações de dados para relatórios técnicos (etapa final descrita na documentação do notebook).

### Datasets Utilizados
- **API Pública de Carga Verificada do ONS (Operador Nacional do Sistema Elétrico):** Dados oficiais do governo brasileiro extraídos da região de São Paulo (SP), contendo os registros de demanda de carga global e supervisionada atualizados por faixas de horário.
