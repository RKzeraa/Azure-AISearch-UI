# Azure-AISearch-UI-

### Explore um Índice do Azure AI Search (UI)

#### Criar Recursos do Azure

1. Acesse o [portal do Azure](https://portal.azure.com).
2. Clique em **+ Criar um recurso**, pesquise por **Azure AI Search** e crie um recurso Azure AI Search com as seguintes configurações:
   - **Assinatura**: Sua assinatura do Azure.
   - **Grupo de recursos**: Selecione ou crie um com um nome exclusivo.
   - **Nome do serviço**: Um nome exclusivo.
   - **Localização**: Escolha qualquer região disponível.
   - **Nível de preços**: Básico.
   - Clique em **Review + create** e, depois de ver a resposta "Validation Success", clique em **Create**.
3. Após a conclusão da implantação, selecione **Ir para o recurso**.

#### Criar um Recurso de Serviços de IA do Azure

1. No portal do Azure, clique em **+ Criar um recurso**, pesquise por **serviços de IA do Azure** e crie um plano de serviços de IA do Azure com as seguintes configurações:
   - **Assinatura**: Sua assinatura do Azure.
   - **Grupo de recursos**: O mesmo do recurso Azure AI Search.
   - **Região**: A mesma do recurso Azure AI Search.
   - **Nome**: Um nome exclusivo.
   - **Nível de preços**: Padrão S0.
2. Após a validação, clique em **Create**.

#### Criar uma Conta de Armazenamento

1. No portal do Azure, clique em **+ Criar um recurso**.
2. Procure por **conta de armazenamento** e crie uma com as seguintes configurações:
   - **Assinatura**: Sua assinatura do Azure.
   - **Grupo de recursos**: O mesmo do Azure AI Search e dos serviços de IA do Azure.
   - **Nome da conta de armazenamento**: Um nome exclusivo.
   - **Localização**: Escolha qualquer local disponível.
   - **Padrão de desempenho**: Padrão.
   - **Redundância**: Armazenamento localmente redundante (LRS).
   - Clique em **Review + create** e, depois de validar, clique em **Create**.
3. Na conta de Armazenamento do Azure, altere a configuração de **Permitir acesso anônimo de Blob** para **Habilitado** e clique em **Salvar**.

#### Carregar Documentos para o Armazenamento do Azure

1. Na conta de armazenamento, no painel de menu esquerdo, selecione **Containers**.
2. Selecione **+ Contêiner** e configure com as seguintes configurações:
   - **Nome**: Coffee-Reviews
   - **Nível de acesso público**: Container
   - Clique em **Criar**.
3. Baixe as avaliações de café compactadas em [este link](https://aka.ms/mslearn-coffee-reviewse) e extraia os arquivos.
4. Selecione o contêiner de avaliações de café, selecione **Carregar** e carregue os arquivos extraídos.

#### Indexar os Documentos

1. No portal do Azure, vá para o recurso Azure AI Search e selecione **Importar dados**.
2. Na página de conexão aos seus dados, selecione **Azure Blob Storage** como Fonte de Dados e preencha os detalhes.
3. Adicione habilidades cognitivas e enriquecimentos conforme necessário.
4. Personalize o índice de destino e crie um indexador.
5. Volte à página do recurso e atualize os indexadores até o status indicar sucesso.

#### Consultar o Índice

1. Utilize o Search Explorer para escrever e testar consultas.
2. Selecione o índice de café criado e altere a visualização para JSON view.
3. Escreva consultas e revise os resultados em JSON.

#### Revisar o Armazenamento de Conhecimento

1. Navegue até a conta de armazenamento do Azure e selecione Containers.
2. Selecione o contêiner de armazenamento de conhecimento e revise os arquivos e projeções disponíveis.
3. Explore as tabelas para visualizar as entidades e os dados enriquecidos extraídos das habilidades de IA.
