---
title: Filtrar um modo de exibição usando uma macro em um aplicativo do Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: db4dbb71-1b22-4dfd-bc07-5f7d694fc038
description: Saiba como filtrar um modo de exibição em um aplicativo do Access usando a ação de macro RequeryRecords e uma macro de dados.
ms.openlocfilehash: 9cd8c74b3949a0bb496798df663b1b42fb2868d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765113"
---
# <a name="filter-a-view-by-using-a-macro-in-an-access-app"></a><span data-ttu-id="a2e5b-103">Filtrar um modo de exibição usando uma macro em um aplicativo do Access</span><span class="sxs-lookup"><span data-stu-id="a2e5b-103">Filter a view by using a macro in an Access app</span></span>

<span data-ttu-id="a2e5b-104">Saiba como filtrar um modo de exibição em um aplicativo do Access usando a ação de macro RequeryRecords e uma macro de dados.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-104">Learn how to filter a view in an Access app by using the RequeryRecords macro action and a data macro.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a2e5b-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 

<span data-ttu-id="a2e5b-107">O modo de exibição de lista padrão em um aplicativo de acesso permite filtrar os problemas nos valores que estão contidos nos campos.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-107">The default list view in an Access app enables you to filter the issues on values that are contained in the fields.</span></span> <span data-ttu-id="a2e5b-108">Pode haver instâncias onde você deseja filtrar um modo de exibição com base em um conjunto de condições, em vez de por um valor de correspondência.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-108">There may be instances where you'd like to filter a view based on a set of conditions instead of by matching a value.</span></span> <span data-ttu-id="a2e5b-109">Para fazer isso, você deve criar uma macro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-109">To do that you must create a macro.</span></span> <span data-ttu-id="a2e5b-110">Este artigo mostra como criar uma macro que filtrar um modo de exibição para exibir tarefas que passaram vencidas ou de vencimento nos próximos sete dias.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-110">This article shows you how to create a macro that filter a view to display tasks that are past due or due in the next 7 days.</span></span>
  
## <a name="prerequisites-for-building-an-app-with-access"></a><span data-ttu-id="a2e5b-111">Pré-requisitos para a criação de um aplicativo com o Access</span><span class="sxs-lookup"><span data-stu-id="a2e5b-111">Prerequisites for building an app with Access</span></span>
<span data-ttu-id="a2e5b-112"><a name="Access2013FilterViewByUsingMacro_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="a2e5b-112"></span></span>

<span data-ttu-id="a2e5b-113">Para executar as etapas neste exemplo, você precisa:</span><span class="sxs-lookup"><span data-stu-id="a2e5b-113">To follow the steps in this example, you need:</span></span>
  
- <span data-ttu-id="a2e5b-114">Access 2013</span><span class="sxs-lookup"><span data-stu-id="a2e5b-114">Access 2013</span></span>
- <span data-ttu-id="a2e5b-115">Um ambiente de desenvolvimento do SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="a2e5b-115">A SharePoint 2013 development environment</span></span>
    
> [!NOTE]
> <span data-ttu-id="a2e5b-116">Para obter mais informações sobre como configurar o ambiente de desenvolvimento do SharePoint, consulte [Configurar um ambiente de desenvolvimento geral para o SharePoint 2013](http://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a2e5b-116">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint 2013](http://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span></span> <span data-ttu-id="a2e5b-117">> Para obter mais informações sobre como adquirir o Access 2013 e SharePoint 2013, consulte os [Downloads](http://msdn.microsoft.com/en-US/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="a2e5b-117">>  For more information about obtaining Access 2013 and SharePoint 2013, see [Downloads](http://msdn.microsoft.com/en-US/office/apps/fp123627).</span></span> 
  
## <a name="create-the-app"></a><span data-ttu-id="a2e5b-118">Criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="a2e5b-118">Create the app</span></span>
<span data-ttu-id="a2e5b-119"><a name="Access2013FilterViewByUsingMacro_CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="a2e5b-119"></span></span>

<span data-ttu-id="a2e5b-120">Suponha que você deseja criar um aplicativo de acesso que rastreia as tarefas para a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-120">Suppose you want to create an Access app that tracks tasks for your business.</span></span> <span data-ttu-id="a2e5b-121">Antes de começar a criar as tabelas e modo de exibição, você deve procurar um modelo de esquema.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-121">Before you start creating the tables and view, you should search for a schema template.</span></span>
  
### <a name="to-create-the-task-tracking-app"></a><span data-ttu-id="a2e5b-122">Para criar a aplicativo de controle de tarefa</span><span class="sxs-lookup"><span data-stu-id="a2e5b-122">To create the task tracking app</span></span>

1. <span data-ttu-id="a2e5b-123">Abra o Access e escolha a opção **Aplicativo da Web personalizado**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-123">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="a2e5b-p105">Digite um nome e um local da Web para o aplicativo. É possível também escolher um local na lista **Locais** e escolher **Criar**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-p105">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="a2e5b-126">Digite **tarefas** na caixa **Pesquisar** e pressione ENTER.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-126">Type **tasks** into the **Search** box and then press ENTER.</span></span> 
    
    <span data-ttu-id="a2e5b-127">Uma lista de modelos que podem ser úteis para controle de tarefas é exibida na Figura 1.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-127">A list of templates that might be useful for tracking tasks is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="a2e5b-128">**Figura 1. Modelos que correspondem a pesquisa para tarefas**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-128">**Figure 1. Templates that match the search for tasks**</span></span>

   <span data-ttu-id="a2e5b-129">![Modelos correspondentes à pesquisa de problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Modelos correspondentes à pesquisa por problemas")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-129">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="a2e5b-130">Escolha **tarefas**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-130">Choose **Tasks**.</span></span>
    
<span data-ttu-id="a2e5b-131">O Access cria um conjunto de tabelas e de modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-131">Access creates a set of tables and views.</span></span>
  
<span data-ttu-id="a2e5b-132">Insira várias tarefas de amostra e os funcionários em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-132">Enter several sample tasks and employees in your app.</span></span> <span data-ttu-id="a2e5b-133">Para fazer isso, escolha **O aplicativo de início** para abrir o aplicativo no seu navegador da web.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-133">To do this, choose **Launch App** to open the app in your web browser.</span></span> <span data-ttu-id="a2e5b-134">Insira um valor no campo de **Data de conclusão** de cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-134">Enter a value in the **Due Date** field for each task.</span></span> <span data-ttu-id="a2e5b-135">Volte para o Access quando terminar.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-135">Return to Access when you're done.</span></span> 
  
## <a name="plan-the-customizations"></a><span data-ttu-id="a2e5b-136">Planejar as personalizações</span><span class="sxs-lookup"><span data-stu-id="a2e5b-136">Plan the customizations</span></span>
<span data-ttu-id="a2e5b-137"><a name="Access2013FilterViewByUsingMacro_PlanCustomizations"> </a></span><span class="sxs-lookup"><span data-stu-id="a2e5b-137"></span></span>

<span data-ttu-id="a2e5b-138">Agora você tem um aplicativo que contém várias tarefas.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-138">You now have an app that contains several tasks.</span></span> <span data-ttu-id="a2e5b-139">O modo de exibição padrão habilita a procura por quaisquer tarefas que usam os itens que são armazenados nos campos exibidos no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-139">The default view enables you to search for any tasks using items that are stored in the fields displayed in the view.</span></span> <span data-ttu-id="a2e5b-140">Por exemplo, você pode pesquisar para problemas de alta prioridade ou em andamento.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-140">For example, you can search for high-priority issues or issues in progress.</span></span> <span data-ttu-id="a2e5b-141">Suponha que você deseja priorizar o seu trabalho exibindo questões ativas devem ser concluídas na semana seguinte.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-141">Suppose you want to prioritize your work by displaying active issues that are due in the coming week.</span></span> <span data-ttu-id="a2e5b-142">Para fazer isso, você deve criar uma macro (UI) da interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-142">To do this, you should create a user interface (UI) macro.</span></span>
  
<span data-ttu-id="a2e5b-143">O comando de macro da interface do usuário que você pode usar para filtrar a exibição é a [Ação de Macro RequeryRecords (aplicativo da web personalizado do Access)](requeryrecords-macro-action-access-custom-web-app.md).</span><span class="sxs-lookup"><span data-stu-id="a2e5b-143">The UI macro command that you can use to filter the view is the [RequeryRecords Macro Action (Access custom web app)](requeryrecords-macro-action-access-custom-web-app.md).</span></span> <span data-ttu-id="a2e5b-144">A ação de macro **RequeryRecords** filtra o modo de exibição com base no argumento *onde* , que é fornecido na forma de uma cláusula SQL WHERE.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-144">The **RequeryRecords** macro action filters the view based on the  *Where*  argument, which is provided in the form of a SQL WHERE clause.</span></span> <span data-ttu-id="a2e5b-145">Para filtrar o modo de exibição, você deve fornecer vários fatos em um formato específico para filtrar a exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-145">To filter the view, you must supply several facts in a specific format to filter the view.</span></span> 
  
<span data-ttu-id="a2e5b-146">Fatos relevantes são:</span><span class="sxs-lookup"><span data-stu-id="a2e5b-146">The relevant facts are:</span></span>
  
- <span data-ttu-id="a2e5b-147">O campo ou campos para comparar</span><span class="sxs-lookup"><span data-stu-id="a2e5b-147">The field or fields to compare</span></span>
    
- <span data-ttu-id="a2e5b-148">Como se referir a data de hoje</span><span class="sxs-lookup"><span data-stu-id="a2e5b-148">How to refer to today's date</span></span>
    
- <span data-ttu-id="a2e5b-149">Como se referir a um determinado dia em relação à data de hoje</span><span class="sxs-lookup"><span data-stu-id="a2e5b-149">How to refer to a particular day relative to today's date</span></span>
    
- <span data-ttu-id="a2e5b-150">Como determinar qual nas tarefas estejam em andamento</span><span class="sxs-lookup"><span data-stu-id="a2e5b-150">How to determine which on tasks are in progress</span></span>
    
<span data-ttu-id="a2e5b-151">O campo **Data de vencimento** fornece informações sobre quando é devida uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-151">The **Due Date** field provides information about when a task is due.</span></span> <span data-ttu-id="a2e5b-152">O campo **Status** fornece informações de status sobre cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-152">The **Status** field provides status information about each task.</span></span> <span data-ttu-id="a2e5b-153">Para se referir a um campo em uma macro, use o formato **[*TableName*]. [ *FieldName*]**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-153">To refer to a field in a macro, use the format **[*TableName*].[*FieldName*]**.</span></span> <span data-ttu-id="a2e5b-154">Uso **[tarefas]. [ Data de conclusão]** para referir-se o campo de **Data de conclusão** e **[tarefas]. [ Status]** para referir-se o campo **Status** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-154">Use **[Tasks].[Due Date]** to refer to the **Due Date** field and **[Tasks].[Status]** to refer to the **Status** field.</span></span> 
  
<span data-ttu-id="a2e5b-155">A função de [Função hoje (aplicativo da web personalizado do Access)](today-function-access-custom-web-app.md) retorna a data de hoje.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-155">The [Today Function (Access custom web app)](today-function-access-custom-web-app.md) function returns today's date.</span></span> <span data-ttu-id="a2e5b-156">A função de [Função DateAdd (aplicativo da web personalizado do Access)](dateadd-function-access-custom-web-app.md) pode ser usada para calcular uma data que seja um determinado número de dias após uma data especificada.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-156">The [DateAdd Function (Access custom web app)](dateadd-function-access-custom-web-app.md) function can be used to calculate a date that's a certain number of days after a specified date.</span></span> 
  
<span data-ttu-id="a2e5b-157">O campo **Status** contém vários valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-157">The **Status** field contains several possible values.</span></span> <span data-ttu-id="a2e5b-158">Um valor **concluído** indica que a tarefa não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-158">A value of **Completed** indicates that the task is no longer active.</span></span> 
  
<span data-ttu-id="a2e5b-159">Esses fatos podem ser combinados na seguinte cláusula SQL WHERE.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-159">These facts can be combined into the following SQL WHERE clause.</span></span>
  
```sql
[Tasks].[Due Date]<DateAdd(Day,7,Today()) AND [Tasks].[Status]<>"Completed"
```

<span data-ttu-id="a2e5b-160">Essa cláusula SQL WHERE é usada na macro para filtrar a exibição para exibir as questões ativas que devem ser concluídas nos próximos sete dias ou vencidas.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-160">This SQL WHERE clause is used in the macro to filter the view to display active issues that are due in the next 7 days or are past due.</span></span>
  
<span data-ttu-id="a2e5b-161">Para executar a macro da interface do usuário, ele precisa ser conectado a um item ou um evento que ocorre no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-161">To run the UI macro, it must be attached to an item or an event that occurs in the view.</span></span> <span data-ttu-id="a2e5b-162">A **Barra de ação** é um local conveniente para adicionar um comando personalizado ao modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-162">The **Action Bar** is a convenient place to add a custom command to the view.</span></span> <span data-ttu-id="a2e5b-163">A **Barra de ação** é uma barra de ferramentas personalizável que aparece na parte superior de cada modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-163">The **Action Bar** is a customizable toolbar that appears at the top of each view.</span></span> <span data-ttu-id="a2e5b-164">Por padrão, a **Barra de ação** contém botões para adicionar, editar, salvar, excluir e Cancelar edições.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-164">By default, the **Action Bar** contains buttons to add, edit, save, delete, and cancel edits.</span></span> <span data-ttu-id="a2e5b-165">Você pode adicionar botões que executam ações personalizadas, como o modo de exibição de filtragem.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-165">You can add buttons that perform custom actions, such as filtering the view.</span></span> 
  
<span data-ttu-id="a2e5b-166">Se o modo de exibição contém registros que atendam aos critérios especificados, **RequeryRecords** filtra o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-166">If the view contains records that meet the specified criteria, then **RequeryRecords** filters the view.</span></span> <span data-ttu-id="a2e5b-167">No entanto, se o modo de exibição não contiver registros que atendam aos critérios, que um novo registro em branco será exibido.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-167">However, if the view doesn't contain any records that meet the criteria, than a new, blank record is displayed.</span></span> <span data-ttu-id="a2e5b-168">Se você não desejar que um registro em branco a ser exibido se não há tarefas devem ser concluídas na próxima semana, você deve encontrar um método para verificar as tarefas antes de chamar a ação de macro **RequeryRecords** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-168">If you don't want a blank record to be displayed if no tasks are due in the next week, then you must find a method to check the tasks before you call the **RequeryRecords** macro action.</span></span> <span data-ttu-id="a2e5b-169">Para fazer isso, crie uma macro de dados para verificar se há registros que atendam aos critérios.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-169">To do this, create a data macro to check for records that meet the criteria.</span></span> 
  
<span data-ttu-id="a2e5b-170">A macro UI chamará a macro de dados, que tenta localizar uma tarefa vencer na próxima semana.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-170">The UI macro will call the data macro, which will try to find a task that's due in the next week.</span></span> <span data-ttu-id="a2e5b-171">Se a macro de dados localiza a tarefa e personalizar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-171">If the data macro finds the task then customize the app.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="a2e5b-172">Personalizar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="a2e5b-172">Customize the app</span></span>
<span data-ttu-id="a2e5b-173"><a name="Access2013FilterViewByUsingMacro_CustomizeApp"> </a></span><span class="sxs-lookup"><span data-stu-id="a2e5b-173"></span></span>

<span data-ttu-id="a2e5b-174">Agora que você determinou as personalizações, implementá-las.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-174">Now that you've determined the customizations, implement them.</span></span> <span data-ttu-id="a2e5b-175">A macro de dados deve ser criada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-175">The data macro should be created first.</span></span> <span data-ttu-id="a2e5b-176">Algumas macros de dados são conectadas diretamente a tabelas.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-176">Some data macros are attached directly to tables.</span></span> <span data-ttu-id="a2e5b-177">No entanto, essa macro de dados é uma macro de dados autônoma.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-177">However, this data macro is a stand-alone data macro.</span></span>
  
### <a name="to-create-the-data-macro"></a><span data-ttu-id="a2e5b-178">Para criar a macro de dados</span><span class="sxs-lookup"><span data-stu-id="a2e5b-178">To create the data macro</span></span>

1. <span data-ttu-id="a2e5b-179">Abra o aplicativo no Access.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-179">Open the app in Access.</span></span>
    
2. <span data-ttu-id="a2e5b-180">No grupo **Criar**, selecione **Avançado** e escolha **Macro de Dados**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-180">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
    <span data-ttu-id="a2e5b-181">Uma macro de dados em branco é aberta no modo de Design da macro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-181">A blank data macro is opened in macro Design View.</span></span>
    
3. <span data-ttu-id="a2e5b-182">Na caixa de listagem **Adicionar nova ação** , selecione **Pesquisarregistro**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-182">From the **Add New Action** list box, choose **LookupRecord**.</span></span>
    
4. <span data-ttu-id="a2e5b-183">Na caixa de listagem **Procurar backup de um registro em** , escolha **tarefas**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-183">In the **Look Up A Record In** list box, choose **Tasks**.</span></span>
    
5. <span data-ttu-id="a2e5b-184">Na caixa **Condição Where** , insira **[tarefas]. [ Data de conclusão]\<DateAdd(Day,7,Today()) e [tarefas]. [Status] \< \>"Concluída"**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-184">In the **Where Condition** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
6. <span data-ttu-id="a2e5b-185">Escolha **SetReturnVar** na caixa de listagem **Adicionar nova ação** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-185">Choose **SetReturnVar** from the **Add New Action** list box.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="a2e5b-186">Você verá duas caixas de listagem **Adicionar nova ação** , um dentro do bloco de **Pesquisarregistro** e outro fora do bloco de **Pesquisarregistro** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-186">You'll see two **Add New Action** list boxes, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="a2e5b-187">Você deve escolher a caixa de listagem **Adicionar nova ação** dentro do bloco **Pesquisarregistro** , conforme mostrado na Figura 1.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-187">You should choose the **Add New Action** list box within the **LookupRecord** block, as shown in Figure 1.</span></span> 
  
   <span data-ttu-id="a2e5b-188">**Figura 1. Adicionar caixa de listagem nova ação**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-188">**Figure 1. Add New Action list box**</span></span>

   <span data-ttu-id="a2e5b-189">![Lista suspensa Adicionar Nova Ação](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Lista suspensa Adicionar Nova Ação")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-189">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="a2e5b-190">Na caixa **nome** , digite **TaskFound**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-190">In the **Name** box, enter **TaskFound**.</span></span> 
    
8. <span data-ttu-id="a2e5b-191">Na caixa **expressão** , insira **"Sim"**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-191">In the **Expression** box, enter **"Yes"**.</span></span> 
    
9. <span data-ttu-id="a2e5b-192">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-192">Choose **Save**.</span></span> <span data-ttu-id="a2e5b-193">Digite **TasksDueSoon** na caixa **Nome da Macro** e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-193">Enter **TasksDueSoon** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="a2e5b-194">A macro deve se parecer com a macro mostrada na Figura 2.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-194">The macro should resemble the macro shown in Figure 2.</span></span>
    
   <span data-ttu-id="a2e5b-195">**Figura 2. Macro de dados TasksDueSoon**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-195">**Figure 2. TasksDueSoon data macro**</span></span>

   <span data-ttu-id="a2e5b-196">![Macro de dados TasksDueSoon] (media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "Macro de dados TasksDueSoon")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-196">![TasksDueSoon data macro](media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "TasksDueSoon data macro")</span></span>
  
10. <span data-ttu-id="a2e5b-197">Feche o Modo Design da macro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-197">Close macro Design View.</span></span>
    
<span data-ttu-id="a2e5b-198">Agora, estamos prontos para adicionar um botão personalizado à barra de ação.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-198">Now, we're ready to add a custom button to the Action Bar.</span></span>
  
### <a name="to-add-a-custom-button-to-the-action-bar"></a><span data-ttu-id="a2e5b-199">Para adicionar um botão personalizado à barra de ação</span><span class="sxs-lookup"><span data-stu-id="a2e5b-199">To add a custom button to the Action Bar</span></span>

1. <span data-ttu-id="a2e5b-200">Escolha a tabela de **tarefas** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-200">Choose the **Tasks** table.</span></span> <span data-ttu-id="a2e5b-201">Isso escolherá o formulário de lista de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-201">This chooses the Tasks List form.</span></span> 
    
2. <span data-ttu-id="a2e5b-202">No Seletor de Modo de Exibição, selecione **Lista**, clique no ícone **Configurações/Ações** e escolha **Editar**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-202">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
    <span data-ttu-id="a2e5b-203">O modo de exibição é aberto no modo de Design.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-203">The view is opened in Design View.</span></span>
    
3. <span data-ttu-id="a2e5b-204">Agora, estamos prontos para adicionar um botão personalizado à barra de ação.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-204">Now, we're ready to add a custom button to the Action Bar.</span></span> <span data-ttu-id="a2e5b-205">Para fazer isso, escolha **Adicionar de ação personalizada** , conforme mostrado na Figura 3.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-205">To do this, choose **Add custom action** as shown in Figure 3.</span></span> 
    
   <span data-ttu-id="a2e5b-206">**Figura 3. Adicionar botão de ação personalizada**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-206">**Figure 3. Add custom action button**</span></span>

   <span data-ttu-id="a2e5b-207">![Botão Adicionar ação personalizada] (media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Botão Adicionar ação personalizada")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-207">![Add custom action button](media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Add custom action button")</span></span>
  
    <span data-ttu-id="a2e5b-208">A nova ação é exibida como um botão com um ícone de estrela, conforme mostrado na Figura 4.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-208">The new action is displayed as a button with a star icon as shown in Figure 4.</span></span>
    
   <span data-ttu-id="a2e5b-209">**Figura 4. Novo botão de barra de ação**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-209">**Figure 4. New Action Bar button**</span></span>

   <span data-ttu-id="a2e5b-210">![Botão da barra de ação New] (media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "Botão da barra de ação New")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-210">![New Action Bar button](media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "New Action Bar button")</span></span>
  
4. <span data-ttu-id="a2e5b-211">Escolha o botão da barra de ação personalizada e, em seguida, escolha o ícone de **dados** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-211">Choose the custom Action Bar Button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="a2e5b-212">A caixa de diálogo de **dados** é exibida.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-212">The **Data** dialog box appears.</span></span> 
    
5. <span data-ttu-id="a2e5b-213">Na caixa **Nome do controle** , digite **FilterTasks**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-213">In the **Control Name** box, enter **FilterTasks**.</span></span> 
    
6. <span data-ttu-id="a2e5b-214">Na caixa **Dica de ferramenta** , insira a **exibição das tarefas antigas de vencimento ou de vencimento na próxima semana**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-214">In the **Tooltip** box, enter **Display tasks past due or due in the next week**.</span></span> 
    
<span data-ttu-id="a2e5b-215">Agora, estamos prontos para criar a macro de interface do usuário que filtrará o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-215">Now, we're ready to create the UI macro that will filter the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-filter-the-view"></a><span data-ttu-id="a2e5b-216">Para criar a macro UI para filtrar a exibição</span><span class="sxs-lookup"><span data-stu-id="a2e5b-216">To create the UI macro to filter the view</span></span>

1. <span data-ttu-id="a2e5b-217">Na caixa de diálogo **dados** , escolha **Na clique** conforme mostrado na Figura 5.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-217">In the **Data** dialog box, choose **On Click** as shown in Figure 5.</span></span> 
    
   <span data-ttu-id="a2e5b-218">**Figura 5. Caixa de diálogo de dados**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-218">**Figure 5. Data dialog box**</span></span>

   <span data-ttu-id="a2e5b-219">![Caixa de diálogo de dados] (media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Caixa de diálogo de dados")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-219">![Data dialog box](media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Data dialog box")</span></span>
  
    <span data-ttu-id="a2e5b-220">Uma macro UI em branco é aberta no modo de Design da macro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-220">A blank UI macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="a2e5b-221">Na caixa de listagem **Adicionar nova ação** , selecione **ExecutarMacrodeDados**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-221">From the **Add New Action** list box, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="a2e5b-222">Na caixa Nome da Macro, digite **TasksDueSoon**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-222">In the Macro Name box, enter **TasksDueSoon**.</span></span> 
    
    <span data-ttu-id="a2e5b-223">Na caixa **DefinirVarLocal** , insira **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-223">In the **SetLocalVar** box, enter **FilterRecords**.</span></span> 
    
    <span data-ttu-id="a2e5b-224">A ação **ExecutarMacrodeDados** chama a macro de dados **TasksDueSoon** criados anteriormente e armazena seu resultado em uma variável denominada **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-224">The **RunDataMacro** action calls the **TasksDueSoon** data macro we created earlier and stores its result in a variable named **FilterRecords**.</span></span> 
    
4. <span data-ttu-id="a2e5b-225">Na caixa da lista **Adicionar nova ação** , selecione **Se**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-225">From the **Add New Action** list box, choose **If**.</span></span> 
    
5. <span data-ttu-id="a2e5b-226">Na caixa de ferramentas **se** , insira **[FilterRecords] = "Yes"**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-226">In the **If** box, enter **[FilterRecords]="Yes"**.</span></span> 
    
6. <span data-ttu-id="a2e5b-227">Na caixa de listagem **Adicionar nova ação** , selecione **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-227">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="a2e5b-228">Você verá duas caixas de listagem **Adicionar nova ação** , um dentro do bloco **Se** e outro fora do bloco **se** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-228">You'll see two **Add New Action** list boxes, one within the **If** block, and another outside the **If** block.</span></span> <span data-ttu-id="a2e5b-229">Você deve escolher a caixa de listagem **Adicionar nova ação** dentro do bloco **Se** , conforme mostrado na Figura 6.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-229">You should choose the **Add New Action** list box within the **If** block, as shown in Figure 6.</span></span> 
  
   <span data-ttu-id="a2e5b-230">**Figura 6. Adicionar caixa de listagem nova ação**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-230">**Figure 6. Add New Action list box**</span></span>

   <span data-ttu-id="a2e5b-231">![Lista suspensa Adicionar Nova Ação](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Lista suspensa Adicionar Nova Ação")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-231">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="a2e5b-232">Na caixa **onde** , insira **[tarefas]. [ Data de conclusão]\<DateAdd(Day,7,Today()) e [tarefas]. [Status] \< \>"Concluída"**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-232">In the **Where** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
8. <span data-ttu-id="a2e5b-233">Na caixa **Order By** , insira **[Data de conclusão]**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-233">In the **Order By** box, enter **[Due Date]**.</span></span> 
    
9. <span data-ttu-id="a2e5b-234">Escolha o link **Adicionar Else** que aparece à direita da caixa **Adicionar nova ação** , conforme mostrado na Figura 7.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-234">Choose the **Add Else** link that appears to the right side of the **Add New Action** box as shown in Figure 7.</span></span> 
    
   <span data-ttu-id="a2e5b-235">**Figura 7. Adicionar link Else**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-235">**Figure 7. Add Else link**</span></span>

   <span data-ttu-id="a2e5b-236">![Adicione outro link] (media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Adicione outro link")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-236">![Add Else link](media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Add Else link")</span></span>
  
    <span data-ttu-id="a2e5b-237">Uma cláusula Else é adicionada à se bloco.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-237">An Else clause is added to the If block.</span></span>
    
10. <span data-ttu-id="a2e5b-238">Na caixa de listagem **Adicionar nova ação** , selecione **MessageBox**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-238">From the **Add New Action** list box, choose **MessageBox**.</span></span> 
    
11. <span data-ttu-id="a2e5b-239">Na caixa de **mensagem** , digite **sem tarefas estão atrasadas ou vencimento em próximos sete dias!**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-239">In the **Message** box, enter **No tasks are overdue or due in the next 7 days!**.</span></span> 
    
12. <span data-ttu-id="a2e5b-240">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-240">Choose **Save**.</span></span>
    
    <span data-ttu-id="a2e5b-241">A macro deverá ser semelhante à macro exibida na Figura 8.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-241">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="a2e5b-242">**Figura 8. Macro UI para filtrar a exibição**</span><span class="sxs-lookup"><span data-stu-id="a2e5b-242">**Figure 8. UI macro to filter the view**</span></span>

    <span data-ttu-id="a2e5b-243">![Macro UI para filtrar a exibição] (media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "Macro UI para filtrar a exibição")</span><span class="sxs-lookup"><span data-stu-id="a2e5b-243">![UI macro to filter the view](media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "UI macro to filter the view")</span></span>
  
13. <span data-ttu-id="a2e5b-244">Feche o Modo Design da macro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-244">Close macro Design View.</span></span>
    
<span data-ttu-id="a2e5b-245">Neste ponto, criamos a macro da interface do usuário que filtra o modo de exibição de lista de tarefas para exibir as tarefas urgentes.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-245">At this point, we've created the UI macro that filters the Tasks List view to display the urgent tasks.</span></span> <span data-ttu-id="a2e5b-246">Ele não seria recomendável deixar o modo de exibição em um estado filtrado sem fornecer um método para remover o filtro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-246">It wouldn't be polite to leave the view in a filtered state without providing a method to remove the filter.</span></span> <span data-ttu-id="a2e5b-247">Para fazer isso, adicione outro botão da barra de ação e Macro da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-247">To do this, add another Action Bar button and UI Macro.</span></span>
  
### <a name="to-add-an-action-bar-button-to-remove-the-filter"></a><span data-ttu-id="a2e5b-248">Para adicionar um botão da barra de ação para remover o filtro</span><span class="sxs-lookup"><span data-stu-id="a2e5b-248">To add an Action Bar Button to remove the filter</span></span>

1. <span data-ttu-id="a2e5b-249">Escolha **Adicionar de ação personalizada**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-249">Choose **Add custom action**.</span></span>
    
    <span data-ttu-id="a2e5b-250">A nova ação é exibida como um botão com um ícone de estrela</span><span class="sxs-lookup"><span data-stu-id="a2e5b-250">The new action is displayed as a button with a star icon</span></span>
    
2. <span data-ttu-id="a2e5b-251">Escolha o botão da barra de ação personalizado e, em seguida, escolha o ícone de **dados** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-251">Choose the custom Action Bar button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="a2e5b-252">A caixa de diálogo de **dados** é exibida.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-252">The **Data** dialog box appears.</span></span> 
    
3. <span data-ttu-id="a2e5b-253">Na caixa **Nome do controle** , digite **RemoveFilter**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-253">In the **Control Name** box, enter **RemoveFilter**.</span></span> 
    
4. <span data-ttu-id="a2e5b-254">Na caixa **Dica de ferramenta** , digite **Remover todos os filtros aplicados ao modo de exibição**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-254">In the **Tooltip** box, enter **Remove all filter applied to the view**.</span></span> 
    
<span data-ttu-id="a2e5b-255">Agora, estamos prontos para criar a macro de interface do usuário que removerá o modo de exibição do formulário de filtro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-255">Now, we're ready to create the UI macro that will remove the filter form the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-remove-the-filter-from-the-view"></a><span data-ttu-id="a2e5b-256">Para criar a macro de interface do usuário para remover o filtro da exibição</span><span class="sxs-lookup"><span data-stu-id="a2e5b-256">To create the UI macro to remove the filter from the view</span></span>

1. <span data-ttu-id="a2e5b-257">Na caixa de diálogo **dados** , escolha **Na clique**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-257">In the **Data** dialog box, choose **On Click**.</span></span>
    
    <span data-ttu-id="a2e5b-258">Uma macro UI em branco é aberta no modo de Design da macro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-258">A blank UI macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="a2e5b-259">Na caixa de listagem **Adicionar nova ação** , selecione **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-259">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    <span data-ttu-id="a2e5b-260">Neste momento, podemos vai deixe as caixas **Where** e **Order By** vazio.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-260">This time, we'll leave the **Where** and **Order By** boxes empty.</span></span> <span data-ttu-id="a2e5b-261">Em seguida, a ação **RequeryRecords** é chamada sem nenhum parâmetro, todos os filtros são removidos da exibição.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-261">Then the **RequeryRecords** action is called without any parameters, all filters are removed from the view.</span></span> 
    
3. <span data-ttu-id="a2e5b-262">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-262">Choose **Save**.</span></span>
    
4. <span data-ttu-id="a2e5b-263">Feche o Modo Design da macro.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-263">Close macro Design View.</span></span>
    
5. <span data-ttu-id="a2e5b-264">Feche o modo de exibição de lista de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-264">Close the Tasks List view.</span></span> <span data-ttu-id="a2e5b-265">Escolha **Sim**, quando for solicitado a salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-265">Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="a2e5b-266">Agora, estamos prontos para a personalização de texto.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-266">Now, we're ready to text the customization.</span></span> <span data-ttu-id="a2e5b-267">Escolha **O aplicativo de início** para abrir o aplicativo no seu navegador da web e escolha o botão da barra de ação FilterTasks personalizado.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-267">Choose **Launch App** to open the app in your web browser and then choose the custom FilterTasks Action Bar button.</span></span> <span data-ttu-id="a2e5b-268">Quaisquer tarefas antigas vencimento ou vencimento em próximos sete dias são exibidas.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-268">Any tasks past due or due in the next 7 days are displayed.</span></span> <span data-ttu-id="a2e5b-269">Uma mensagem é exibida se o aplicativo não contém urgentes tarefas.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-269">A message is displayed if the app contains no urgent tasks.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="a2e5b-270">Conclusão</span><span class="sxs-lookup"><span data-stu-id="a2e5b-270">Conclusion</span></span>

<span data-ttu-id="a2e5b-271">Você pode usar a ação de macro **RequeryRecords** em uma macro UI para filtrar a exibição com base nos critérios que você escolher.</span><span class="sxs-lookup"><span data-stu-id="a2e5b-271">You can use the **RequeryRecords** macro action in a UI macro to filter the view based on the criteria that you choose.</span></span> <span data-ttu-id="a2e5b-272">Dependendo de comportamento que você deseja, convém criar uma macro de dados para verificar se um registro atende aos critérios antes de usar a ação de macro **RequeryRecords** .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-272">Depending on the behavior that you want, you may want to create a data macro to verify that a record meets the criteria before you use the **RequeryRecords** macro action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2e5b-273">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2e5b-273">See also</span></span>

- [<span data-ttu-id="a2e5b-274">Novidades para os desenvolvedores do Access 2013</span><span class="sxs-lookup"><span data-stu-id="a2e5b-274">What's new for Access 2013 developers</span></span>](http://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx)
    

