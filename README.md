# Polarização na Câmara dos Deputados
This repository contains all scripts used throughout my undergraduate dissertation. 


## 1. **Descrição do Projeto**

Esta série de scripts tem o objetivo de reliazar uma análise exploratória dos dados sobre votações nominais da Câmara dos Deputados para os anos de 2003-2021. 


## 2. **Organização dos Materias nas Pastas**

2.1. Pasta Principal: Projeto Polarização \
2.2. Pastas Secundárias: \
      * CODES: Todos os Scripts Desenvolvidos para o Projeto \
      * OUTPUT: Output dos scripts 1 e 2 (servem como imput para os scripts 3,4 e 5) \
      * HTML: Output em .html dos scripts 3,4 e 5 \ 



## 3. **Etapas / Scripts**

 **1_polarizacao.R** -------------------------------------------------

  Importa os dados do url da Câmara dos Deputados 
  * Corrige strings para um padrão único
  * Salva o df final como .csv
  * Input: Dados Portal da Transparência Câmara dos Deputados
  * Output: "1_dados_camara.csv"


**2_clean_data.R**  --------------------------------------------------
  * Organiza os dados "1_dados_camara.csv" 
  * Retira votações com menos de 257 votos
  * Salva o df final como .csv
  * Input: "1_dados_camara.csv"
  * Output: "2c_dados_camara_cleaned.csv"


**3_analise_partido.Rmd** ----------------------------------------

  * Produz gráficos e tabelas sobre a participação dos partidos na Câmara dos Deputados (por ano/legislatura/classificação ideológica)
  * Input: "2c_dados_camara_cleaned.csv"
  * Output: html file

 
 **4_analise_instruementos.Rmd** ----------------------------------

  * Produz gráficos e tabelas sobre os instrumentos mais votados na Câmara dos Deputados (por ano/legislatura/partido)
  * Input: "2c_dados_camara_cleaned.csv"
  * Output: html file


**5_analise_votos.Rmd** ------------------------------------------ 

  * Produz gráficos e tabelas sobre a correlação do percentual de votos sim entre todos os partidos da Câmara dos Deputados
  * Input: "2c_dados_camara_cleaned.csv"
  * Output: html file


## 4. Próximos Passos

**3_analise_partido.Rmd** ----------------------------------------
  * Gráfico 7: Assentos na Câmara dos Deputados para o Ano de 2003
  * Arrumar legenda/ordem dos partidos por ideologia


**5_analise_votos.Rmd** ----------------------------------------

**O que foi feito:** 
     * Padronizar nome dos partidos (ex: SD e SDD -> SOLIDARIEDADE)
     * Ordenar partidos por ideologia antes de plotar correlação
     * Descobri que existe um erro filtrar as votações por legislatura. (Erro:número de partidos que votam em cada proposição não é o mesmo depois de filtrar)\
     \
**O que ainda precisa ser feito:** 
* Para cada par de partidos, checar o número de votações em comum entre eles
* Descobrir o pq de valores NA nos graficos de correlação 


