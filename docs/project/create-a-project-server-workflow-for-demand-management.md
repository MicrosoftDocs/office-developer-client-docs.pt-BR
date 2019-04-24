---
title: Criar um fluxo de trabalho do Project Server para o Gerenciamento de Propostas
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: Este artigo descreve como criar um fluxo de trabalho simples com o SharePoint Designer 2013.
ms.openlocfilehash: bbefc5d30ccb508a24c32fe41e733e6e8187ecd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355475"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Criar um fluxo de trabalho do Project Server para o Gerenciamento de Propostas

Este artigo descreve como criar um fluxo de trabalho simples com o SharePoint Designer 2013. Você pode exportar o fluxo de trabalho para o Visio 2013 para visualização e edição, ou usar o Visio 2013 para criar fluxos de trabalho do Project Server 2013 e importar o design para o SharePoint Designer 2013 para publicação no Project Web App. Para saber mais sobre a plataforma de fluxo de trabalho do SharePoint e a criação de fluxos de trabalho com o Visio 2013 e o SharePoint Designer 2013, confira os artigos sobre [Fluxos de trabalho no SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) na documentação de desenvolvedor do SharePoint 2013. 
  
Para saber mais sobre a preparação do Project Server para fluxos de trabalho, consulte [Início: Instalar e configurar o Gerenciador de Fluxos de Trabalho do SharePoint 2013](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx).

<a name="pj15_CreateWorkflowSPD_General"> </a>

## <a name="creating-a-general-workflow"></a>Como criar um fluxo de trabalho geral

Use as etapas a seguir para criar um fluxo de trabalho do Project Server 2013 com o SharePoint Designer 2013. O fluxo de trabalho é projetado para o gerenciamento de propostas de projeto.
  
Para obter as etapas detalhadas, consulte a seção [Criando um fluxo de trabalho de ramificação](#pj15_CreateWorkflowSPD_Detailed). 
  
### <a name="to-create-a-project-server-workflow-general-procedure"></a>Para criar um fluxo de trabalho do Project Server (procedimento geral)

1. Determine os requisitos e então projete o fluxo de trabalho. Organize-o em fases e estágios e determine os campos personalizados que o fluxo de trabalho usará.
    
2. No Project Web App, crie as entidades exigidas pelo fluxo de trabalho:
    
    1. Examine as fases existentes do fluxo de trabalho; crie fases como o necessário.
        
    2. Crie os campos personalizados da empresa que o fluxo de trabalho usará. Para estar disponível em um estágio do fluxo de trabalho, um campo personalizado deverá ser controlado por um fluxo de trabalho.
        
    3. Edite ou crie as páginas de detalhes do projeto (PDPs) que os estágios do seu fluxo de trabalho usarão para coletar informações para o projeto. Neste exemplo, os estágios usarão PDPs padrão editados para incluírem um novo campo personalizado.
        
    4. Crie os estágios necessários do fluxo de trabalho e então associe cada estágio de fluxo de trabalho à fase correta.
    
3. No SharePoint Designer 2013, construa o fluxo de trabalho usando instruções declarativas no **Designer Baseado em Texto**:
    
    > [!NOTE]
    > Você também pode alternar para o **Designer Visual ** do SharePoint Designer 2013 ou importar um fluxo de trabalho existente do Visio 2013. Siga estas etapas para usar o **Designer Baseado em Texto**: 
    > 
    > 1. Abra o site do Project Web App e então crie um fluxo de trabalho de site que use a plataforma de fluxo de trabalho **Fluxo de Trabalho do SharePoint 2013 - Project Server**. 
    > 2. Adicione os estágios usados pelo fluxo de trabalho.
    > 3. Insira as etapas, as condições, as ações e os loops do fluxo de trabalho necessários em cada estágio.
    > 4. Verifique se há algum erro no fluxo de trabalho e corrija os que encontrar.
    > 5. (Opcional) Alterne do modo de exibição para o **Designer Visual**, ou de exportar o fluxo de trabalho para um arquivo do Visio 2013. Modifique o modo de exibição do Visio e salve as alterações no fluxo de trabalho atual. Edite o arquivo do Visio e importe-o para o SharePoint Designer 2013 para criar outros fluxos de trabalho.
    > 6. Publique o fluxo de trabalho. Depois de publicado, o fluxo de trabalho será mostrado na lista de fluxos de trabalho para o site do Project Web App.
    
4. No Project Web App, use o fluxo de trabalho para o gerenciamento de propostas de projeto:
    
    1. Crie um modelo de projeto corporativo (EPT) que use o fluxo de trabalho.
        
    2. Na página Centro de Projeto, crie um projeto que use o EPT para o fluxo de trabalho e então siga os estágios do fluxo de trabalho.
        
    3. Teste o fluxo de trabalho cuidadosamente.
        
    4. Implante o fluxo de trabalho em um servidor de produção.

<a name="pj15_CreateWorkflowSPD_Detailed"> </a>

## <a name="creating-a-branching-workflow"></a>Criando um fluxo de trabalho de ramificação

Antes de poder usar o SharePoint Designer 2013 para criar um fluxo de trabalho do Project Server, o serviço do cliente do Workflow Manager Client 1.0 deverá ser configurado para usar as atividades de fluxo de trabalho do Project Server 2013. Para saber mais sobre como configurar o Workflow Manager Client 1.0, confira os artigos sobre [Fluxos de trabalho no SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) na documentação de desenvolvedor do SharePoint Server 2013. 
  
O procedimento detalhado a seguir inclui as mesmas etapas da seção [Como criar um fluxo de trabalho geral](#pj15_CreateWorkflowSPD_General). 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>Para criar um fluxo de trabalho de ramificação do Project Server (procedimento detalhado)

#### <a name="1-plan-and-design-the-workflow"></a>1. Planeje e projete o fluxo de trabalho.

Um fluxo de trabalho do Project Server pode ser integrado a vários estágios e fases de um processo de gerenciamento de propostas. Como os fluxos de trabalho podem ser complexos, você deve compreender os requisitos de negócios e planejar um fluxo de trabalho com cuidado. Para obter um exemplo simples, projete um fluxo de trabalho de ramificação que use o custo estimado de uma proposta de projeto para determinar se a proposta será aceita. Se o custo estimado for maior que US$ 25.000, rejeite a proposta. Caso contrário, aceite a proposta e crie o projeto.
    
Já que você pode usar o Visio 2013 e o SharePoint Designer 2013 para ajudar a projetar e criar fluxos de trabalho do Project Server 2013, fica mais fácil experimentar fluxos de trabalho do que com o Project Server 2010. O exemplo de design de fluxo de trabalho deste artigo é o igual ao do artigo [Criar um fluxo de trabalho ramificação](https://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) do SDK do Project 2010. Você pode projetar e criar um fluxo de trabalho de teste em um computador remoto usando uma instância de teste do Project Web App, não sendo necessário criar fluxos de trabalho diretamente em um computador com o Project Server 2013. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Crie as entidades exigidas pelo seu fluxo de trabalho.

No Project Web App, examine as fases e estágio de fluxo de trabalho disponíveis e os campos personalizados empresariais disponíveis. Se necessário, crie as entidades exigidas pelo seu fluxo de trabalho, como nas etapas a seguir:
    
1. **Fases de fluxo de trabalho** A instalação padrão do Project Web App inclui as fases Criar, Selecionar, Planejar, Gerenciar e Concluído. Para o exemplo de fluxo de trabalho de ramificação, você não precisa criar outras fases. 
        
2. **Campos personalizados empresariais** O fluxo de trabalho de ramificação exige um campo personalizado de custo do projeto que é controlado pelo fluxo de trabalho. O valor de um campo personalizado controlado pelo fluxo de trabalho é definido em uma PDP que usa o fluxo de trabalho. Por exemplo, escolha o ícone de **Configurações** no canto superior direito de uma página do Project Web App, escolha **Configurações do PWA** e, em seguida, escolha **Campos personalizados empresariais e tabelas de pesquisa**.
        
   Crie um campo personalizado chamado Custo da Proposta para a entidade **Projeto** e selecione o tipo **Custo**. Para a descrição, digite o Custo estimado de uma proposta de projeto. Na seção **Comportamento**, escolha **Comportamento controlado por fluxo de trabalho**.
        
3. **Páginas de detalhes do projeto** Edite ou crie as PDPs que os estágios de fluxo de trabalho irão usar. Por exemplo, siga estas etapas: 
        
    1. Escolha **Páginas de Detalhes do Projeto** na página Configurações do Servidor e então escolha o PDP **ProjectInformation**. 
            
    2. Na guia **PÁGINA** da faixa de opções, no grupo **Editar**, escolha **Editar Página**.
            
    3. Escolha a seta para baixo no canto superior direito da web part **Informações Básicas** e então escolha **Editar web part**. Ou, na guia **WEB PART** da faixa de opções, no grupo **Propriedades**, escolha **Propriedades da web part** para mostrar a parte do editor. 
            
    4. Na seção **Campos do Projeto Exibidos** da parte do editor (consulte a Figura 1), escolha **Modificar**.
            
    5. Adicione o campo personalizado **Custo da Proposta**, mova-o para acima do campo **Proprietário** na lista **Campos do Projeto Selecionados** e então escolha **OK** (ver Figura 1).
      
    6. Na parte do editor, escolha **OK** e então escolha **Parar a Edição** no grupo **Editar**, na guia **PÁGINA** da faixa de opções. A Figura 2 mostra o campo personalizado **Proposal Cost** adicionado ao PDP Informações do Projeto. 

    **Figura 1. Edição da web part Campos do Projeto em uma PDP**

    ![Edição da web part Campos do Projeto em uma PDP](media/pj15_CreateWorkflowSPD_EditPDP.gif "Edição da web part Campos do Projeto em uma PDP")

    **Figura 2. A PDP editada inclui o campo personalizado Custo da Proposta**

    ![A PDP editada inclui o campo Custo da Proposta](media/pj15_CreateWorkflowSPD_EditedPDP.gif "A PDP editada inclui o campo Custo da Proposta")
  
4. **Estágios do fluxo de trabalho** Crie os estágios necessários para cada fase do fluxo de trabalho. Na página Configurações do Servidor, escolha **Estágios do Fluxo de Trabalho**, e então escolha **NOVO ESTÁGIO DO FLUXO DE TRABALHO**. A Figura 3 mostra parte da página Adicionar Estágio do Fluxo de Trabalho.
    
    **Figura 3. Como adicionar um estágio do fluxo de trabalho no Project Web App**

    ![Como adicionar um estágio de fluxo de trabalho no Project Web App](media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Como adicionar um estágio de fluxo de trabalho no Project Web App")
  
    O exemplo de fluxo de trabalho de ramificação usa os quatro estágios mostrados na Tabela 1. Nas **Configurações Adicionais da seção Página de Detalhes do Projeto Visível** da página Adicionar Estágio do Fluxo de Trabalho (não mostrada na Figura 3), os valores são opcionais. Eles fornecem mais informações sobre a página Status do Fluxo de Trabalho. Por exemplo, como a PDP de Detalhes da Proposta Inicial exige a inserção de dados pelo usuário, marque a caixa de seleção **A Página de Detalhes do Projeto requer atenção** e adicione uma descrição específica, como Definir o nome do projeto e o custo para esta PDP.
    
    A Figura 4 mostra os quatro estágios concluídos na página Estágios do Fluxo de Trabalho.
    
    **Tabela 1. Estágios para o fluxo de trabalho de ramificação**

    |Nome|Descrição|Descrição para envio|Fase|PDPs visíveis|Campos Personalizados|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Detalhes Iniciais da Proposta  <br/> |Defina o nome e o custo do projeto.  <br/> |Envie o projeto como uma proposta.  <br/> |Criar  <br/> |Informações do Projeto  <br/> Detalhes do Projeto  <br/> |Custo da Proposta (obrigatório)  <br/> |
    |Detalhes do Projeto  <br/> |Forneça detalhes sobre o projeto proposto.  <br/> |Envie detalhes para continuar com o projeto.  <br/> |Criar  <br/> |Informações do Projeto  <br/> Detalhes do Projeto  <br/> |Custo da Proposta (somente leitura)  <br/> |
    |Rejeição Automatizada  <br/> |A proposta é rejeitada, com base nas informações fornecidas.  <br/> | <br/> |Criar  <br/> |Informações do Projeto  <br/> |Custo da Proposta (somente leitura)  <br/> |
    |Execução  <br/> |A proposta é aceita e está pronta para o gerenciamento de projetos.  <br/> | <br/> |Gerenciar  <br/> |Informações do Projeto  <br/> Detalhes do Projeto  <br/> |Custo da Proposta (somente leitura)  <br/> |
   
    **Figura 4. Lista dos estágios do fluxo de trabalho no Project Web App**

    ![Lista de estágios do fluxo de trabalho no Project Web App](media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Lista de estágios do fluxo de trabalho no Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. Construa o fluxo de trabalho no Designer Baseado em Texto.

No SharePoint Designer 2013, construa o fluxo de trabalho usando instruções declarativas no Designer Baseado em Texto. Você pode começar a digitar na linha de inserção laranja para obter instruções de conclusão automática sensíveis ao contexto para a lógica e as etapas do fluxo de trabalho ou pode inserir a lógica e as etapas usando controles no grupo **Inserir** na guia **FLUXO DE TRABALHO** da faixa de opções. 
    
1. No modo de exibição Backstage do SharePoint Designer 2013, escolha **Abrir Site**. Por exemplo, abra o `https://ServerName/pwa`. No painel de **navegação**, clique em **Fluxos de Trabalho**. Em seguida, na guia **FLUXOS DE TRABALHO** da faixa de opções, no grupo **Novo**, escolha **Site do Fluxo de Trabalho**. Por exemplo, chame o fluxo de trabalho de Fluxo de Trabalho de Ramificação. Garanta que **Fluxo de Trabalho do SharePoint 2013 - Project Server** esteja selecionado como a lista suspensa **Tipo de Plataforma** (ver Figura 5). 
    
    **Figura 5. Como criar um fluxo de trabalho do site do Project Server**

    ![Uso d um fluxo de trabalho do site do Project Server](media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Como criar um fluxo de trabalho do site do Project Server")
  
2. Selecione a guia **Fluxo de Trabalho de Ramificação**. Em seguida, na guia **FLUXO DE TRABALHO** da faixa de opções, no grupo **Gerenciar**, na lista suspensa **Exibições**, escolha **Designer Baseado em Texto**. Para mostrar a exibição com a linha de inserção laranja piscando (consulta a Figura 6), clique na exibição.
    
    **Figura 6. Uso do modo de exibição de Designer Baseado em Texto para o fluxo de trabalho**

    ![Uso do modo de exibição de Designer Baseado em Texto para o fluxo de trabalho](media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "Usando o modo de exibição de Designer Baseado em Texto para o fluxo de trabalho")
  
3. Na exibição **Designer Baseado em Texto**, adicione os estágios usados pelo fluxo de trabalho. Na guia **FLUXO DE TRABALHO** da faixa de opções, no grupo **Inserir**, na lista suspensa **Estágio** em **Criar**, escolha **Detalhes Iniciais da Proposta**.
    
    De maneira semelhante, posicione a linha de inserção laranja abaixo da caixa **Estágio: Detalhes Iniciais da Proposta** e adicione os outros estágios usados pelo fluxo de trabalho: **Detalhes do Projeto**, **Rejeição Automatizada** e **Execução** (consulte a Figura 7). 
    
    **Figura 7. Como adicionar um estágio a um fluxo de trabalho no SharePoint Designer**

    ![Como adicionar um estágio a um fluxo de trabalho no SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Como adicionar um estágio a um fluxo de trabalho no SPD")
  
4. Adicione as etapas e a lógica do fluxo de trabalho em cada estágio: 
    
    1. No estágio **Detalhes Iniciais da Proposta**, posicione a linha de inserção laranja na parte superior do corpo do estágio. No grupo **Inserir** na faixa de opções, escolha **Ação**, role para baixo até **Ações do Project Web App** e então escolha **Aguardar Evento de Projeto**. Escolha **este evento de projeto** e então selecione **Evento: Quando um projeto é enviado** na lista suspensa. 
    
    2. Na seção **Transição para o estágio** do estágio **Detalhes Iniciais da Proposta**, insira **Se qualquer valor for igual ao valor**. Você pode começar a digitar a declaração ou usar o controle **Condição** no grupo **Inserir** na faixa de opções. 
    
    3. Escolha o primeiro controle de **valor** e então escolha **fx** para mostrar a caixa de diálogo **Definir Pesquisa de Fluxo de Trabalho** (consulte a Figura 8). Na lista suspensa **Fonte de dados**, selecione **Dados do Projeto**. Na lista suspensa **Campo da origem**, selecione **Custo da Proposta**.
    
       **Figura 8. Definição de um valor de pesquisa no fluxo de trabalho**

       ![Definição de um valor de pesquisa no fluxo de trabalho](media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Definição de um valor de pesquisa no fluxo de trabalho")
  
    4. Conclua a instrução `If` de forma que ela mostre o seguinte: **Se Dados do Projeto:Custo da Proposta for maior do que 25000**
    
       > [!NOTE]
       > Como alternativa, você poderia criar uma variável de fluxo de trabalho, definir uma variável como o valor do campo personalizado e então comprar a variável ao valor. Por exemplo, da lista suspensa **Variáveis Locais** na faixa de opções, crie uma variável chamada **TotalCost** (sem espaços) do tipo **Number**. Na caixa **Definir Pesquisa do Fluxo de Trabalho**, selecione **Variáveis e Parâmetros do Fluxo de Trabalho** como a fonte de dados e então selecione **Variável: TotalCost** como o campo. A instrução **Se** seria então: **Se a Variável: TotalCost for maior do que 25000**
  
    5. Posicione a linha de inserção laranja na ramificação `If` e então insira **Vá para um estágio** usando o controle **Ação** do grupo **Inserir** na faixa de opções. Escolha o controle da lista suspensa de **um estágio** e selecione o estágio **Rejeição Automatizada**. 
    
       Da mesma forma, na ramificação `Else`, insira a instrução **Ir para Detalhes do Projeto**. A Figura 9 mostra o estágio **Detalhes Iniciais da Proposta** concluído. 
    
       **Figura 9. Lógica concluída para o estágio Detalhes Iniciais da Proposta**

       ![Lógica concluída para o estágio Detalhes Iniciais da Proposta](media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Lógica concluída para o estágio Detalhes Iniciais da Proposta")
  
    6. No estágio **Rejeição Automatizada**, a menos que você queira pausar o fluxo de trabalho e mostrar alguns dados em um PDP, deixe a primeira seção vazia. A seção **Transição para o estágio** deve conter uma transição; como não há outro estágio após uma rejeição, digite Ir para o Fim do Fluxo de Trabalho para a instrução. 
    
    7. No estágio **Detalhes do Projeto**, adicione Ir para a Execução na seção **Transição para o estágio**. A menos que haja outros dados a serem adicionados, ou se você quiser pausar o fluxo de trabalho, não será necessário aguardar por um evento enviado. 
    
    8. No estágio **Execução**, a menos que queira pausar o fluxo de trabalho, deixe a seção de ação do estágio vazia. Na seção **Transição para o estágio**, adicione **Ir para o Fim do Fluxo de Trabalho**.
    
5. No grupo **Salvar** da faixa de opções, escolha **Verificar Erros** para verificar a existência de erros de fluxo de trabalho (consulte a Figura 10). Corrija qualquer erro e então escolha **Salvar**.
    
    **Figura 10. Como verificar o fluxo de trabalho em busca de erros no SharePoint Designer**

    ![Como verificar o fluxo de trabalho em busca de erros](media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Como verificar o fluxo de trabalho em busca de erros")
  
6. (Opcional) No grupo **Gerenciar** na faixa de opções, no menu suspenso **Exibições**, escolha **Visual Designer**. Na Figura 11, a exibição terá o zoom reduzido para 50%.
    
    Você pode editar itens no fluxo de trabalho usando o Virtual Designer. Por exemplo, selecione a condição **Se qualquer valor for igual ao valor**, escolha o ícone de ferramenta no canto inferior esquerda da condição e então selecione **Valor** para mostrar as condições de comparação na caixa de diálogo **Propriedades**. 
    
    **Figura 11. Uso do Designer Visual para um fluxo de trabalho**

    ![Uso do modo de exibição de design do fluxo de trabalho do Visio](media/pj15_CreateWorkflowSPD_SwitchView.gif "Usando o modo de exibição de design do fluxo de trabalho do Visio")
  
    Quando o fluxo de trabalho estiver no modo de exibição do Designer Visual, para salvar o fluxo de trabalho em um arquivo do Visio 2013 (.vsdx) como um backup ou para uso posterior, você poderá escolher **Exportar para o Visio**.
    
7. Publique o fluxo de trabalho. Quando você usa o SharePoint Designer 2013 para publicar o fluxo de trabalho no site ativo do Project Web App, o fluxo de trabalho será registrado no site do SharePoint ou no Azure e ficará disponível no Project Web App para novos EPTs.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. Crie um EPT para o fluxo de trabalho e então teste o fluxo de trabalho.

No Project Web App, crie um EPT para o fluxo de trabalho e então teste o fluxo de trabalho criando uma proposta de projeto:
    
1. Na página Configurações do PWA, escolha **Tipos de Projeto Corporativo**e crie um EPT chamado Fluxo de Trabalho de Ramificação de Teste. Desmarque as caixas de seleção **Criar novos projetos como Projetos de Lista de Tarefas do SharePoint**, dessa forma o Project Server manterá total controle dos projetos criados pela EPT. Selecione **Fluxo de Trabalho de Ramificação** na lista suspensa **Associação de Fluxo de Trabalho de Site** e selecione a PDP **Informações do Projeto** na lista suspensa **Nova Página do Projeto** para ser a primeira página que o fluxo de trabalho mostra. 
    
    **Figura 12. Adição de um EPT ao fluxo de trabalho**

    ![Adição de um EPT ao fluxo de trabalho](media/pj15_CreateWorkflowSPD_EPTs.gif "Adição de um EPT ao fluxo de trabalho")
  
    > [!NOTE]
    > Um valor **Sim** na coluna **Projeto de Lista de Tarefas do SharePoint** da tabela de tipos de projeto da empresa refere-se a um EPT que cria uma lista de tarefas do SharePoint, onde a lista de tarefas fica visível no Project Web App, mas o SharePoint mantém o controle do projeto. Para saber mais sobre o gerenciamento de projetos como listas de tarefas do SharePoint, consulte [Project Server 2013 architecture](project-server-2013-architecture.md). 
  
2. Abra a página Projetos no Project Web App e crie um projeto usando o novo EPT (ver Figura 13). Como o **Fluxo de Trabalho de Ramificação de Teste** está associado ao **Fluxo de Trabalho de Ramificação**, a criação do projeto começa sob controle do fluxo de trabalho.
    
    **Figura 13. Como criar um projeto com o EPT Fluxo de Trabalho de Ramificação de Teste**

    ![Como criar um projeto com o EPT](media/pj15_CreateWorkflowSPD_NewProject.gif "Como criar um projeto com o EPT")
  
3. Quando o fluxo de trabalho exibe a PDP **Informações do Projeto**, adicione dados aos campos do projeto. Por exemplo, insira um valor de **Custo da Proposta** de 30.000. A versão em inglês dos EUA do Project Server altera o campo para mostrar US$ 30.000 (ver Figura 14).
    
    **Figura 14. Uso da PDP Informações do Projeto editada**

    ![Uso da PDP Informações do Projeto editada](media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "Uso da PDP Informações do Projeto editada")
  
4. Na guia **PROJETO** da faixa de opções, no grupo **Projeto**, escolha **Salvar**. O Project Server adiciona os dados do PDP ao projeto e então mostra a página Status do Fluxo de Trabalho (consulte a Figura 15). Para ver a descrição completa do estágio Detalhes Iniciais da Proposta no diagrama de status do fluxo de trabalho, passe o ponteiro do mouse sobre o estágio no diagrama de visualização do fluxo de trabalho.
    
    A grade **Todos os Estágios do Fluxo de Trabalho** usa uma seta verde para mostrar que o estágio Detalhes Iniciais da Proposta está aguardando uma entrada. Isso acontece porque o fluxo de trabalho aguarda um evento de envio no estágio Detalhes Iniciais da Proposta. Se o fluxo de trabalho não tiver aguardado um evento de envio, você pode escolher **Avançar** no grupo **Página** para avançar para o próximo PDP. 
    
    **Figura 15. Uso da página Status do Fluxo de Trabalho no estágio Detalhes Iniciais da Proposta**

    ![Página Status do Fluxo de Trabalho depois da primeiro estágio](media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Página Status do Fluxo de Trabalho depois da primeiro estágio")
  
    O diagrama de visualização do fluxo de trabalho mostra o estágio atual em verde. Na fase **Criar**, o estágio Detalhes Iniciais da Proposta é o estágio atual. 
    
5. Na faixa de opções, no grupo **Fluxo de Trabalho**, escolha **Enviar**.
    
    > [!TIP]
    > Se o controle **Enviar** estiver desabilitado, atualize a página. 
  
    Se o valor **Custo da Proposta** for maior do que US$ 25.000, o fluxo de trabalho se moverá para o estágio Rejeição Automatizada. A Figura 16 mostra o status do estágio Rejeição Automatizada quando você escolher **Enviar** novamente. Se o **Custo da Proposta** for de US$ 25.000 ou menos, o fluxo de trabalho se moverá para o estágio Detalhes do Projeto (consulte a Figura 17). 
    
    **Figura 16. O fluxo de trabalho é concluído no estágio Rejeição Automatizada**

    ![O fluxo de trabalho é concluído em Rejeição Automatizada](media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "O fluxo de trabalho é concluído em Rejeição Automatizada")
  
    A Figura 17 mostra outro teste com uma proposta de projeto chamada **Teste 2 - Ramificação**, em que o estágio Detalhes do Projeto é atual na fase Criar. A fase Gerenciar é exibida na cor azul claro, o que indica que fase ainda não está ativa.
    
    **Figura 17. O fluxo de trabalho prossegue para o estágio Detalhes do Projeto se o custo for inferior a US$ 25.000**

    ![Status do Fluxo de Trabalho no estágio Detalhes do Projeto](media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "Status do Fluxo de Trabalho no estágio Detalhes do Projeto")
  
6. Se você avançar para o estágio Detalhes do Projeto, não haverá outros dados a serem adicionados na página padrão. Escolha **Enviar** novamente para avançar para o estágio Execução (consulte a Figura 18). 
    
    **Figura 18. O fluxo de trabalho está pronto para ser gerenciado no estágio Execução**

    ![Execução](media/pj15_CreateWorkflowSPD_ExecutionStage.gif "Status do Fluxo de Trabalho no estágio Execução")
  
No estágio Detalhes do Projeto, o fluxo de trabalho não aguarda um evento de envio. Se o PDP Detalhes do Projeto incluir campos obrigatórios adicionais, o Project Server aguardará até você adicionar dados aos campos antes de prosseguir para o estágio Execução. Como definido no Fluxo de Trabalho de Ramificação, o estágio Execução também não aguarda um evento de envio. No estágio Execução, você pode editar o projeto como um gerente de projeto ou escolher **Fechar ** na guia **PROJETO** da faixa de opções. Quando você escolher **Fechar** poderá fazer check-in no projeto e editá-lo posteriormente ou deixar o projeto em check-out.

O projeto **Fluxo de Trabalho de Ramificação** é um exemplo simples que tem somente um teste de comparação. O fluxo de trabalho envolve três estágios na fase Criar e um estágio na fase Gerenciar do Gerenciamento de Propostas. Para testar cuidadosamente um fluxo de trabalho, você deverá testar todas as ramificações do fluxo de trabalho e usar valores extremos e típicos para ver se o comportamento é o esperado. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Como importar um fluxo de trabalho do Visio

Para alterar o fluxo de trabalho, você pode criar ou modificar campos personalizados controlados pelo fluxo de trabalho e criar ou modificar fases e estágios do fluxo de trabalho. Você pode usar o SharePoint Designer 2013 para adicionar condições, ações, loops e estágios e, em seguida, salvar e republicar o fluxo de trabalho. Para reutilizar ou manter um backup de um fluxo de trabalho, você pode exportar para um arquivo do Visio 2013. 
  
Você também pode criar ou editar o fluxo de trabalho do Visio 2013 e importar o arquivo para o SharePoint Designer 2013 para usar com o Project Web App. Para usar um fluxo de trabalho não modificado, a instância do Project Web App deve incluir propriedades do estágio do fluxo de trabalho que são as mesmas da instância original do Project Web App. Para saber mais sobre como usar o Visio para ajudar a criar a luxos de trabalho, confira [Desenvolvimento de fluxos de trabalho no SharePoint Designer 2013 e no Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx).
  
> [!NOTE]
> Quando você importa um arquivo do Visio 2013 para outra instância do Project Web App, os estágios têm diferentes GUIDs de estágio, mesmo se os nomes dos estágios forem iguais. Depois de importar o fluxo de trabalho, você precisa configurar as propriedades de estágio e ação para usar valores específicos para a instância do Project Web App. 
> 
> Quando você cria um fluxo de trabalho do Visio 2013, os estágios e as ações não têm nenhuma propriedade específica para uma instância do Project Web App, uma vez que o Visio não se conecta com o Project Web App. Quando você conecta o SharePoint Designer 2013 ao Project Web App, cria um fluxo de trabalho e, depois, importa o arquivo VSDX, você substitui o fluxo de trabalho ativo. Então é necessário configurar as propriedades de estágio e ação para corresponder os valores que o SharePoint Designer 2013 obtém do Project Web App. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>Para importar um fluxo de trabalho do Visio para o SharePoint Designer

1. No Visio 2013, crie um fluxo de trabalho simples. Por exemplo, siga estas etapas:
    
   1. Abra o Visio e então crie um fluxo de trabalho. Escolha o painel **CATEGORIAS** para um novo fluxo de trabalho, escolha **Fluxograma**, escolha o modelo **Fluxo de Trabalho do Microsoft SharePoint 2013** no painel **Novo** e então escolha **Criar**. O fluxo de trabalho abre com uma forma Estágio chamada **Estágio 1**. O fluxo de trabalho inclui um componente Iniciar e uma forma Entrar e uma forma Sair como parte da forma Estágio.
    
      Quando você passa o mouse sobre a forma de estágio e escolhe o ícone **Propriedades**, a seleção é desabilitada. É possível definir as propriedades de estágio e ação depois de importar o diagrama de fluxo de trabalho para o SharePoint Designer 2013. 
    
      > [!NOTE]
      >  Os únicos estênceis de forma que você deve usar são os seguintes na lista de formas de Fluxo de Trabalho: 
      > - **Ações – Fluxo de Trabalho do SharePoint 2013**
      > - **Componentes – Fluxo de Trabalho do SharePoint 2013**
      > - **Condições – Fluxo de Trabalho do SharePoint 2013**
  
   2. No painel **Formas**, escolha **Formas Rápidas** e então arraste a forma Condição chamada **Se qualquer valor for igual ao valor** à direita da forma Estágio. 
    
   3. Na guia **Página Inicial** da faixa de opções, escolha a ferramenta **Conector** e então conecte a forma Sair no estágio à forma Condição (consulte a Figura 19). 
    
      **Figura 19. Conexão de uma forma Estágio a uma forma Condição em um diagrama de fluxo de trabalho do Visio**

      ![Como criar um diagrama de fluxo de trabalho no Visio](media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Como criar um diagrama de fluxo de trabalho no Visio")
  
   4. Arraste outras duas formas Estágio à direita da forma de condição. As formas se chamam **Estágio 2** e **Estágio 3**.
    
   5. Com a ferramenta **Conector**, conecte o lado direito da forma Condição à forma Inserir **Estágio 2**. Escolha a ferramenta **Ponteiro**, clique duas vezes na conexão para mostrar uma caixa de texto para o nome e, então, nomeie a conexão como Sim.
    
   6. Conecte a parte inferior da forma Condição à forma Entrar do **Estágio 3**. Com a ferramenta **Ponteiro**, clique com o botão direito do mouse na conexão e então escolha **Não**. Qualquer um dos métodos funciona para nomear os conectores como **Sim** ou **Não**.
    
   7. No painel **Formas**, escolha **Ações – Fluxo de Trabalho do SharePoint 2013** e então arraste a ação **Aguardar evento de projeto** para a parte central da forma para o **Estágio 1** (ver Figura 20). 
    
      **Figura 20. Como concluir o fluxo de trabalho no Visio**

      ![Como concluir o fluxo de trabalho no Visio](media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "Como concluir o fluxo de trabalho no Visio")
  
   8. Na guia **PROCESSO** da faixa de opções, no grupo **Validação de Diagrama**, escolha **Verificar Diagrama**. Corrija os erros e salve o desenho. Por exemplo, nomeie o arquivo como Fluxo de trabalho teste do Visio.vsdx.
    
      Para saber mais sobre a correção de erros de fluxo de trabalho, consulte [Como solucionar problemas de erros de validação de fluxo de trabalho do SharePoint Server 2013 no Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx).
    
2. Abra o SharePoint Designer 2013 e, em seguida, abra o mesmo site do Project Web App que você usou para o exemplo de **Fluxo de Trabalho de Ramificação**. 
    
3. Escolha **Fluxos de Trabalho** no painel **Navegação** e então crie um fluxo de trabalho de site (escolha **Fluxo de Trabalho de Site** na guia **FLUXOS DE TRABALHO** da faixa de opções). Por exemplo, nomeie o fluxo de trabalho como Fluxo de trabalho simples do Visio.
    
   Na caixa de diálogo **Criar Site de Fluxo de Trabalho**, verifique se o tipo de plataforma é **Fluxo de Trabalho do SharePoint 2013 – Project Server**. Escolha **Criar**, e o SharePoint Designer abrirá o painel **Designer Baseado em Texto** para o novo fluxo de trabalho. 
    
4. No grupo **Gerenciar** da guia **FLUXO DE TRABALHO** da faixa de opções, escolha **Configurações do Fluxo de Trabalho**.
    
5. No grupo **Gerenciar**, na guia **CONFIGURAÇÕES DE FLUXO DE TRABALHO** da faixa de opções, escolha **Importar do Visio** e, em seguida, importe o arquivo **Fluxo de trabalho de teste do Visio.vsdx** salvo anteriormente. Uma caixa de diálogo do **Microsoft SharePoint Designer** alerta que o diagrama que você está importando não contém propriedades de fluxo de trabalho e pergunta se deseja substituir o fluxo de trabalho atual. Escolha **Sim**. O SharePoint Designer importa o diagrama de fluxo de trabalho, cria estênceis para as formas e exibe o painel do **Designer Visual** que contém o fluxo de trabalho importado. 
    
6. Defina as propriedades de cada forma do estágio do fluxo de trabalho. Por exemplo, a primeira forma do estágio é chamada de **Estágio 1 (Inválido)** porque ela não representa um estágio válido na instância do Project Web App conectado. Quando você seleciona ou passa o mouse sobre o estágio, é possível escolher o ícone **Propriedades** na parte inferior esquerda da forma do estágio para mostrar a caixa de diálogo **Propriedades do Estágio** (ver Figura 21). Selecione o estágio **Detalhes Iniciais da Proposta** na lista suspensa **Estágio do Projeto** e, em seguida, escolha **OK**. O SharePoint Designer renomeia o estágio.
    
   **Figura 21. Configuração da propriedade do estágio no SharePoint Designer**

   ![Como configurar as propriedades em um fluxo de trabalho importado](media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Como configurar as propriedades em um fluxo de trabalho importado")
  
   Para o segundo estágio, defina a propriedade **Estágio do Projeto** como **Rejeição Automatizada**. Para o terceiro estágio, defina a propriedade **Estágio do Projeto** como **Execução**.
    
7. De maneira semelhante, para a ação **Aguardar evento de projeto**, defina a propriedade **Nome do Evento** como **Evento: Quando um projeto é enviado**.
    
8. Da mesma forma, defina as propriedades da condição **Se qualquer valor for igual ao valor**. Por exemplo, defina a primeira propriedade **Valor** como **Dados do Projeto:Custo da Proposta**. Configure a propriedade **Operador** como **é menor que**. Configure a segunda propriedade **Valor** como 5.000.
    
9. Verifique se o fluxo de trabalho tem erros e então salve o fluxo de trabalho. Se não houver erros, você poderá alterar a exibição para o **Designer Baseado em Texto** (consulte a Figura 22). 
    
   **Figura 22. Exibição do fluxo de trabalho importado no Designer Baseado em Texto**

   ![Exibição do fluxo de trabalho importado](media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Exibição do fluxo de trabalho importado")
  
10. Publique o fluxo de trabalho. Se você salvar o fluxo de trabalho mas não publicá-lo, o fluxo de trabalho não estará disponível quando você criar um tipo de projeto corporativo.
    
11. Para testar o **Fluxo de trabalho simples do Visio** importado no Project Web App, crie um EPT que use o fluxo de trabalho e então crie projetos que usem o novo EPT como fez para o exemplo de **Fluxo de Trabalho de Ramificação**. Nesse caso, no entanto, os projetos com custos inferiores a US$ 5.000 são rejeitados. 
    
Nas etapas deste artigo, você criou e testou um fluxo de trabalho de ramificação simples usando o SharePoint Designer 2013 para definir diretamente os estágios, condições e ações usadas pelo fluxo de trabalho. Você também criou um diagrama para um fluxo de trabalho de ramificação ainda mais simples usando o Visio 2013. Importou o diagrama de fluxo de trabalho do Visio para o SharePoint Designer 2013, onde você definiu as propriedades de cada estágio, condição e ação da conexão ao Project Web App.
  
O Visio 2013 e o SharePoint Designer juntos fornecem maneiras convenientes de designers, gerentes de projeto, desenvolvedores de fluxo de trabalho e testers criar, compartilhar e personalizar designs de fluxo de trabalho para diferentes instalações do Project Server 2013 e no Project Online. Para fluxos de trabalho que requerem acesso programático ao Project Server não fornecido pelo SharePoint Designer, é possível usar o Visual Studio 2012 com o modelo de objeto do lado cliente (CSOM).
  
## <a name="see-also"></a>Confira também

- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)
- [Início: Instalar e configurar o Gerenciador de fluxo de trabalho do SharePoint 2013](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx)
- [Compreensão de como empacotar e implantar fluxos de trabalho no SharePoint 2013](https://msdn.microsoft.com/library/jj819316%28office.15%29.aspx)
- [Fluxos de trabalho no SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx)
- [Desenvolvimento de fluxos de trabalho no SharePoint Designer 2013 e no Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
- [Solução de erros na validação dos fluxos de trabalho do SharePoint Server 2013 no Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx)
- [Fluxo de Trabalho e Gerenciamento de Propostas](https://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

