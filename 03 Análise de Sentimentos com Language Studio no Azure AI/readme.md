<h1>
    <a href="https://github.com/AureliobotIA/Microsoft-Fundamentos-de-IA-DIO/blob/main/01%20Trabalhando%20com%20Machine%20Learning%20na%20Pr%C3%A1tica%20no%20Azure%20ML/download.jpg/">
     <img align="center" width="100px" src="https://github.com/AureliobotIA/Microsoft-Fundamentos-de-IA-DIO/blob/main/01%20Trabalhando%20com%20Machine%20Learning%20na%20Pr%C3%A1tica%20no%20Azure%20ML/download.jpg"></a>
    <span> Análise de Sentimentos com Language Studio no Azure AI</span>
</h1>


![Captura de tela 2024-03-15 101045](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/03%20An%C3%A1lise%20de%20Sentimentos%20com%20Language%20Studio%20no%20Azure%20AI/inputs/conversacao%20tempo%20real.JPG)
Passo a passo de experimento usando:
  - Análise de Sentimentos com Language Studio no Azure AI.
    
## Estúdio de Fala
- Em outra guia do navegador, abra o [Portal Estúdio de Fala](https://speech.microsoft.com/portal) entrando com a conta da Microsoft do Azure.
  
### Comentário: O sistema pega um arquivo de áudio e vai transcrever em texto ou um texto e vai transformar em áudio.

## Configuração:
#### Selecione Configurações e depois Crie um recurso. Configure-o com as seguintes configurações:
- Nome do novo recurso : Insira um nome exclusivo.
- Assinatura : sua assinatura do Azure.
- Região : Selecione uma região suportada: Leste dos EUA.
- Nível de preços : selecione Padrão S0.
- Grupo de recursos : selecione ou crie um grupo de recursos com um nome exclusivo.
- Selecione Criar recurso.
- Aguarde até que o recurso seja criado.
- selecione Usar recurso.
- Aperte em X para navegar para a página Introdução à Fala.

## Conversão de fala em texto: 
### Passo 1
- Acessar a parte da tela onde tem conversão de fala em texto.
- Apertar Conversão de fala em texto em tempo real.

### Passo 2

![Captura de tela 2024-03-15 101045](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/03%20An%C3%A1lise%20de%20Sentimentos%20com%20Language%20Studio%20no%20Azure%20AI/inputs/audio%20em%20texto.JPG
)

## Análise de Sentimentos:
### Passo 1
- Em outra guia do navegador, abra o portal do Azure em [Portal Azure](https://portal.azure.com), entrando com a conta da Microsoft associada à sua assinatura do Azure.

### Passo 2
- Clique no botão ＋ Create a resource.
- Procure por Language service.
- Selecione criar Language service.
- Você será levado a uma página para Select additional features.
- Mantenha a seleção padrão e clique em Continue to create your resource.

### Passo 3
#### Na página Create Language, configure-o com as seguintes configurações:
- Subscription: sua assinatura do Azure.
- Resource group: selecione ou crie um grupo de recursos com um nome exclusivo.
- Region: East US.
- Name: Insira um nome exclusivo..
- Pricing tier: Free F0.
- Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo: Selecionado.
- Selecione Review + create e depois Create e aguarde a conclusão da implantação.

### Passo 4
- Em outra guia do navegador, abra o [Portal Language Studio](https://language.cognitive.azure.com) e entre com a conta da Microsoft do Azure.
![Captura de tela 2024-03-15 101045](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/03%20An%C3%A1lise%20de%20Sentimentos%20com%20Language%20Studio%20no%20Azure%20AI/inputs/language%20azure.JPG)
### Passo 5
#### Quando solicitado com Select an Azure resource, faça as seguintes configurações:
- Azure directory: Diretório Padrão, o diretório que você está usando. Ex: Canal da Cloud.
- Azure subscription: Selecione a assinatura que você está usando.
- Resource type: Language
- Resource name: Selecione o recurso de serviço de idioma que você acabou de criar.
- Em seguida, selecione: Done.

### Passo 6
- Na página inicial Language Studio. Selecione a guia Classify text.
- Em seguida, selecione o bloco Analyze sentiment and mine opinions.
- Em Selecionar idioma do texto, pode ser Inglês ou Português de sua preferência.
- Escreva a Sentença ou Selecione o seu recurso Azure.
- Marque o CheckBox e Aperte em Run.

## Resultado:
### Sentimento do Documento:

![Captura de tela 2024-03-15 113314](https://github.com/DalilaDeveloperMobile/dio-practice-microsoft-azure-ai-fundamentals/assets/29806802/2bb65bf4-cd85-4117-97f7-75fc1bd6fe57)

### Sentence 1
![S1](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/03%20An%C3%A1lise%20de%20Sentimentos%20com%20Language%20Studio%20no%20Azure%20AI/inputs/sentenca%2001.JPG
)

### Sentence 2

![S2](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/03%20An%C3%A1lise%20de%20Sentimentos%20com%20Language%20Studio%20no%20Azure%20AI/inputs/sentenca%2002.JPG
)

### Sentence 3

![S3](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/03%20An%C3%A1lise%20de%20Sentimentos%20com%20Language%20Studio%20no%20Azure%20AI/inputs/sentenca%2003.JPG
)

### Sentence 4

![S4](https://github.com/AureliobotIA/Microsoft-Fundamentos-de-AI-DIO/blob/main/03%20An%C3%A1lise%20de%20Sentimentos%20com%20Language%20Studio%20no%20Azure%20AI/inputs/sentenca%2004.JPG
)

