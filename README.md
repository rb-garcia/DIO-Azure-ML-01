# DIO-Azure-ML-01
Trabalhando com Machine Learning na Prática no Azure ML

Machine Learning Studio, opção Automated ML
- Crie um novo trabalho com as seguintes configurações avançando pela interface do usuário

# Configurações básicas
- Nome do trabalho: mslearn-bike-autom 
- Nome do experimento: mslearn-bike-rental
- Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
- Marcadores: nenhum 
- Selecione o tipo de tarefa: Regressão
- Selecionar conjunto de dados:
- Crie um novo conjunto de dados com as seguintes configurações:
- Nome: alugueldebicicletas
- Descrição: Dados históricos de aluguel de bicicletas
- Tipo: Tabular
- Fonte de dados: Selecione dos arquivos da web URL da Web: URL da Web: https://aka.ms/bike-rentals
- Ignorar validação de dados: não selecionar
- Formato de arquivo: Delimitado
- Delimitador: Vírgula
- Codificação: UTF-8
- Cabeçalhos de coluna: apenas o primeiro arquivo possui cabeçalhos
- Pular linhas: Nenhum
- O conjunto de dados contém dados multilinhas: não selecione
- Esquema: Incluir todas as colunas exceto Caminho Revise os tipos detectados automaticamente Selecione Criar.
- Após a criação do conjunto de dados, selecione o conjunto de dados "alugueldebicicletas" para continuar a enviar o trabalho de ML automatizado.

# Configurações de tarefa
- Tipo de tarefa: Regressão
- Conjunto de dados: alugueldebicicletas
- Coluna de destino : Aluguéis (inteiro)
- Configurações adicionais :
- Métrica primária: raiz do erro quadrático médio normalizado
- Explique o melhor modelo : Não selecionado
- Usar todos os modelos suportados : Desmarcado
- Você restringirá o trabalho para tentar apenas alguns algoritmos específicos.
- Modelos permitidos: Selecione apenas RandomForest e LightGBM 
- Limites: expanda esta seção
- Máximo de testes: 3
- Máximo de testes simultâneos: 3
- Máximo de nós: 3
- Limite de pontuação da métrica : 0,085
- Tempo limite : 15
- Tempo limite de iteração : 15
- Habilitar rescisão antecipada: selecionado
- Validação e teste: Tipo de validação : divisão de validação de trem Porcentagem de dados de validação : 10
- Conjunto de dados de teste: Nenhum Calcular
- Selecione o tipo de computação : sem servidor Tipo de máquina virtual : CPU Camada de máquina virtual : Dedicada Tamanho da máquina virtual : Standard_DS3_V2* Número de instâncias : 1
