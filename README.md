# flexsdm-exemplo

Esse repositório é um exemplo comentado de uso do pacote `flexsdm` para a construção de Modelos de Adequação de Habitat (HSM), incluindo todas as instruções necessárias para você organizar os seus dados no formato correto que será usado para construir os modelos. 

Aqui estão as principais etapas:

### 1. Organizar os dados geográficos
Primeiramente, é preciso que você identifique a área geográfica de estudo. Forneça uma pasta com o arquivo .shp (shapefile) que delimita a sua área, dentro da pasta `data/geo` (você pode seguir o exemplo do shapefile que já foi carregado, ou poderia construir o próprio polígono usando o pacote `sf` e salvar o polígono - um exemplo se encontra no código `Area_Geografica.Rmd`). Será necessário modificar nos outros códigos o caminho do arquivo shapefile desejado.

### 2. Organizar os dados de ocorrência
Traga todos os arquivos com ocorrências da espécie, preferencialmente para a pasta `data/ocorrencias`. Eles serão integrados em um único arquivo .csv no código `Ocorrencias_Tratamento.Rmd`, mas é preciso que você modifique este código de acordo com sua estrutura, carregando cada formato de arquivo que você deseja e filtrando de acordo com sua necessidade.

### 3. Organizar os dados ambientais
Da mesma forma, é preciso que você forneça os dados ambientais que serão usados. Idealmente, você deve fornecer o arquivo .tif com todas as variáveis ambientais que serão usadas em um período. No exemplo feito, existe um arquivo .tif para cada combinação de cenário do CMIP6 e período de tempo, no caso, em décadas, além do cenário "baseline" que representa o cenário atual ao qual os modelos serão ajustados. Com os arquivos .tif nomeados corretamente o código de Modelos já irá funcionar, mas existe o código `Ambientais_Tratamento.Rmd` para auxiliar você a organizar os dados ambientais caso necessário.

### 4. Ajustar os Modelos de Adequação de Habitat
Com todos os dados organizados, você pode seguir as etapas do código `Modelos_HSM.Rmd` para construir os Modelos de Adequação de Habitat, definindo os seus parâmetros desejados.

Autor: Gabriel Schaldach Morgado