<h1>
    <a href="https://github.com/AureliobotIA/Microsoft-Fundamentos-de-IA-DIO/blob/main/01%20Trabalhando%20com%20Machine%20Learning%20na%20Pr%C3%A1tica%20no%20Azure%20ML/download.jpg/">
     <img align="center" width="100px" src="https://github.com/AureliobotIA/Microsoft-Fundamentos-de-IA-DIO/blob/main/01%20Trabalhando%20com%20Machine%20Learning%20na%20Pr%C3%A1tica%20no%20Azure%20ML/download.jpg"></a>
    <span> Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados</span>
</h1>

## Previsão

# ai-search-microsoft-azure
Passo a passo de experimento usando:
  - Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados.

 #### Realizado como desafio de projeto no Bootcamp Microsoft Azure AI Fundamentals da [Dio.me](https://www.dio.me/).

 > [!NOTE]
> Essas informações são exclusivamente uma maneira de fazer essas atividades.
>  Mais o preferencial sempre será a Documentação Oficial: [AI Search](https://aka.ms/ai900-ai-search).

### Passo 1
- Entre no [Portal do Azure](https://portal.azure.com/?azure-portal=true).

#### Clique no botão + Create a resource, pesquise por Azure AI Search, e crie um recurso do Azure AI Search com as seguintes configurações:
- Subscription: Sua assinatura do Azure.
- Resource group: Selecione ou crie um grupo de recursos com um nome exclusivo.
- Service name: Um nome exclusivo.
- Location: Escolha qualquer região disponível. East US.
- Pricing tier: Básico. Selecione Basic.
- Selecione Review + create, e depois de ver a resposta Validation Success, selecione Create.
- Após a conclusão da implantação, selecione Go to resource. Na página de visão geral do Azure AI Search, você pode adicionar índices, importar dados e pesquisar índices criados.

### Passo 2
- Retorne à página inicial do portal do Azure. Clique no botão ＋Create a resource e pesquise por Azure AI services. Selecione criar um plano de Azure AI services. Você será levado a uma página para criar um recurso de Azure AI services. Configure-o com as seguintes configurações:
- Subscription: Sua assinatura do Azure.
- Resource group: O mesmo grupo de recursos que o seu recurso Azure AI Search.
- Region: O mesmo local que o seu recurso Azure AI Search. East US.
- Name: Um nome exclusivo.
- Pricing tier: Standard S0.
- Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo: Selecionado.
- Selecione Review + create. Depois de ver a resposta Validação aprovada, selecione Create.
- Aguarde a conclusão da implantação e visualize os detalhes da implantação.

### Passo 3
- Retorne à página inicial do portal do Azure e selecione o botão + Create a resource.
- Procure por storage account, e crie um recurso de Storage account com as seguintes configurações:
- Subscription: Sua assinatura do Azure.
- Resource group: O mesmo grupo de recursos que os recursos do Azure AI Search e dos serviços Azure AI.
- Storage account name: Um nome exclusivo.
- Location: Escolha qualquer local disponível. (US) East US.
- Performance: Standard
- Redundancy: Locally redundant storage (LRS).
- Clique em Revisar e em Criar. Aguarde a conclusão da implantação e vá para o recurso implantado.
- Na Azure Storage account que você criou, no painel de menu esquerdo, selecione Configuration (em Settings).
- Altere a configuração de Allow Blob anonymous access para Enabled e selecione Save.

### Passo 4
- No painel de menu esquerdo, selecione Containers.

![Captura de tela](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/04%20Azure%20Cognitive%20Search%3A%20Utilizando%20AI%20Search%20para%20indexa%C3%A7%C3%A3o%20e%20consulta%20de%20Dados/input/04.png)

- Selecione + Container. Um painel do seu lado direito é aberto.
- Insira as seguintes configurações e clique em Create:
- Name: coffeereviews. Avaliações de café.
- Public access level: Container (anonymous read access for containers and blobs)
- Advanced: sem alterações.
- Aperte em Create.

### Passo 5
- Em uma nova guia do navegador, baixe as avaliações compactadas do café em https://aka.ms/mslearn-coffee-reviews, e extraia os arquivos para a pasta de coffee-reviews.
- No portal do Azure, selecione o coffee-reviews container. No container, selecione Upload.

![Captura de tela ](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/04%20Azure%20Cognitive%20Search%3A%20Utilizando%20AI%20Search%20para%20indexa%C3%A7%C3%A3o%20e%20consulta%20de%20Dados/input/05.png)

- No painel Upload blob, selecione Selecionar um arquivo.
- Na janela do Explorer, selecione todos os arquivos na pasta de avaliações, selecione Abrir e, em seguida, selecione Upload.

![Captura de tela ](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/04%20Azure%20Cognitive%20Search%3A%20Utilizando%20AI%20Search%20para%20indexa%C3%A7%C3%A3o%20e%20consulta%20de%20Dados/input/05%202.png)

- Depois que o upload for concluído, você poderá fechar o painel Upload blob. Seus documentos estão agora em seu coffee-reviews storage container.

### Passo 6
- No portal do Azure, navegue até o recurso Azure AI Search. Na página Visão geral, selecione Import data.

![Captura de tela 2024-03-18 103306](h%3A%20Utilizando%20AI%20Search%20para%20indexa%C3%A7%C3%A3o%20e%20consulta%20de%20Dados/input/06.png)

- Na página Connect to your data, na lista Data Source, selecione Azure Blob Storage. Preencha os detalhes do armazenamento de dados com os seguintes valores:
- Data Source: Azure Blob Storage.
- Data source name: coffee-customer-data.
- Data to extract: Content and metadata
- Parsing mode: Default
- Connection string: *Selecione Escolha uma conexão existente. Selecione sua conta de armazenamento, selecione o contêiner de avaliações de café e clique em Selecionar.
- Managed identity authentication: None
- Container name: esta configuração é preenchida automaticamente depois que você escolhe uma conexão existente.
- Blob folder: Deixe isso em branco.
- Description: Reviews for Fourth Coffee shops.
- Selecione Next: Add cognitive skills (Optional).

### Passo 7
- Na Página "Add Cognitive skills (optional)", em "Attach AI Services", selecione seu recurso.
- Em "add enrichments" preencher conforme o texto seguido.
- Escreva o nome da Skillset para coffee-skillset.
- Marque a caixa de seleção: Enable OCR and merge all text into merged_content field.
- Certifique-se de que o Source data field esteja definido como merged_content.
- Altere o Enrichment granularity level para Pages (5000 character chunks).
- Não selecione: Enable incremental enrichment.
- Selecione os seguintes campos enriquecidos:
- Extract location names: locations.
- Extract key phrases: keyphrases.
- Detect sentiment: sentiment.
- Generate tags from images: imageTags.
- Generate captions from images: imageCaption.
- Em Save enrichments to a knowledge store, selecione: "Image projections".
- Selecione "choose an existing connection".
- Escolha o storage criado anteriormente.
- Clique em + Container para criar um novo contêiner chamado knowledge-store com o nível de privacidade definido como Private, e selecione Create.
- Selecione então o knowledge-store e clique em "select".

### Passo 8
- Selecione Azure blob projections: Document. Uma configuração para o nome do contêiner com as exibições preenchidas automaticamente do contêiner de armazenamento de conhecimento. Não altere o nome do contêiner.
- Selecione Next: Customize target index. Altere o nome do índice para coffee-index.
- Certifique-se de que a chave esteja definida como metadata_storage_path. Deixe o nome do Suggester name em branco e o Search mode preenchido automaticamente.
- Revise as configurações padrão dos campos de índice. Selecione filterable para todos os campos que estão selecionados por padrão.
- Selecione Next: Create an indexer.

### Passo 9
- Altere o nome do Indexer name para coffee-indexer.
- Deixe o Schedule definida como Once.
- Certifique-se de que a opção Base-64 Encode Keys esteja selecionada.
- Aperte em "submit".

### Passo 10
- Abrir o Azure AI Services| Ai Search, e Aperte em Search Explorer

![Captura de tela ](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/04%20Azure%20Cognitive%20Search%3A%20Utilizando%20AI%20Search%20para%20indexa%C3%A7%C3%A3o%20e%20consulta%20de%20Dados/input/10.png)

- No Search Explorer, Filtrar por conta search=*&$count=true, e aperte em "search".

- Filtrar por sentimentos negativos de pessoas search=sentiment:'negative'.

- Filtrar por localização sentimentos search=locations:'Chicago'.

<hr>

