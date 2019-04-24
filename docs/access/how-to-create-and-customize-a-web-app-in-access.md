---
title: Criar e personalizar um aplicativo Web no Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
localization_priority: Priority
ms.openlocfilehash: d7d27e98189a5b6784e4db48c81a545b85f01fc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306089"
---
# <a name="create-and-customize-a-web-app-in-access"></a><span data-ttu-id="1d995-102">Criar e personalizar um aplicativo Web no Access</span><span class="sxs-lookup"><span data-stu-id="1d995-102">Create and customize a web app in Access</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d995-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="1d995-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
<span data-ttu-id="1d995-p102">Access 2013 apresenta um novo modelo de aplicativo, que permite aos especialistas da área criar de forma rápida os aplicativos baseados na Web. Acompanha Access um conjunto de modelos que podem ser usados para promover a criação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1d995-p102">Access 2013 features a new application model that enables subject matter experts to quickly create web-based applications. Included with Access are a set of templates that you can use to jump start creating your application.</span></span>

<span data-ttu-id="1d995-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="1d995-107"></span></span>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a><span data-ttu-id="1d995-108">Pré-requisitos para a criação de um aplicativo no Access 2013</span><span class="sxs-lookup"><span data-stu-id="1d995-108">Prerequisites for building an app with Access 2013</span></span>

<span data-ttu-id="1d995-109">Para acompanhar as etapas deste exemplo, será necessário:</span><span class="sxs-lookup"><span data-stu-id="1d995-109">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="1d995-110">Access</span><span class="sxs-lookup"><span data-stu-id="1d995-110">Access</span></span>
    
- <span data-ttu-id="1d995-111">Um ambiente de desenvolvimento do SharePoint</span><span class="sxs-lookup"><span data-stu-id="1d995-111">A SharePoint development environment</span></span>
    
<span data-ttu-id="1d995-112">Para obter mais informações sobre como configurar o ambiente de desenvolvimento do SharePoint, confira [Configurar um ambiente de desenvolvimento geral para o SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span><span class="sxs-lookup"><span data-stu-id="1d995-112">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span></span> 
  
<span data-ttu-id="1d995-113">Para saber mais sobre como obter o Access e o SharePoint, confira [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="1d995-113">For more information about obtaining Access and SharePoint, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span>

<span data-ttu-id="1d995-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="1d995-114"></span></span>

## <a name="create-the-app"></a><span data-ttu-id="1d995-115">Criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="1d995-115">Create the app</span></span>

<span data-ttu-id="1d995-p103">Imagine que você deseja criar um Access aplicativo que acompanha problemas em sua empresa. Antes de começar a criar as tabelas e vista do zero, você deve procurar um modelo de esquema que atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="1d995-p103">Suppose you want to create an Access app that tracks issues for your business. Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-issue-tracking-app"></a><span data-ttu-id="1d995-118">Para criar o aplicativo de acompanhamento de problemas</span><span class="sxs-lookup"><span data-stu-id="1d995-118">To create the issue tracking app</span></span>

1. <span data-ttu-id="1d995-119">Abra o Access e escolha a opção **Aplicativo da Web personalizado**.</span><span class="sxs-lookup"><span data-stu-id="1d995-119">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="1d995-p104">Digite um nome e um local da Web para o aplicativo. É possível também escolher um local na lista **Locais** e escolher **Criar**.</span><span class="sxs-lookup"><span data-stu-id="1d995-p104">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="1d995-122">Digite **Problemas** na caixa **O que deseja acompanhar?** e pressione ENTER.</span><span class="sxs-lookup"><span data-stu-id="1d995-122">Type **Issues** into the **What would you like to track?** box and then press ENTER.</span></span> 
    
   <span data-ttu-id="1d995-123">Uma lista de modelos que podem ser úteis para o acompanhamento de problemas é exibida na Figura 1.</span><span class="sxs-lookup"><span data-stu-id="1d995-123">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="1d995-124">**Figura 1. Modelos que correspondem à pesquisa de problemas**</span><span class="sxs-lookup"><span data-stu-id="1d995-124">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="1d995-125">![Modelos correspondentes à pesquisa de problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Modelos correspondentes à pesquisa por problemas")</span><span class="sxs-lookup"><span data-stu-id="1d995-125">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="1d995-126">Escolha **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="1d995-126">Choose **Issues**.</span></span>
    
<span data-ttu-id="1d995-127">O Access cria um conjunto de tabelas e de modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="1d995-127">Access creates a set of tables and views.</span></span>
  
## <a name="explore-the-app"></a><span data-ttu-id="1d995-128">Explorar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="1d995-128">Explore the app</span></span>
<span data-ttu-id="1d995-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="1d995-129"></span></span>

<span data-ttu-id="1d995-130">Para compreender se o esquema e os modos de exibição atendem às suas necessidades, será necessário testá-los.</span><span class="sxs-lookup"><span data-stu-id="1d995-130">To understand whether the schema and views meet your needs, you should examine them.</span></span>
  
<span data-ttu-id="1d995-p105">As tabelas criadas por meio da seleção do esquema Problemas serão exibidas no Painel Bloco. As tabelas Problemas, Clientes e Funcionários são o objeto principal do aplicativo. A tabela Problemas armazena informações sobre cada problema. Cada problema é aberto e atribuído por um funcionário em nome de um cliente. As tabelas Problemas Relacionados e Comentários do Problema desempenham um papel de suporte no aplicativo. A tabela Problemas Relacionados permite a vinculação de um problema a outro. A tabela Comentários do Problema armazena vários comentários para um único problema.</span><span class="sxs-lookup"><span data-stu-id="1d995-p105">The tables created by selecting the Issues schema are displayed in the Tile Pane. The Issues, Customer, and Employees tables are the main focus of the app. The Issues table stores information about each issue. Each issue is opened by and assigned to an employee on behalf of a customer. The Related Issues and Issue Comments tables play a supporting role in the app. The Related Issues table enables you to link one issue to another. The Issue Comments table stores multiple comments for a single issue.</span></span>
  
<span data-ttu-id="1d995-p106">Em um banco de dados de área de trabalho do Access (.accdb), os relacionamentos entre tabelas são gerenciados na janela **Relacionamentos**. Access 2013 Os aplicativos gerenciam os relacionamentos usando campos para definir o tipo de dados de **Pesquisa**. Teste os relacionamentos da tabela Problemas ao clicar com o botão direito de mouse no bloco **Problemas** e selecione **Editar Tabela**.</span><span class="sxs-lookup"><span data-stu-id="1d995-p106">In an Access desktop (.accdb) database, the relationships between tables are managed in the **Relationships** window. Access 2013 apps manage relationships by using fields set to the **Lookup** data type. Let's examine the relationships for the Issues table by right-clicking the **Issues** tile and selecting **Edit Table**.</span></span>
  
<span data-ttu-id="1d995-p107">O campo **Cliente** está relacionado à tabela **Clientes**. Para testar os relacionamentos, selecione o campo **Cliente** e, em seguida, **Modificar Pesquisas**. O **Assistente de pesquisa** é exibido como na Figura 2.</span><span class="sxs-lookup"><span data-stu-id="1d995-p107">The **Customer** field is related to the **Customers** table. To examine the relationship, select the **Customer** field and then select **Modify Lookups**. The **Lookup Wizard** is displayed, as shown in Figure 2.</span></span> 
  
<span data-ttu-id="1d995-144">**Figura 2. O assistente de pesquisa exibindo a relação da tabela Clientes**</span><span class="sxs-lookup"><span data-stu-id="1d995-144">**Figure 2. Lookup Wizard displaying the relationship to the Customers table**</span></span>

<span data-ttu-id="1d995-145">![Assistente de Pesquisa exibindo a relação](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Assistente de Pesquisa exibindo a relação")</span><span class="sxs-lookup"><span data-stu-id="1d995-145">![Lookup Wizard displaying the relationship](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Lookup Wizard displaying the relationship")</span></span>
  
<span data-ttu-id="1d995-146">A caixa de diálogo do assistente de pesquisa mostra que o campo **Cliente** está associado à tabela **Clientes** e para retornar ao campo **Nome para Exibição Nome Sobrenome** na tabela **Clientes**.</span><span class="sxs-lookup"><span data-stu-id="1d995-146">The Lookup Wizard dialog box shows that the **Customer** field is linked to the **Customers** table and to return the **Display Name First Last** field from the **Customers** table.</span></span> 
  
<span data-ttu-id="1d995-p108">Os campos **Aberto por**, **Atribuído por** e **Alterado por** estão relacionados à tabela **Funcionários**. Diversos outros campos também são definidos para o tipo de dados de **Pesquisa**. Nesses casos, o tipo de dados de pesquisa é usado para determinar os valores específicos a serem permitidos no campo.</span><span class="sxs-lookup"><span data-stu-id="1d995-p108">The **Opened By**, **Assigned To**, and **Changed By** fields are related to the **Employees** table. Several other fields are also set to the **Lookup** data type. In these cases, the Lookup data type is used to specify the specific values to allow for in the field.</span></span> 
  
<span data-ttu-id="1d995-p109">Feche a tabela **Problemas** e teste o Painel Bloco. Os três blocos superiores, para as tabelas **Problemas**, **Clientes** e **Funcionários** são exibidos de forma diferente em relação aos dois blocos inferiores, para as tabelas **Problemas Relacionados** e **Comentários do Problema**, como mostrado na Figura 3.</span><span class="sxs-lookup"><span data-stu-id="1d995-p109">Close the **Issues** table and examine the Tile Pane. The top three tiles, for the **Issues**, **Customers**, and **Employees** tables, are displayed differently than the bottom two tiles for the **Related Issues** and **Issue Comments** table, as shown in Figure 3.</span></span> 
  
<span data-ttu-id="1d995-152">**Figura 3. Painel Bloco para o esquema Problemas**</span><span class="sxs-lookup"><span data-stu-id="1d995-152">**Figure 3. Tile Pane for the Issues schema**</span></span>

<span data-ttu-id="1d995-153">![Painel Bloco para o esquema Problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Painel Bloco para o esquema de Problemas")</span><span class="sxs-lookup"><span data-stu-id="1d995-153">![Tile Pane for the Issues schema](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Tile Pane for the Issues schema")</span></span>
  
<span data-ttu-id="1d995-154">As tabelas **Problemas Relacionados** e **Comentários do Problema** estarão desativadas, pois devem ser ocultadas do usuário no navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="1d995-154">The **Related Issues** and **Issue Comments** tables are dimmed because they are to be hidden from the user in the web browser.</span></span> 
  
<span data-ttu-id="1d995-p110">Use o aplicativo para acompanhar alguns problemas. Para isso, clique em **Iniciar aplicativo** para abri-lo no navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="1d995-p110">Let's use the app to track some issues. To do this, click **Launch App** to open the app in your web browser.</span></span> 
  
<span data-ttu-id="1d995-p111">O aplicativo vai abrir a exibição **Lista de Problemas** da tabela Problemas. Antes de adicionar um problema, convém adicionar alguns clientes e funcionários. Clique no bloco **Clientes** para começar a adicioná-los.</span><span class="sxs-lookup"><span data-stu-id="1d995-p111">The app opens the **Issues List** view of the Issues table. Before adding an issue, it would be a good idea to add some customers and employees. Click the **Customers** tile to start adding customers.</span></span> 
  
<span data-ttu-id="1d995-160">Use o Seletor de Modo de Exibição para escolher um entre os três disponíveis para a tabela **Clientes**, rotulados como **Lista**, **Folha de Dados** e **Grupos**, como mostrado na Figura 4.</span><span class="sxs-lookup"><span data-stu-id="1d995-160">Use the View Selector to choose one of three views available for the **Customers** table, labeled **List**, **Datasheet**, and **Groups** as shown in Figure 4.</span></span> 
  
<span data-ttu-id="1d995-161">**Figura 4. Seletor de Modo de Exibição**</span><span class="sxs-lookup"><span data-stu-id="1d995-161">**Figure 4. View Selector**</span></span>

<span data-ttu-id="1d995-162">![Seletor de Modo de Exibição](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Seletor de Modo de Exibição")</span><span class="sxs-lookup"><span data-stu-id="1d995-162">![View Selector](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "View Selector")</span></span>
  
<span data-ttu-id="1d995-p112">Escolher **Lista** vai ativar o modo de exibição de **Lista de Clientes**, que é um modo de exibição de Detalhes da Lista. Detalhes da Lista é um dos modos de exibição Access gerados automaticamente quando você criar uma tabela. A principal característica que distingue o modo de exibição Detalhes da Lista é o painel de Lista exibido ao lado esquerdo da exibição. Esse painel é usado para filtrar e para navegar entre os registros no modo de exibição. Em um Access banco de dados de área de trabalho, implementar um modo de exibição de lista pesquisável exige um código escrito personalizado.</span><span class="sxs-lookup"><span data-stu-id="1d995-p112">Choosing **List** activates the **Customers List** view, which is a List Details view. List Details is one of the views Access automatically generates when you create a table. The main feature that distinguishes a List Details view is the list pane that appears on the left side of the view. The list pane is used to filter and navigate the records contained in the view. In an Access desktop database, implementing a searchable list view would require writing custom code.</span></span> 
  
<span data-ttu-id="1d995-p113">Escolher a **Folha de Dados** abrirá o modo de exibição **Folha de Dados de Clientes**. A Folha de Dados é outro tipo de visualização que o Access gera automaticamente quando cria uma tabela. Os modos de exibição de Folha de Dados são úteis para quem considerar mais fácil inserir, classificar e filtrar dados, como se o fizesse em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="1d995-p113">Choosing **Datasheet** opens the **Customers Datasheet** view. Datasheet is the other kind of view Access automatically generates when you create a table. Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span></span> 
  
<span data-ttu-id="1d995-p114">Escolher Grupos abrirá o Modo de Exibição de Resumo. Esse recurso pode ser usado para agrupar registros baseados em um campo e, opcionalmente, poderá calcular uma soma ou uma média.</span><span class="sxs-lookup"><span data-stu-id="1d995-p114">Choosing Groups opens a Summary view. Summary views can be used to group records based on a field and optionally calculate a sum or average.</span></span>
  
<span data-ttu-id="1d995-p115">À medida que adicionar clientes, use a Barra de Ações para adicionar, editar, salvar e excluir registros, além de cancelar edições. A Barra de Ações é uma barra de ferramentas personalizável, exibida na parte superior dos modos de exibição, como mostrado na Figura 5.</span><span class="sxs-lookup"><span data-stu-id="1d995-p115">As you're adding customers, use the Action Bar to add records, edit records, save records, delete records, and cancel edits. The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span>
  
<span data-ttu-id="1d995-175">**Figura 5. Barra de Ações**</span><span class="sxs-lookup"><span data-stu-id="1d995-175">**Figure 5. Action Bar**</span></span>

<span data-ttu-id="1d995-176">![Barra de Ações](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Barra de Ações")</span><span class="sxs-lookup"><span data-stu-id="1d995-176">![Action Bar](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Action Bar")</span></span>
  
<span data-ttu-id="1d995-p116">Ao adicionar alguns clientes e funcionários, abra o modo de exibição Lista de Problemas e comece a adicionar problemas. À medida que você digitar o nome de um cliente na caixa Cliente, serão exibidos um ou mais nomes de clientes, como mostrado na Figura 6.</span><span class="sxs-lookup"><span data-stu-id="1d995-p116">Once you've added some customers and employees open the Issues List view and start adding an issue. As you type the name of a customer into the into the Customer box, one or more of the customer names will appear, as shown in Figure 6.</span></span>
  
<span data-ttu-id="1d995-179">**Figura 6. Controle de Preenchimento Automático**</span><span class="sxs-lookup"><span data-stu-id="1d995-179">**Figure 6. AutoComplete control**</span></span>

<span data-ttu-id="1d995-180">![Controle de Preenchimento Automático](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "Controle de Preenchimento Automático")</span><span class="sxs-lookup"><span data-stu-id="1d995-180">![AutoComplete control](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoComplete control")</span></span>
  
<span data-ttu-id="1d995-p117">A caixa Cliente é um controle de preenchimento automático. Esse controle exibe uma lista de registros que correspondem ao que você estiver digitando dentro da caixa. Isso ajuda a garantir a precisão da entrada de dados.</span><span class="sxs-lookup"><span data-stu-id="1d995-p117">The Customer box is an AutoComplete control. The AutoComplete control displays a list of records that match what you're typing into the box. This helps ensure the accuracy of data entry.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="1d995-184">Personalizar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="1d995-184">Customize the app</span></span>
<span data-ttu-id="1d995-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="1d995-185"></span></span>

<span data-ttu-id="1d995-p118">Agora que você está familiarizado com o aplicativo, observe que o modo de exibição Lista de Problemas não inclui as informações de contato dos clientes. Personalize o aplicativo para adicionar o telefone comercial do cliente à tabela Problemas, à medida que o problema for criado.</span><span class="sxs-lookup"><span data-stu-id="1d995-p118">Now that you've taken a tour of the app, you notice that the Issues List view doesn't contain contact information for the customer. Let's customize the app to add the customer's work phone to the Issues table as the issue is being created.</span></span>
  
### <a name="to-add-a-field-to-the-issues-table"></a><span data-ttu-id="1d995-188">Para adicionar um campo à tabela Problemas</span><span class="sxs-lookup"><span data-stu-id="1d995-188">To add a field to the Issues table</span></span>

1. <span data-ttu-id="1d995-189">Abra o aplicativo no Access.</span><span class="sxs-lookup"><span data-stu-id="1d995-189">Open the app in Access.</span></span>
    
2. <span data-ttu-id="1d995-190">Selecione o bloco **Problemas**, escolha o ícone **Configurações/Ações** e selecione **Editar Tabela**.</span><span class="sxs-lookup"><span data-stu-id="1d995-190">Choose the **Issues** tile, choose the **Settings/Action** icon, and then choose **Edit Table**.</span></span>
    
3. <span data-ttu-id="1d995-191">Digite o **Número de Contato** na primeira célula em branco, na coluna **Nome do Campo**.</span><span class="sxs-lookup"><span data-stu-id="1d995-191">Enter **Contact Number** in the first blank cell in the **Field Name** column.</span></span> 
    
4. <span data-ttu-id="1d995-192">Escolha **Texto Curto** na coluna **Tipo de Dados**.</span><span class="sxs-lookup"><span data-stu-id="1d995-192">Choose **Short Text** in the **Data Type** column.</span></span> 
    
5. <span data-ttu-id="1d995-193">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="1d995-193">Choose **Save**.</span></span>
    
6. <span data-ttu-id="1d995-194">Feche a tabela Problemas.</span><span class="sxs-lookup"><span data-stu-id="1d995-194">Close the Issues table.</span></span>
    
<span data-ttu-id="1d995-195">Agora que você já tem um campo para armazenar o número de telefone, crie uma macro de dados para pesquisar as informações do contato.</span><span class="sxs-lookup"><span data-stu-id="1d995-195">Now that we have field in which to store the phone number, let's create a data macro to look up the contact information.</span></span>
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a><span data-ttu-id="1d995-196">Como criar a macro de dados para pesquisar informações de contato</span><span class="sxs-lookup"><span data-stu-id="1d995-196">To create the data macro to look up contact information</span></span>

1. <span data-ttu-id="1d995-197">No grupo **Criar**, selecione **Avançado** e escolha **Macro de Dados**.</span><span class="sxs-lookup"><span data-stu-id="1d995-197">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
2. <span data-ttu-id="1d995-198">Escolha **Criar Parâmetro**.</span><span class="sxs-lookup"><span data-stu-id="1d995-198">Choose **Create Parameter**.</span></span>
    
3. <span data-ttu-id="1d995-p119">Na caixa **Nome**, digite **CustID**. Na lista suspensa **Tipo**, escolha **Número (Decimal Flutuante).**</span><span class="sxs-lookup"><span data-stu-id="1d995-p119">In the **Name** box, enter **CustID**. In the **Type** dropdown, choose **Number (Floating Decimal).**</span></span>
    
4. <span data-ttu-id="1d995-201">Na lista suspensa **Adicionar Nova Ação**, escolha **LookupRecord**.</span><span class="sxs-lookup"><span data-stu-id="1d995-201">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span> 
    
5. <span data-ttu-id="1d995-202">Na lista suspensa **Pesquisar Novo Registro em**, escolha **Clientes**.</span><span class="sxs-lookup"><span data-stu-id="1d995-202">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span> 
    
6. <span data-ttu-id="1d995-203">Na caixa **Condição Where**, digite **[Clientes].[ID]=[CustID]**.</span><span class="sxs-lookup"><span data-stu-id="1d995-203">In the **Where Condition** box, enter **[Customers].[ID]=[CustID]**.</span></span> 
    
7. <span data-ttu-id="1d995-204">Escolha **SetReturnVar** na lista suspensa **Adicionar Nova Ação**.</span><span class="sxs-lookup"><span data-stu-id="1d995-204">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="1d995-p120">Serão exibidas duas listas suspensas **Adicionar Nova Ação**, uma dentro do bloco **LookupRecord** e outra fora **dele**. É necessário escolher a lista suspensa **Adicionar Nova Ação** dentro do bloco **LookupRecord**, como descrito na Figura 7.</span><span class="sxs-lookup"><span data-stu-id="1d995-p120">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block. You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="1d995-207">**Figura 7. Lista suspensa Adicionar Nova Ação**</span><span class="sxs-lookup"><span data-stu-id="1d995-207">**Figure 7. Add New Action dropdown**</span></span>

   <span data-ttu-id="1d995-208">![Lista suspensa Adicionar Nova Ação](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Lista suspensa Adicionar Nova Ação")</span><span class="sxs-lookup"><span data-stu-id="1d995-208">![Add New Action dropdown](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Add New Action dropdown")</span></span>
  
8. <span data-ttu-id="1d995-209">Na caixa **Nome**, digite **ContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="1d995-209">In the **Name** box, enter **ContactPhone**.</span></span> 
    
9. <span data-ttu-id="1d995-210">Na caixa **Expressão**, digite **[Clientes].[Telefone Comercial]**.</span><span class="sxs-lookup"><span data-stu-id="1d995-210">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
10. <span data-ttu-id="1d995-p121">Selecione **Salvar**. Digite **GetContactPhone** na caixa **Nome da Macro** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1d995-p121">Choose **Save**. Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="1d995-213">A macro deverá ser semelhante à macro exibida na Figura 8.</span><span class="sxs-lookup"><span data-stu-id="1d995-213">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="1d995-214">**Figura 8. Macro de dados GetContactPhone**</span><span class="sxs-lookup"><span data-stu-id="1d995-214">**Figure 8. GetContactPhone data macro**</span></span>

    <span data-ttu-id="1d995-215">![Macros de dados GetContactPhone](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "Macros de dados GetContactPhone")</span><span class="sxs-lookup"><span data-stu-id="1d995-215">![GetContactPhone data macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone data macro")</span></span>
  
11. <span data-ttu-id="1d995-216">Feche o Modo Design da macro.</span><span class="sxs-lookup"><span data-stu-id="1d995-216">Close macro Design View.</span></span>
    
<span data-ttu-id="1d995-217">Agora você está pronto para adicionar o campo **Número de Contato** ao formulário Lista de Problemas.</span><span class="sxs-lookup"><span data-stu-id="1d995-217">Now we're ready to add the **Contact Number** field to the Issues List form.</span></span> 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a><span data-ttu-id="1d995-218">Para adicionar o campo Número de Contato ao formulário Lista de Problemas</span><span class="sxs-lookup"><span data-stu-id="1d995-218">To add the Contact Number field to the Issues List form</span></span>

1. <span data-ttu-id="1d995-p122">Selecione a tabela **Problemas**. Desse modo, o formulário Lista de Problemas será selecionado.</span><span class="sxs-lookup"><span data-stu-id="1d995-p122">Choose the **Issues** table. This chooses the Issues list form.</span></span> 
    
2. <span data-ttu-id="1d995-221">No Seletor de Modo de Exibição, selecione **Lista**, clique no ícone **Configurações/Ações** e escolha **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1d995-221">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
3. <span data-ttu-id="1d995-222">Arraste o campo **Número de Contato** do painel **Lista do Campo** para o local do formulário no qual deseja que o número de contato seja exibido.</span><span class="sxs-lookup"><span data-stu-id="1d995-222">Drag the **Contact Number** field form the **Field List** pane to the location on the form where you want the contact number to be displayed.</span></span> 
    
4. <span data-ttu-id="1d995-223">Selecione a caixa de texto **Número de Contato** e clique em **Dados**.</span><span class="sxs-lookup"><span data-stu-id="1d995-223">Choose the **Contact Number** text box, and then click **Data**.</span></span> 
    
5. <span data-ttu-id="1d995-224">Na caixa **Nome do Controle**, digite **CustomerContact** e feche o menu pop-up **Dados**.</span><span class="sxs-lookup"><span data-stu-id="1d995-224">In the **Control Name** box, enter **CustomerContact** and then close the **Data** popup.</span></span> 
    
6. <span data-ttu-id="1d995-225">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="1d995-225">Choose **Save**.</span></span>
    
<span data-ttu-id="1d995-p123">Agora é necessário escrever uma macro de interface do usuário (UI), que copiará o campo **Telefone Comercial**, da tabela **Clientes** para o campo **Telefone de Contato** da tabela **Problemas**. O evento **After Update** do controle **CustomerAutocomplete** é um bom local para a macro.</span><span class="sxs-lookup"><span data-stu-id="1d995-p123">Now we should write a user interface (UI) macro that copies the **Work Phone** field from the **Customers** table into the **Contact Phone** field of the **Issues** table. The **After Update** event of the **CustomerAutocomplete** control is a good location for the macro.</span></span> 
  
### <a name="to-create-the-afterupdate-macro"></a><span data-ttu-id="1d995-228">Para criar uma macro AfterUpdate</span><span class="sxs-lookup"><span data-stu-id="1d995-228">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="1d995-229">Escolha o controle **CustomerAutocomplete**, selecione o botão **Ações** e clique em **Após Atualização**.</span><span class="sxs-lookup"><span data-stu-id="1d995-229">Choose the **CustomerAutocomplete** control, choose the **Actions** button, and then choose **After Update**.</span></span> 
    
    <span data-ttu-id="1d995-230">Uma macro em branco será aberta no Modo Design de macro.</span><span class="sxs-lookup"><span data-stu-id="1d995-230">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="1d995-231">Na lista suspensa **Adicionar Nova Ação**, escolha **RunDataMacro**.</span><span class="sxs-lookup"><span data-stu-id="1d995-231">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="1d995-232">Na lista suspensa **Nome da macro**, escolha **GetContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="1d995-232">In the **Macro Name** dropdown, choose **GetContactPhone**.</span></span> 
    
4. <span data-ttu-id="1d995-233">Na caixa **CustID**, digite **[CustomerAutocomplete]**.</span><span class="sxs-lookup"><span data-stu-id="1d995-233">In the **CustID** box, enter **[CustomerAutocomplete]**.</span></span> 
    
5. <span data-ttu-id="1d995-234">Na caixa **SetLocalVar**, digite **Phone**.</span><span class="sxs-lookup"><span data-stu-id="1d995-234">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="1d995-235">Quando você escolhe a macro de dados GetContactPhone criada anteriormente, o Access preenche automaticamente no nome do parâmetro e retorna variáveis para a macro.</span><span class="sxs-lookup"><span data-stu-id="1d995-235">When you chose the GetContactPhone data macro that was created earlier, Access automatically filled in the parameter name and return variable for the macro.</span></span>
    
    <span data-ttu-id="1d995-236">O número de telefone do cliente será armazenado em uma variável chamada Telefone.</span><span class="sxs-lookup"><span data-stu-id="1d995-236">The phone number for the customer is stored in a variable named Phone.</span></span>
    
6. <span data-ttu-id="1d995-237">A partir da lista suspensa **Adicionar Nova Ação**, escolha **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="1d995-237">From the **Add New Action** dropdown, choose **SetProperty**.</span></span> 
    
7. <span data-ttu-id="1d995-238">Na caixa **Nome do Controle**, digite **CustomerContact**.</span><span class="sxs-lookup"><span data-stu-id="1d995-238">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
8. <span data-ttu-id="1d995-239">Na lista suspensa **Propriedades**, escolha **Valor**.</span><span class="sxs-lookup"><span data-stu-id="1d995-239">In the **Property** dropdown, choose **Value**.</span></span> 
    
9. <span data-ttu-id="1d995-240">Na caixa **Valor**, digite **=[Phone]**.</span><span class="sxs-lookup"><span data-stu-id="1d995-240">In the **Value** box, enter **=[Phone]**.</span></span> 
    
10. <span data-ttu-id="1d995-241">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="1d995-241">Choose **Save**.</span></span>
    
    <span data-ttu-id="1d995-242">A macro deverá ser semelhante à macro exibida na Figura 9.</span><span class="sxs-lookup"><span data-stu-id="1d995-242">The macro should resemble the macro shown in Figure 9.</span></span>
    
    <span data-ttu-id="1d995-243">**Figura 9. Macro Após Atualização**</span><span class="sxs-lookup"><span data-stu-id="1d995-243">**Figure 9. After Update macro**</span></span>

    <span data-ttu-id="1d995-244">![Macro Após Atualização](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "Macro Após Atualização")</span><span class="sxs-lookup"><span data-stu-id="1d995-244">![After Update macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "After Update macro")</span></span>
  
11. <span data-ttu-id="1d995-245">Feche o Modo Design da macro.</span><span class="sxs-lookup"><span data-stu-id="1d995-245">Close macro Design View.</span></span>
    
12. <span data-ttu-id="1d995-p124">Feche o modo de exibição Lista de Problemas. Escolha **Sim**, quando for solicitado que você salve as alterações.</span><span class="sxs-lookup"><span data-stu-id="1d995-p124">Close the Issues List view. Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="1d995-248">Agora estamos prontos para testar a personalização.</span><span class="sxs-lookup"><span data-stu-id="1d995-248">Now we're ready to text the customization.</span></span> <span data-ttu-id="1d995-249">Clique em **Iniciar Aplicativo** para abrir o aplicativo no navegador da web e adicionar um problema novo.</span><span class="sxs-lookup"><span data-stu-id="1d995-249">Click **Launch App** to open the app in your web browser and then add a new issue.</span></span> <span data-ttu-id="1d995-250">A caixa **Número de Contato** será atualizada automaticamente depois que o nome do cliente for digitado, como mostra a Figura 10.</span><span class="sxs-lookup"><span data-stu-id="1d995-250">The **Contact Number** box updates automatically after the customer name is entered,  as shown in Figure 10.</span></span> 
  
<span data-ttu-id="1d995-251">**Figura 10. O modo de exibição Problemas atualizado com o número de telefone**</span><span class="sxs-lookup"><span data-stu-id="1d995-251">**Figure 10. Issues view updated with phone number**</span></span>

<span data-ttu-id="1d995-252">![O modo de exibição Problemas atualizado com o número de telefone](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "O modo de exibição Problemas atualizado com o número de telefone")</span><span class="sxs-lookup"><span data-stu-id="1d995-252">![Issues view updated with phone number](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Issues view updated with phone number")</span></span>
  
## <a name="conclusion"></a><span data-ttu-id="1d995-253">Conclusão</span><span class="sxs-lookup"><span data-stu-id="1d995-253">Conclusion</span></span>

<span data-ttu-id="1d995-p126">Usar um dos modelos de esquema que acompanham o é uma boa maneira de promover a criação de um Access aplicativo da Web. Os modos de exibição criados automaticamente por você contêm funcionalidades avançadas que exigem a implementação de código personalizado em um banco de dados de área de trabalho do Access.</span><span class="sxs-lookup"><span data-stu-id="1d995-p126">Using one of the schema templates included with is a good way to jump start the creation of an Access web app. The views that are automatically created for you contain advanced functionally that requires custom code to implement in a Access desktop database.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d995-256">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d995-256">See also</span></span>

- [<span data-ttu-id="1d995-257">Novidades para os desenvolvedores do Access 2013</span><span class="sxs-lookup"><span data-stu-id="1d995-257">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [<span data-ttu-id="1d995-258">Referência de aplicativo Web personalizado do Access</span><span class="sxs-lookup"><span data-stu-id="1d995-258">Access custom web app reference</span></span>](access-custom-web-app-reference.md)
  

