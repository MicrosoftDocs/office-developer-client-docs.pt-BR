---
title: Criar um fluxo de trabalho do Project Server para gerenciamento de demanda
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: Este artigo descreve como criar um fluxo de trabalho simple usando o SharePoint Designer 2013.
ms.openlocfilehash: d548cbc47585add2648396f4736e6ad36a00bcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771062"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Criar um fluxo de trabalho do Project Server para gerenciamento de demanda

Este artigo descreve como criar um fluxo de trabalho simple usando o SharePoint Designer 2013. Você pode exportar o fluxo de trabalho para o Visio 2013 para visualização e edição, ou use o Visio 2013 para fluxos de trabalho do Project Server 2013 de design e importar o design para o SharePoint Designer 2013 para publicação ao Project Web App. Para obter mais informações sobre a plataforma de fluxo de trabalho do SharePoint e criando fluxos de trabalho com o SharePoint Designer 2013 e o Visio 2013, consulte os artigos de [fluxos de trabalho no SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx) na documentação do desenvolvedor do SharePoint 2013. 
  
Para obter informações sobre como preparar o Project Server para fluxos de trabalho, consulte [Iniciar: definida para cima e para configurar o Gerenciador de fluxo de trabalho do SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163276%28office.15%29.aspx).

<a name="pj15_CreateWorkflowSPD_General"> </a>

## <a name="creating-a-general-workflow"></a>Criando um fluxo de trabalho geral

Use as etapas a seguir para criar um fluxo de trabalho do Project Server 2013 usando o SharePoint Designer 2013. O fluxo de trabalho foi projetado para gerenciamento de propostas de propostas de projeto.
  
Para obter etapas detalhadas, consulte a seção [Criando um fluxo de trabalho ramificação](#pj15_CreateWorkflowSPD_Detailed) . 
  
### <a name="to-create-a-project-server-workflow-general-procedure"></a>Para criar um fluxo de trabalho do Project Server (procedimento geral)

1. Determine os requisitos e então projete o fluxo de trabalho. Organize-o em fases e estágios e determine os campos personalizados que o fluxo de trabalho usará.
    
2. No Project Web App, crie as entidades que requer que o fluxo de trabalho:
    
    1. Examine as fases existentes do fluxo de trabalho; crie fases como o necessário.
        
    2. Crie os campos personalizados da empresa que o fluxo de trabalho usará. Para estar disponível em um estágio do fluxo de trabalho, um campo personalizado deverá ser controlado por um fluxo de trabalho.
        
    3. Edite ou crie as páginas de detalhes do projeto (PDPs) que os estágios do seu fluxo de trabalho usarão para coletar informações para o projeto. Neste exemplo, os estágios usarão PDPs padrão editados para incluírem um novo campo personalizado.
        
    4. Crie os estágios necessários do fluxo de trabalho e então associe cada estágio de fluxo de trabalho à fase correta.
    
3. No SharePoint Designer 2013, construa o fluxo de trabalho usando afirmações de declaração no **Designer baseado em texto**:
    
    > [!NOTE]
    > Você também pode alternar para o **Visual Designer** no SharePoint Designer 2013 ou importar um fluxo de trabalho existente do Visio 2013. Siga estas etapas para usar o **Designer baseado em texto**: 
    > 
    > 1. Abra o site do Project Web App e, em seguida, crie um fluxo de trabalho de site que usa a plataforma de fluxo de trabalho do **SharePoint 2013 Workflow - Project Server** . 
    > 2. Adicione os estágios usados pelo fluxo de trabalho.
    > 3. Insira as etapas, as condições, as ações e os loops do fluxo de trabalho necessários em cada estágio.
    > 4. Verifique se há algum erro no fluxo de trabalho e corrija os que encontrar.
    > 5. (Opcional) Alternar o modo de exibição para o **Visual Designer**ou exportar o fluxo de trabalho para um arquivo do Visio 2013. Você pode modificar o modo de exibição do Visio e salvar as alterações no fluxo de trabalho atual. Você pode editar o arquivo do Visio e importá-lo no SharePoint Designer 2013 criar outros fluxos de trabalho.
    > 6. Publica o fluxo de trabalho. Depois que ele for publicado, o fluxo de trabalho mostra na lista de fluxos de trabalho para o site do Project Web App.
    
4. No Project Web App, use o fluxo de trabalho para gerenciamento de propostas de propostas de projeto:
    
    1. Crie um modelo de projeto corporativo (EPT) que use o fluxo de trabalho.
        
    2. Na página Centro de Projeto, crie um projeto que use o EPT para o fluxo de trabalho e então siga os estágios do fluxo de trabalho.
        
    3. Teste o fluxo de trabalho cuidadosamente.
        
    4. Implante o fluxo de trabalho em um servidor de produção.

<a name="pj15_CreateWorkflowSPD_Detailed"> </a>

## <a name="creating-a-branching-workflow"></a>Criando um fluxo de trabalho de ramificação

Antes de poder usar o SharePoint Designer 2013 para criar um fluxo de trabalho do Project Server, o serviço de cliente do Gerenciador de fluxo de trabalho 1.0 deve ser configurado para usar as atividades de fluxo de trabalho do Project Server 2013. Para obter informações sobre como configurar o cliente do Gerenciador de fluxo de trabalho 1.0, consulte os artigos de [fluxos de trabalho no SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx) na documentação do desenvolvedor do SharePoint Server 2013. 
  
O procedimento a seguir detalhado inclui as mesmas etapas da seção [Criando um fluxo de trabalho geral](#pj15_CreateWorkflowSPD_General) . 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>Para criar um fluxo de trabalho de ramificação do Project Server (procedimento detalhado)

#### <a name="1-plan-and-design-the-workflow"></a>1. planejar e projetar o fluxo de trabalho.

Um fluxo de trabalho do Project Server pode se integrar com várias fases e fases em um processo de gerenciamento de demanda. Como os fluxos de trabalho podem ser complexos, você deve entender os requisitos de negócios e planeje cuidadosamente um fluxo de trabalho. Para obter um exemplo simple, crie um fluxo de trabalho ramificação que usa o custo estimado de uma proposta de projeto para determinar se a proposta foi aceita. Se o custo estimado for maior que US $ 25.000, rejeitar a proposta; Caso contrário, aceite a proposta e criar o projeto.
    
Como você pode usar o Visio 2013 e SharePoint Designer 2013 para ajudar a projetar e criar fluxos de trabalho do Project Server 2013, você pode mais facilmente experiências com fluxos de trabalho que é possível com o Project Server 2010. O exemplo de design de fluxo de trabalho neste artigo forem os mesmos que o artigo [criar um fluxo de trabalho ramificação](http://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) no SDK do Project 2010. Você pode criar e criar um fluxo de trabalho de teste em um computador remoto usando uma instância de teste do Project Web App — você não precisará criar fluxos de trabalho diretamente em um computador do Project Server 2013. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Crie as entidades que requer que o fluxo de trabalho.

No Project Web App, examine as fases do fluxo de trabalho disponíveis e estágios e os campos personalizados da empresa que estão disponíveis. Se necessário, crie as entidades que requer o fluxo de trabalho, como as seguintes etapas:
    
1. **Fases do fluxo de trabalho** A instalação padrão do Project Web App inclui criar, selecionar, planejar, gerenciar e fases terminadas. No exemplo ramificação do fluxo de trabalho, você não precisará criar outras fases. 
        
2. **Campos personalizados da empresa** O fluxo de trabalho ramificação requer um campo personalizado de custo do projeto é controlado por fluxo de trabalho. O valor de um campo personalizado controlado por fluxo de trabalho é definido em um PDP que usa o fluxo de trabalho. Por exemplo, escolha o ícone de **configurações** no canto superior direito de uma página do Project Web App, escolha **Configurações do PWA**e escolha **campos personalizados da empresa e tabelas de pesquisa**.
        
   Criar um campo personalizado denominado custo da proposta da entidade de **projeto** e selecione o tipo de **custo**. Para a descrição, digite o custo estimado de uma proposta de projeto. Na seção **comportamento** , escolha **comportamento controlado por fluxo de trabalho**.
        
3. **Páginas de detalhes do projeto** Editar ou criar o PDPs que usarão os estágios do fluxo de trabalho. Por exemplo, execute as seguintes etapas: 
        
    1. Escolha **Páginas de Detalhes do Projeto** na página Configurações do Servidor e então escolha o PDP **ProjectInformation**. 
            
    2. Na guia **PÁGINA** da faixa de opções, no grupo **Editar**, escolha **Editar Página**.
            
    3. Escolha a seta para baixo no canto superior direito da web part **Básica Info** e escolha **Editar web part**. Ou então, na guia **WEB PART** da faixa de opções, no grupo **Propriedades** , escolha a **web part de propriedades** para mostrar a parte de editor. 
            
    4. Na seção **Campos do Projeto Exibidos** da parte do editor (consulte a Figura 1), escolha **Modificar**.
            
    5. Adicione o campo personalizado de **Custo da proposta** , movê-lo acima do campo **proprietário** na lista de **Campos do projeto selecionado** e escolha **Okey** (consulte a Figura 1).
      
    6. Na parte do editor, escolha **OK** e então escolha **Parar a Edição** no grupo **Editar**, na guia **PÁGINA** da faixa de opções. A Figura 2 mostra o campo personalizado **Proposal Cost** adicionado ao PDP Informações do Projeto. 

    **Figura 1. Editando a web part de campos do projeto em um PDP**

    ![Editando os campos do projeto da web part em uma PDP] (media/pj15_CreateWorkflowSPD_EditPDP.gif "Editando os campos do projeto da web part em uma PDP")

    **Figura 2. O PDP editado inclui o campo personalizado Custo da Proposta**

    ![O PDP editada inclui o campo Custo da proposta] (media/pj15_CreateWorkflowSPD_EditedPDP.gif "O PDP editada inclui o campo Custo da proposta")
  
4. **Estágios do fluxo de trabalho** Crie os estágios que são necessários para cada fase do fluxo de trabalho. Na página Configurações do servidor, escolha **Estágios do fluxo de trabalho**e, em seguida, escolha **Novo ESTÁGIO de fluxo de trabalho**. A Figura 3 mostra a parte da página Adicionar estágio de fluxo de trabalho.
    
    **Figura 3. Adicionando um estágio do fluxo de trabalho no Project Web App**

    ![Adicionando um estágio de fluxo de trabalho no Project Web App] (media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Adicionando um estágio de fluxo de trabalho no Project Web App")
  
    O exemplo de fluxo de trabalho ramificação usa os quatro estágios que são mostrados na tabela 1. Na seção **Configurações adicionais para a página de detalhes do projeto visíveis** da página Adicionar estágio de fluxo de trabalho (não é mostrada na Figura 3), os valores são opcionais. eles fornecem mais informações sobre a página Status do fluxo de trabalho. Por exemplo, porque o PDP inicial de detalhes de proposta exigir a entrada do usuário, você pode marque a caixa de seleção **a página de detalhes do projeto precisam de atenção** e, em seguida, adicione uma descrição específica como definido no nome do projeto e custo por este PDP.
    
    A Figura 4 mostra os quatro estágios concluídos na página Estágios do Fluxo de Trabalho.
    
    **Tabela 1. Estágios para o fluxo de trabalho de ramificação**

    |Nome|Descrição|Descrição para envio|Fase|PDPs visíveis|Campos Personalizados|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Detalhes Iniciais da Proposta  <br/> |Defina o nome e o custo do projeto.  <br/> |Envie o projeto como uma proposta.  <br/> |Criar  <br/> |Informações do Projeto  <br/> Detalhes do Projeto  <br/> |Custo da Proposta (obrigatório)  <br/> |
    |Detalhes do Projeto  <br/> |Forneça detalhes sobre o projeto proposto.  <br/> |Envie detalhes para continuar com o projeto.  <br/> |Criar  <br/> |Informações do Projeto  <br/> Detalhes do Projeto  <br/> |Custo da Proposta (somente leitura)  <br/> |
    |Rejeição Automatizada  <br/> |A proposta é rejeitada, com base nas informações fornecidas.  <br/> | <br/> |Criar  <br/> |Informações do Projeto  <br/> |Custo da Proposta (somente leitura)  <br/> |
    |Execução  <br/> |A proposta é aceita e está pronta para o gerenciamento de projetos.  <br/> | <br/> |Gerenciar  <br/> |Informações do Projeto  <br/> Detalhes do Projeto  <br/> |Custo da Proposta (somente leitura)  <br/> |
   
    **Figura 4. Lista dos estágios do fluxo de trabalho no Project Web App**

    ![Lista dos estágios do fluxo de trabalho no Project Web App] (media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Lista dos estágios do fluxo de trabalho no Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. construa o fluxo de trabalho no Designer baseado em texto.

No SharePoint Designer 2013, construa o fluxo de trabalho usando afirmações de declaração no Designer baseado em texto. Você pode começar a digitar na linha de inserção laranja para obter instruções de AutoCompletar sensível ao contexto para as etapas e a lógica de fluxo de trabalho, ou você pode inserir a lógica e etapas usando os controles no grupo **Inserir** na guia **fluxo de trabalho** da faixa de opções. 
    
1. No modo de exibição Backstage do SharePoint Designer 2013, escolha **Abrir Site**. Por exemplo, abrir `http://ServerName/pwa`. No painel de **navegação** , escolha **fluxos de trabalho**. Em seguida, na guia **fluxos de trabalho** da faixa de opções, no grupo **novo** , escolha **Site de fluxo de trabalho**. Nesse exemplo, nome o fluxo de trabalho de ramificação de fluxo de trabalho. Certifique-se de que o **SharePoint 2013 Workflow - Project Server** está selecionado na lista suspensa **Tipo de plataforma** (consulte a Figura 5). 
    
    **Figura 5. Criando um fluxo de trabalho do site do Project Server**

    ![Criando um fluxo de trabalho de site do Project Server] (media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Criando um fluxo de trabalho de site do Project Server")
  
2. Selecione a guia **Fluxo de Trabalho de Ramificação**. Em seguida, na guia **FLUXO DE TRABALHO** da faixa de opções, no grupo **Gerenciar**, na lista suspensa **Exibições**, escolha **Designer Baseado em Texto**. Para mostrar a exibição com a linha de inserção laranja piscando (consulta a Figura 6), clique na exibição.
    
    **Figura 6. Usando a exibição Designer Baseado em Texto para o fluxo de trabalho**

    ![Usando o modo de exibição do Designer baseado em texto] (media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "Usando o modo de exibição do Designer baseado em texto")
  
3. Na exibição **Designer Baseado em Texto**, adicione os estágios usados pelo fluxo de trabalho. Na guia **FLUXO DE TRABALHO** da faixa de opções, no grupo **Inserir**, na lista suspensa **Estágio** em **Criar**, escolha **Detalhes Iniciais da Proposta**.
    
    De maneira semelhante, posicione a linha de inserção laranja abaixo da caixa **Estágio: Detalhes Iniciais da Proposta** e adicione os outros estágios usados pelo fluxo de trabalho: **Detalhes do Projeto**, **Rejeição Automatizada** e **Execução** (consulte a Figura 7). 
    
    **Figura 7. Adicionando um estágio a um fluxo de trabalho no SharePoint Designer**

    ![Adicionando um estágio para um fluxo de trabalho no SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Adicionando um estágio para um fluxo de trabalho no SPD")
  
4. Adicione as etapas e a lógica do fluxo de trabalho em cada estágio: 
    
    1. No estágio **Detalhes Iniciais da Proposta**, posicione a linha de inserção laranja na parte superior do corpo do estágio. No grupo **Inserir** na faixa de opções, escolha **Ação**, role para baixo até **Ações do Project Web App** e então escolha **Aguardar Evento de Projeto**. Escolha **este evento de projeto** e então selecione **Evento: Quando um projeto é enviado** na lista suspensa. 
    
    2. Na seção **Transição para o estágio** do estágio **Detalhes Iniciais da Proposta**, insira **Se qualquer valor for igual ao valor**. Você pode começar a digitar a declaração ou usar o controle **Condição** no grupo **Inserir** na faixa de opções. 
    
    3. Escolha o primeiro controle de **valor** e então escolha **fx** para mostrar a caixa de diálogo **Definir Pesquisa de Fluxo de Trabalho** (consulte a Figura 8). Na lista suspensa **Fonte de dados**, selecione **Dados do Projeto**. Na lista suspensa **Campo da origem**, selecione **Custo da Proposta**.
    
       **Figura 8. Definindo um valor de pesquisa no fluxo de trabalho**

       ![Definir um valor de pesquisa no fluxo de trabalho] (media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Definir um valor de pesquisa no fluxo de trabalho")
  
    4. Conclua o `If` instrução de forma que ele mostra o seguinte: **custo de dados: proposta de projeto se for maior que 25000**
    
       > [!NOTE]
       > Como alternativa, você poderia criar uma variável de fluxo de trabalho, definir uma variável como o valor do campo personalizado e então comprar a variável ao valor. Por exemplo, da lista suspensa **Variáveis Locais** na faixa de opções, crie uma variável chamada **TotalCost** (sem espaços) do tipo **Number**. Na caixa **Definir Pesquisa do Fluxo de Trabalho**, selecione **Variáveis e Parâmetros do Fluxo de Trabalho** como a fonte de dados e então selecione **Variável: TotalCost** como o campo. A instrução **Se** seria então: **Se a Variável: TotalCost for maior do que 25000**
  
    5. Coloque a linha de inserção laranja dentro do `If` de filiais e inserir **Ir para um estágio** usando o controle de **ação** , no grupo **Inserir** na faixa de opções. Escolha o controle de lista suspensa de **um estágio** e selecione o estágio de **Rejeição automatizada** . 
    
       Da mesma forma, no `Else` de filiais, insira a instrução **Ir para detalhes do projeto** . Figura 9 mostra o estágio de **Detalhes da proposta inicial** concluído. 
    
       **Figura 9. Lógica concluída para o estágio Detalhes Iniciais da Proposta**

       ![Lógica de Completed para obter detalhes de proposta inicial] (media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Lógica de Completed para obter detalhes de proposta inicial")
  
    6. No estágio **Rejeição Automatizada**, a menos que você queira pausar o fluxo de trabalho e mostrar alguns dados em um PDP, deixe a primeira seção vazia. A seção **Transição para o estágio** deve conter uma transição; como não há outro estágio após uma rejeição, digite Ir para o Fim do Fluxo de Trabalho para a instrução. 
    
    7. No estágio **Detalhes do Projeto**, adicione Ir para a Execução na seção **Transição para o estágio**. A menos que haja outros dados a serem adicionados, ou se você quiser pausar o fluxo de trabalho, não será necessário aguardar por um evento enviado. 
    
    8. No estágio **Execução**, a menos que queira pausar o fluxo de trabalho, deixe a seção de ação do estágio vazia. Na seção **Transição para o estágio**, adicione **Ir para o Fim do Fluxo de Trabalho**.
    
5. No grupo **Salvar** da faixa de opções, escolha **Verificar Erros** para verificar a existência de erros de fluxo de trabalho (consulte a Figura 10). Corrija qualquer erro e então escolha **Salvar**.
    
    **Figura 10. Verificando o fluxo de trabalho em busca de erros no SharePoint Designer**

    ![Verificando se há erros no fluxo de trabalho] (media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Verificando se há erros no fluxo de trabalho")
  
6. (Opcional) No grupo **Gerenciar** na faixa de opções, no menu suspenso **Exibições**, escolha **Visual Designer**. Na Figura 11, a exibição terá o zoom reduzido para 50%.
    
    Você pode editar itens no fluxo de trabalho usando o Virtual Designer. Por exemplo, selecione a condição **Se qualquer valor for igual ao valor**, escolha o ícone de ferramenta no canto inferior esquerda da condição e então selecione **Valor** para mostrar as condições de comparação na caixa de diálogo **Propriedades**. 
    
    **Figura 11. Usando o Visual Designer para um fluxo de trabalho**

    ![Usando o modo de design do Visio do fluxo de trabalho] (media/pj15_CreateWorkflowSPD_SwitchView.gif "Usando o modo de design do Visio do fluxo de trabalho")
  
    Quando o fluxo de trabalho está no modo de exibição Visual Designer, para salvar o fluxo de trabalho em um arquivo do Visio 2013 (. vsdx) como um backup ou para uso posterior, você pode escolher a **Exportar para o Visio**.
    
7. Publica o fluxo de trabalho. Quando você usa o SharePoint Designer 2013 para publicar o fluxo de trabalho para o site do Project Web App ativo, o fluxo de trabalho está registrado para o site do SharePoint ou no Windows Azure e se torna disponível no Project Web App para o novos EPTs.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. criar um EPT para o fluxo de trabalho e depois testar o fluxo de trabalho.

No Project Web App, crie um EPT para o fluxo de trabalho e depois testar o fluxo de trabalho gerando uma proposta de projeto:
    
1. Na página Configurações do PWA, escolha **Tipos de projeto corporativo**e, em seguida, crie um EPT denominado Test ramificação fluxo de trabalho. Desmarque a caixa de seleção **criar novos projetos como projetos de lista de tarefas do SharePoint** para que o Project Server manter o controle total de projetos que são criados pelo EPT. Selecione **a ramificação fluxo de trabalho** na lista suspensa **Associação de fluxo de trabalho de Site** e, em seguida, selecione as **Informações do projeto** PDP na lista suspensa **Nova página do projeto** a ser a primeira página que mostra o fluxo de trabalho. 
    
    **Figura 12. Adicionando um EPT ao fluxo de trabalho**

    ![Adicionando um EPT para o fluxo de trabalho] (media/pj15_CreateWorkflowSPD_EPTs.gif "Adicionando um EPT para o fluxo de trabalho")
  
    > [!NOTE]
    > Um valor **Sim** na coluna **Projeto de Lista de Tarefas do SharePoint** da tabela de tipos de projeto da empresa refere-se a um EPT que cria uma lista de tarefas do SharePoint, onde a lista de tarefas fica visível no Project Web App, mas o SharePoint mantém o controle do projeto. Para saber mais sobre o gerenciamento de projetos como listas de tarefas do SharePoint, consulte [Project Server 2013 architecture](project-server-2013-architecture.md). 
  
2. Abra a página de projetos no Project Web App e, em seguida, crie um projeto usando o novo EPT (consulte a Figura 13). Como **Teste ramificação fluxo de trabalho** é associado **a ramificação fluxo de trabalho**, criação do projeto é iniciado sob o controle do fluxo de trabalho.
    
    **Figura 13. Criando um projeto com o EPT Fluxo de Trabalho de Ramificação de Teste**

    ![Como criar um projeto com o EPT] (media/pj15_CreateWorkflowSPD_NewProject.gif "Como criar um projeto com o EPT")
  
3. Quando o fluxo de trabalho exibe as **Informações do projeto** PDP, adicione dados para os campos do projeto. Por exemplo, insira um valor de **Custo da proposta** de 30000. Versão em inglês dos EUA do Project Server altera o campo para mostrar a US $30.000 (consulte a Figura 14).
    
    **Figura 14. Usando o PDP Informações do Projeto**

    ![Usando o PDP editadas de informações de projeto] (media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "Usando o PDP editadas de informações de projeto")
  
4. Na guia **PROJETO** da faixa de opções, no grupo **Projeto**, escolha **Salvar**. O Project Server adiciona os dados do PDP ao projeto e então mostra a página Status do Fluxo de Trabalho (consulte a Figura 15). Para ver a descrição completa do estágio Detalhes Iniciais da Proposta no diagrama de status do fluxo de trabalho, passe o ponteiro do mouse sobre o estágio no diagrama de visualização do fluxo de trabalho.
    
    A grade **Todos os Estágios do Fluxo de Trabalho** usa uma seta verde para mostrar que o estágio Detalhes Iniciais da Proposta está aguardando uma entrada. Isso acontece porque o fluxo de trabalho aguarda um evento de envio no estágio Detalhes Iniciais da Proposta. Se o fluxo de trabalho não tiver aguardado um evento de envio, você pode escolher **Avançar** no grupo **Página** para avançar para o próximo PDP. 
    
    **Figura 15. Usando a página Status do Fluxo de Trabalho no estágio Detalhes Iniciais da Proposta**

    ![Página de status do fluxo de trabalho após o primeiro estágio] (media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Página de status do fluxo de trabalho após o primeiro estágio")
  
    O diagrama de visualização do fluxo de trabalho mostra o estágio atual em verde. Na fase **Criar**, o estágio Detalhes Iniciais da Proposta é o estágio atual. 
    
5. Na faixa de opções, no grupo **Fluxo de Trabalho**, escolha **Enviar**.
    
    > [!TIP]
    > Se o controle **Enviar** estiver desabilitado, atualize a página. 
  
    Se o valor **Custo da Proposta** for maior do que US$ 25.000, o fluxo de trabalho se moverá para o estágio Rejeição Automatizada. A Figura 16 mostra o status do estágio Rejeição Automatizada quando você escolher **Enviar** novamente. Se o **Custo da Proposta** for de US$ 25.000 ou menos, o fluxo de trabalho se moverá para o estágio Detalhes do Projeto (consulte a Figura 17). 
    
    **Figura 16. O fluxo de trabalho é concluído no estágio Rejeição Automatizada**

    ![O fluxo de trabalho está concluído em rejeição automatizada] (media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "O fluxo de trabalho está concluído em rejeição automatizada")
  
    A Figura 17 mostra outro teste com uma proposta de projeto chamada **Testar 2 - ramificação**, onde o estágio de detalhes do projeto é atual na fase de criar. A fase gerenciar apresentações de uma luz azul a cor, que indica a fase ainda não está ativo.
    
    **Figura 17. O fluxo de trabalho prossegue para o estágio Detalhes do Projeto se o custo for inferior a US$ 25.000**

    ![Status do fluxo de trabalho no estágio de detalhes do projeto] (media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "Status do fluxo de trabalho no estágio de detalhes do projeto")
  
6. Se você avançar para o estágio Detalhes do Projeto, não haverá outros dados a serem adicionados na página padrão. Escolha **Enviar** novamente para avançar para o estágio Execução (consulte a Figura 18). 
    
    **Figura 18. O fluxo de trabalho está pronto para ser gerenciado no estágio Execução**

    ![Status do fluxo de trabalho no estágio de execução] (media/pj15_CreateWorkflowSPD_ExecutionStage.gif "Status do fluxo de trabalho no estágio de execução")
  
No estágio Detalhes do Projeto, o fluxo de trabalho não aguarda um evento de envio. Se o PDP Detalhes do Projeto incluir campos obrigatórios adicionais, o Project Server aguardará até você adicionar dados aos campos antes de prosseguir para o estágio Execução. Como definido no Fluxo de Trabalho de Ramificação, o estágio Execução também não aguarda um evento de envio. No estágio Execução, você pode editar o projeto como um gerente de projeto ou escolher **Fechar ** na guia **PROJETO** da faixa de opções. Quando você escolher **Fechar** poderá fazer check-in no projeto e editá-lo posteriormente ou deixar o projeto em check-out.

O projeto **Fluxo de Trabalho de Ramificação** é um exemplo simples que tem somente um teste de comparação. O fluxo de trabalho envolve três estágios na fase Criar e um estágio na fase Gerenciar do Gerenciamento de Propostas. Para testar cuidadosamente um fluxo de trabalho, você deverá testar todas as ramificações do fluxo de trabalho e usar valores extremos e típicos para ver se o comportamento é o esperado. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Importando um fluxo de trabalho do Visio

Para alterar o fluxo de trabalho, você pode criar ou modificar campos personalizados controlados por fluxo de trabalho e criar ou modificar o etapas e fases do fluxo de trabalho. Você pode usar o SharePoint Designer 2013 para adicionar condições, ações, loops e estágios e salve republicar o fluxo de trabalho. Para reutilizar ou manter um backup de um fluxo de trabalho, você poderá exportá-lo em um arquivo do Visio 2013. 
  
Você também pode criar ou editar o fluxo de trabalho no Visio 2013 e importe o arquivo para o SharePoint Designer 2013 para ser usado pelo Project Web App. Para usar um fluxo de trabalho não modificado, a instância do Project Web App deve incluir propriedades de estágio de fluxo de trabalho que são os mesmos na instância do Project Web App original. Para obter mais informações sobre como usar o Visio para ajudar a criar fluxos de trabalho, consulte o [desenvolvimento de fluxo de trabalho no SharePoint Designer 2013 e Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx).
  
> [!NOTE]
> Quando você importa um arquivo do Visio 2013 para uma instância diferente do Project Web App, os estágios tem diferente estágio GUIDs, mesmo se os nomes do estágio são iguais. Depois de importar o fluxo de trabalho, você deve configurar as propriedades de estágio e ação para usar valores que são específicos para a instância do Project Web App. 
> 
> Se você criar um fluxo de trabalho no Visio 2013, as etapas e ações adotadas tem sem propriedades que são específicas para uma instância do Project Web App porque o Visio não se conectar ao Project Web App. Quando você conecta o SharePoint Designer 2013 ao Project Web App, criar um fluxo de trabalho e depois importar o arquivo VSDX, substituirá o fluxo de trabalho ativo. Em seguida, você deve configurar as propriedades de estágio e ação para coincidir com os valores que o SharePoint Designer 2013 obtém do Project Web App. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>Para importar um fluxo de trabalho do Visio para o SharePoint Designer

1. No Visio 2013, crie um fluxo de trabalho simple. Por exemplo, execute as seguintes etapas:
    
   1. Abra o Visio e então crie um fluxo de trabalho. Escolha o painel **CATEGORIAS** para um novo fluxo de trabalho, escolha **Fluxograma**, escolha o modelo **Fluxo de Trabalho do Microsoft SharePoint 2013** no painel **Novo** e então escolha **Criar**. O fluxo de trabalho abre com uma forma Estágio chamada **Estágio 1**. O fluxo de trabalho inclui um componente Iniciar e uma forma Entrar e uma forma Sair como parte da forma Estágio.
    
      Quando você passe o mouse sobre a forma de estágio e escolha o ícone de **Propriedades** , a seleção é desabilitada. Você pode definir as propriedades estágio e ação depois de importar o diagrama de fluxo de trabalho para o SharePoint Designer 2013. 
    
      > [!NOTE]
      >  Os únicos estênceis de forma que você deve usar são os seguintes na lista de formas de Fluxo de Trabalho: 
      > - **Ações - fluxo de trabalho do SharePoint 2013**
      > - **Componentes - fluxo de trabalho do SharePoint 2013**
      > - **Condições - fluxo de trabalho do SharePoint 2013**
  
   2. No painel **Formas**, escolha **Formas Rápidas** e então arraste a forma Condição chamada **Se qualquer valor for igual ao valor** à direita da forma Estágio. 
    
   3. Na guia **Página Inicial** da faixa de opções, escolha a ferramenta **Conector** e então conecte a forma Sair no estágio à forma Condição (consulte a Figura 19). 
    
      **Figura 19. Conectando uma forma Estágio a uma forma Condição em um diagrama de fluxo de trabalho do Visio**

      ![Criando um diagrama de fluxo de trabalho no Visio] (media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Criando um diagrama de fluxo de trabalho no Visio")
  
   4. Arraste outras duas formas Estágio à direita da forma de condição. As formas se chamam **Estágio 2** e **Estágio 3**.
    
   5. Usando a ferramenta de **conector** , conecte-se à direita da forma condição à forma do **estágio 2**Enter. Escolha a ferramenta **ponteiro** , clique duas vezes a conexão para mostrar uma caixa de texto para o nome e depois nomeie a conexão Sim.
    
   6. Conecte a parte inferior da forma Condição à forma Entrar do **Estágio 3**. Com a ferramenta **Ponteiro**, clique com o botão direito do mouse na conexão e então escolha **Não**. Qualquer um dos métodos funciona para nomear os conectores como **Sim** ou **Não**.
    
   7. No painel **formas** , escolha **ações - fluxo de trabalho do SharePoint 2013**e arraste a ação de **aguardar o evento de projeto** para o meio da forma para **estágio 1** (consulte a Figura 20). 
    
      **Figura 20. Concluindo o fluxo de trabalho no Visio**

      ![Concluir o fluxo de trabalho no Visio] (media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "Concluir o fluxo de trabalho no Visio")
  
   8. Na guia **processo** da faixa de opções, no grupo de **Validação de diagrama** , escolha **Verificar diagrama**. Corrija quaisquer erros e salve o desenho. Por exemplo, nome o fluxo de trabalho de teste de arquivo de Visio.vsdx.
    
      Para obter informações sobre como corrigir erros de fluxo de trabalho, consulte os [erros de validação de fluxo de trabalho de solução de problemas do SharePoint Server 2013 no Visio 2013](http://msdn.microsoft.com/en-us/library/jj163971%28v=office.15%29.aspx).
    
2. Abra o SharePoint Designer 2013 e em seguida, abra o site do Project Web App mesmo que você usou para o exemplo de **Fluxo de trabalho ramificação** . 
    
3. Escolha os **fluxos de trabalho** no painel de **navegação** e, em seguida, criar um fluxo de trabalho de site (escolha **Fluxo de trabalho de Site** , na guia **fluxos de trabalho** da faixa de opções). Por exemplo, nome o fluxo de trabalho simples de fluxo de trabalho do Visio.
    
   Na caixa de diálogo **Criar fluxo de trabalho de Site** , certifique-se de que o tipo de plataforma é o **SharePoint 2013 Workflow - Project Server**. Escolha **criar**e SharePoint Designer abre o painel de **Designer baseado em texto** para o novo fluxo de trabalho. 
    
4. No grupo **Gerenciar** da guia **FLUXO DE TRABALHO** da faixa de opções, escolha **Configurações do Fluxo de Trabalho**.
    
5. No grupo **Gerenciar** , na guia **Configurações de fluxo de trabalho** da faixa de opções, escolha **Importar do Visio**e importe o arquivo de **fluxo de trabalho de teste de Visio.vsdx** salvo anteriormente. Uma caixa de diálogo do **Microsoft SharePoint Designer** avisa que o diagrama que você está importando contiver sem propriedades do fluxo de trabalho e perguntando se você deseja substituir o fluxo de trabalho atual. Escolha **Sim**. SharePoint Designer importa o diagrama de fluxo de trabalho, gera estênceis para as formas e exibe o painel **Visual Designer** que contém o fluxo de trabalho importado. 
    
6. Defina as propriedades de cada forma do estágio do fluxo de trabalho. Por exemplo, a primeira forma do estágio é nomeada **estágio 1 (inválido)**, porque ela não representa um estágio válido na instância do Project Web App conectada. Quando você seleciona ou passe o mouse sobre o estágio, você pode escolher o ícone de **Propriedades** no canto inferior esquerdo da forma estágio para mostrar a caixa de diálogo **Propriedades do estágio** caixa (consulte a Figura 21). Selecione o estágio de **Detalhes da proposta inicial** na lista suspensa **Estágio do projeto** e escolha **Okey**. SharePoint Designer renomeia o estágio.
    
   **Figura 21. Configurando a propriedade do estágio no SharePoint Designer**

   ![Definindo propriedades em um fluxo de trabalho importada] (media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Definindo propriedades em um fluxo de trabalho importada")
  
   Para o segundo estágio, defina a propriedade **Estágio do Projeto** como **Rejeição Automatizada**. Para o terceiro estágio, defina a propriedade **Estágio do Projeto** como **Execução**.
    
7. De maneira semelhante, para a ação **Aguardar evento de projeto**, defina a propriedade **Nome do Evento** como **Evento: Quando um projeto é enviado**.
    
8. Da mesma forma, defina as propriedades da condição **se qualquer valor for igual a valor** . Por exemplo, defina a propriedade **Value** primeira ao **Custo de dados: proposta de projeto**. Defina a propriedade **Operator** como **é menor que**. Defina a propriedade **Value** segunda para 5000.
    
9. Verifique se o fluxo de trabalho tem erros e então salve o fluxo de trabalho. Se não houver erros, você poderá alterar a exibição para o **Designer Baseado em Texto** (consulte a Figura 22). 
    
   **Figura 22. Exibindo o fluxo de trabalho importado no Designer Baseado em Texto**

   ![Exibindo o fluxo de trabalho importado] (media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Exibindo o fluxo de trabalho importado")
  
10. Publique o fluxo de trabalho. Se você salvar o fluxo de trabalho mas não publicá-lo, o fluxo de trabalho não estará disponível quando você criar um tipo de projeto corporativo.
    
11. Para testar o **fluxo de trabalho Simple do Visio** de importadas no Project Web App, crie um EPT que usa o fluxo de trabalho e, em seguida, criar projetos que usam o EPT novo, como fez para o exemplo de **Fluxo de trabalho ramificação** . Nesse caso, entretanto, os projetos que são menores que o custo de US $5.000 são rejeitados. 
    
Seguir as etapas neste artigo, você criou e testado um fluxo de trabalho ramificação simple usando o SharePoint Designer 2013 para definir diretamente os estágios, condições e ações que usa o fluxo de trabalho. Você também criou um diagrama para um fluxo de trabalho ramificação ainda mais simples usando o Visio 2013. Você importado o diagrama de fluxo de trabalho do Visio no SharePoint Designer 2013, onde você pode definir as propriedades de cada estágio, a condição e a ação da conexão com o Project Web App.
  
Visio 2013 e SharePoint Designer juntos oferecem maneiras convenientes para designers, gerentes de projeto, os desenvolvedores de fluxo de trabalho e testadores criar, compartilhar e personalizar designs de fluxo de trabalho para instalações diferentes do Project Server 2013 e Project Online. Para fluxos de trabalho que exigem acesso programático para o Project Server que o SharePoint Designer não fornece, você pode usar o Visual Studio 2012 com o modelo de objeto do cliente (CSOM).
  
## <a name="see-also"></a>Confira também

- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)
- [Início: Instalar e configurar o Gerenciador de fluxo de trabalho do SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163276%28office.15%29.aspx)
- [Noções básicas sobre como empacotar e implantar um fluxo de trabalho no SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj819316%28office.15%29.aspx)
- [Fluxos de trabalho no SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx)
- [Desenvolvimento de fluxos de trabalho no SharePoint Designer 2013 e no Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
- [Solucionando problemas de erros de validação de fluxo de trabalho do SharePoint Server 2013 no Visio 2013](http://msdn.microsoft.com/en-us/library/jj163971%28v=office.15%29.aspx)
- [Gerenciamento de demanda e fluxo de trabalho](http://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

