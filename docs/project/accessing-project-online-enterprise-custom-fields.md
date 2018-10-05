---
title: Acessar campos personalizados da empresa no Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online é um serviço do Office 365 que as empresas podem ampliar para atender às necessidades de negócios. Uma área de extensão é campos personalizados da empresa (ECFs). ECFs são campos de valor digitado que podem ser adicionados a projetos, recursos e tarefas. A tabela a seguir lista ECFs associar projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância do que ECF:'
ms.openlocfilehash: 978fdfbf4ba75382ad85b9f92f8ac4df5c7f97c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401150"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="c2c2f-106">Acessar campos personalizados da empresa no Project Online</span><span class="sxs-lookup"><span data-stu-id="c2c2f-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="c2c2f-107">Project Online é um serviço do Office 365 que as empresas podem ampliar para atender às necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="c2c2f-108">Uma área de extensão é campos personalizados da empresa (ECFs).</span><span class="sxs-lookup"><span data-stu-id="c2c2f-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="c2c2f-109">ECFs são campos de valor digitado que podem ser adicionados a projetos, recursos e tarefas.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="c2c2f-110">A tabela a seguir lista ECFs associar projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância do que ECF:</span><span class="sxs-lookup"><span data-stu-id="c2c2f-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="c2c2f-111">Nome do ECF</span><span class="sxs-lookup"><span data-stu-id="c2c2f-111">ECF Name</span></span>|<span data-ttu-id="c2c2f-112">Tipo ECF</span><span class="sxs-lookup"><span data-stu-id="c2c2f-112">ECF Type</span></span>|<span data-ttu-id="c2c2f-113">Association</span><span class="sxs-lookup"><span data-stu-id="c2c2f-113">Association</span></span>|<span data-ttu-id="c2c2f-114">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="c2c2f-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c2c2f-115">Justificativa</span><span class="sxs-lookup"><span data-stu-id="c2c2f-115">Justification</span></span>  <br/> |<span data-ttu-id="c2c2f-116">TEXT</span><span class="sxs-lookup"><span data-stu-id="c2c2f-116">TEXT</span></span>  <br/> |<span data-ttu-id="c2c2f-117">Project</span><span class="sxs-lookup"><span data-stu-id="c2c2f-117">Project</span></span>  <br/> |<span data-ttu-id="c2c2f-118">Um usuário final pode registrar estatísticas importantes e dados de integridade, com os resultados que incluem uma avaliação de integridade e uma ação individualizada plano rumo melhor integridade.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="c2c2f-119">Classificação de risco</span><span class="sxs-lookup"><span data-stu-id="c2c2f-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="c2c2f-120">TEXT</span><span class="sxs-lookup"><span data-stu-id="c2c2f-120">TEXT</span></span>  <br/> |<span data-ttu-id="c2c2f-121">Project</span><span class="sxs-lookup"><span data-stu-id="c2c2f-121">Project</span></span>  <br/> |<span data-ttu-id="c2c2f-122">Baixa</span><span class="sxs-lookup"><span data-stu-id="c2c2f-122">Low</span></span>  <br/> |
|<span data-ttu-id="c2c2f-123">RETORNO DO INVESTIMENTO</span><span class="sxs-lookup"><span data-stu-id="c2c2f-123">ROI</span></span>  <br/> |<span data-ttu-id="c2c2f-124">NÚMERO</span><span class="sxs-lookup"><span data-stu-id="c2c2f-124">NUMBER</span></span>  <br/> |<span data-ttu-id="c2c2f-125">Project</span><span class="sxs-lookup"><span data-stu-id="c2c2f-125">Project</span></span>  <br/> |<span data-ttu-id="c2c2f-126">2,10</span><span class="sxs-lookup"><span data-stu-id="c2c2f-126">2.10</span></span>  <br/> |
|<span data-ttu-id="c2c2f-127">Custo total</span><span class="sxs-lookup"><span data-stu-id="c2c2f-127">Total Cost</span></span>  <br/> |<span data-ttu-id="c2c2f-128">CUSTO</span><span class="sxs-lookup"><span data-stu-id="c2c2f-128">COST</span></span>  <br/> |<span data-ttu-id="c2c2f-129">Project</span><span class="sxs-lookup"><span data-stu-id="c2c2f-129">Project</span></span>  <br/> |<span data-ttu-id="c2c2f-130">US $1,031,514</span><span class="sxs-lookup"><span data-stu-id="c2c2f-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="c2c2f-131">Início da equipe</span><span class="sxs-lookup"><span data-stu-id="c2c2f-131">Launch Team</span></span>  <br/> |<span data-ttu-id="c2c2f-132">TEXT</span><span class="sxs-lookup"><span data-stu-id="c2c2f-132">TEXT</span></span>  <br/> |<span data-ttu-id="c2c2f-133">Resources</span><span class="sxs-lookup"><span data-stu-id="c2c2f-133">Resources</span></span>  <br/> |<span data-ttu-id="c2c2f-134">Sim</span><span class="sxs-lookup"><span data-stu-id="c2c2f-134">Yes</span></span>  <br/> |
|<span data-ttu-id="c2c2f-135">Função posição</span><span class="sxs-lookup"><span data-stu-id="c2c2f-135">Position Role</span></span>  <br/> |<span data-ttu-id="c2c2f-136">TEXT</span><span class="sxs-lookup"><span data-stu-id="c2c2f-136">TEXT</span></span>  <br/> |<span data-ttu-id="c2c2f-137">Resources</span><span class="sxs-lookup"><span data-stu-id="c2c2f-137">Resources</span></span>  <br/> |<span data-ttu-id="c2c2f-138">Testador</span><span class="sxs-lookup"><span data-stu-id="c2c2f-138">Tester</span></span>  <br/> |
|<span data-ttu-id="c2c2f-139">Status do Sinalizador</span><span class="sxs-lookup"><span data-stu-id="c2c2f-139">Flag Status</span></span>  <br/> |<span data-ttu-id="c2c2f-140">SINALIZADOR</span><span class="sxs-lookup"><span data-stu-id="c2c2f-140">FLAG</span></span>  <br/> |<span data-ttu-id="c2c2f-141">Task</span><span class="sxs-lookup"><span data-stu-id="c2c2f-141">Task</span></span>  <br/> |<span data-ttu-id="c2c2f-142">Não</span><span class="sxs-lookup"><span data-stu-id="c2c2f-142">No</span></span>  <br/> |
|<span data-ttu-id="c2c2f-143">Saúde</span><span class="sxs-lookup"><span data-stu-id="c2c2f-143">Health</span></span>  <br/> |<span data-ttu-id="c2c2f-144">TEXT</span><span class="sxs-lookup"><span data-stu-id="c2c2f-144">TEXT</span></span>  <br/> |<span data-ttu-id="c2c2f-145">Task</span><span class="sxs-lookup"><span data-stu-id="c2c2f-145">Task</span></span>  <br/> |<span data-ttu-id="c2c2f-146">Não especificado</span><span class="sxs-lookup"><span data-stu-id="c2c2f-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="c2c2f-147">ECFs são definidas na instância do Project Web Application (PWA), externa de qualquer projeto, recurso ou tarefa.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="c2c2f-148">Ainda assim, eles podem se tornar associados a um projeto, recurso ou tarefa.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="c2c2f-149">Este artigo fornece um olhar introdutório sobre campos personalizados usando um aplicativo de amostra e se concentra em recuperando valores de ECF.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="c2c2f-150">Você pode baixar o exemplo completo em https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-150">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="c2c2f-151">Além disso, Project Online suporta campos personalizados locais como somente leitura entidades específicas para o projeto específico, recurso ou tarefa.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="c2c2f-152">Para obter mais informações sobre campos personalizados locais, consulte o exemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="c2c2f-153">Materiais de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="c2c2f-153">Background materials</span></span>

<span data-ttu-id="c2c2f-154">Um artigo anterior, [desenvolvimento de um aplicativo do Project Online usando o modelo de objeto do cliente](developing-a-project-online-application-using-the-client-side-object-model.md), fornece um plano de fundo e a orientação inicial para desenvolver aplicativos usando o CSOM.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="c2c2f-155">Consulte este artigo para os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="c2c2f-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="c2c2f-156">Informações básicas sobre o projeto, edições autônomos e baseado em nuvem</span><span class="sxs-lookup"><span data-stu-id="c2c2f-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="c2c2f-157">Ambiente de desenvolvimento (edições do Visual Studio e bibliotecas de software)</span><span class="sxs-lookup"><span data-stu-id="c2c2f-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="c2c2f-158">Instalação de projeto do Visual Studio para um aplicativo .NET usando a biblioteca de CSOM</span><span class="sxs-lookup"><span data-stu-id="c2c2f-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="c2c2f-159">Conectando ao serviço Project Online</span><span class="sxs-lookup"><span data-stu-id="c2c2f-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="c2c2f-160">Etapas preliminares (nível da classe declarations)</span><span class="sxs-lookup"><span data-stu-id="c2c2f-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="c2c2f-161">A classe para esse aplicativo define dois itens de dados: o contexto de projeto e o dicionário de pwaECF.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="c2c2f-162">O objeto de contexto do projeto é parte do CSOM do projeto e conecta-se o aplicativo e a instância do PWA.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="c2c2f-163">Todas as solicitações ao serviço usam o contexto do projeto.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="c2c2f-164">O contexto precisa o ponto de extremidade de conexão para criar uma instância de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="c2c2f-165">O ponto de extremidade de conexão é a URL da sua instância do PWA.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="c2c2f-166">O dicionário pwaECF armazena o projeto ECFs definidas no nível do PWA.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="c2c2f-167">O dicionário usa o ECF. InternalName como a chave e o objeto CustomField como o valor.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="c2c2f-168">O dicionário é preenchido no método ListPWACustomFields e, em seguida, usado como uma referência no método Main.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="c2c2f-169">Método principal</span><span class="sxs-lookup"><span data-stu-id="c2c2f-169">Main method</span></span>

<span data-ttu-id="c2c2f-170">O método Main gerencia o fluxo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-170">The Main method manages the application flow.</span></span> <span data-ttu-id="c2c2f-171">Como com outros aplicativos que usam o Project Online CSOM Main inicializa o contexto do projeto.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="c2c2f-172">Recupere e listar os ECFs no Project Online PWA.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="c2c2f-173">Essa funcionalidade é implementada no método ListPWACustomFields.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="c2c2f-174">Recupere os projetos com campos personalizados e não personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="c2c2f-175">Ao recuperar projetos com ECFs, a solicitação de consulta para o serviço do Project Online precisa incluir os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="c2c2f-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="c2c2f-176">**IncludeCustomFields** &ndash; Esse item solicita o serviço para retornar uma coleção de PublishedProjects onde cada projeto publicado inclui uma extensão que ofereça suporte a campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="c2c2f-177">A menos que esse item for especificado, o Project Online retorna PublishedProject objetos que não incluem dados de campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="c2c2f-178">**IncludeCustomFields.CustomFields** &ndash; este item solicita o serviço para preencher os objetos PublishedProject com dados CustomFields.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="c2c2f-179">A solicitação a seguir especifica o Id do projeto e nome, bem como a extensão do objeto para campos personalizados e os valores de campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="c2c2f-180">Examine cada projeto.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-180">Examine each project.</span></span>
    
   <span data-ttu-id="c2c2f-181">Os objetos de projeto usados nesse aplicativo são o tipo de PublishedProject porque os valores são recuperados e exibidos.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="c2c2f-182">Se você precisar atualizar os valores de dados em um ou mais projetos, o projeto sendo submetido a atualização seria fazer check-out e o aplicativo usaria um objeto DraftProject para recuperar os valores e atualizar o projeto.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="c2c2f-183">Acessando as entradas ECF para um projeto</span><span class="sxs-lookup"><span data-stu-id="c2c2f-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="c2c2f-184">Cada instância ECF separa o valor do campo do restante das informações ECF.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="c2c2f-185">O valor do campo é armazenado como parte de um par de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="c2c2f-186">O restante das informações é armazenado em um objeto CustomField.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="c2c2f-187">Acessar valores de ECF em um projeto consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="c2c2f-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="c2c2f-188">Percorrendo a coleção CustomFields</span><span class="sxs-lookup"><span data-stu-id="c2c2f-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="c2c2f-189">Acessando a entrada adequada usando duas construções.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="c2c2f-190">Cada projeto armazena entradas ECF associadas em dois lugares, um conjunto de CustomFields enumeráveis e e os valores de campo como parte de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="c2c2f-191">Nos pares de chave/valor, o internalName é a chave e o valor do campo é o valor.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="c2c2f-192">Use um dicionário para manter e acessar os valores de campo.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="c2c2f-193">As propriedades ECF, que não seja os valores de campo são armazenadas em objetos CustomField, um objeto por projeto.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="c2c2f-194">Use um conjunto de CustomFields para acessar os ECFs associados a um projeto individual.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="c2c2f-195">Cada projeto armazena os ECFs associados em uma coleção onde cada entrada ECF consiste em uma chave--o nome interno do ECF – e um objeto que contém o valor do ECF.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="c2c2f-196">Transferi um dicionário para acessar entradas individuais da coleção.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="c2c2f-197">A declaração segue.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="c2c2f-198">O valor em uma entrada do dicionário corresponde ao tipo de dados do ECF.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="c2c2f-199">O objeto para cada ECF mapeado para um dos diversos tipos de.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="c2c2f-200">A maioria dos ECFs usam tipos de simples que se encaixam em variáveis standard.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="c2c2f-201">O fragmento a seguir mostra que o mínimo de processamento está envolvido para vários tipos:</span><span class="sxs-lookup"><span data-stu-id="c2c2f-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   <span data-ttu-id="c2c2f-202">A tabela de pesquisa de valores de texto, no entanto, requer processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="c2c2f-203">O aplicativo recupera a tabela de pesquisa apropriado do serviço e produz a instância ECF (com um ou vários valores) atravessando a tabela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="c2c2f-204">O fragmento de código a seguir mostra o processamento de texto ECFs, incluindo aqueles que possuem valores simples e aquelas que usam tabelas de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="c2c2f-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   <span data-ttu-id="c2c2f-205">Esse aplicativo simplesmente emite o valor (es); No entanto, é possível fazer mais significado a partir do valor de dados (es).</span><span class="sxs-lookup"><span data-stu-id="c2c2f-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="c2c2f-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="c2c2f-206">ListPWACustomFields</span></span>

<span data-ttu-id="c2c2f-207">O método ListPWACustomFields recupera e lista os ECFs associados aos projetos.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="c2c2f-208">Esse método lista os ECFs registrados na instância do PWA que pode ser associada aos projetos individuais.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="c2c2f-209">O ponto de entrada para acessar os ECFs usa o elemento CustomFields do contexto do projeto, como a solicitação de consulta a seguir:</span><span class="sxs-lookup"><span data-stu-id="c2c2f-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="c2c2f-210">O método não verifica para ver se um projeto usa um ECF específico.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c2c2f-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2c2f-211">See also</span></span>

- [<span data-ttu-id="c2c2f-212">Portal de desenvolvimento do Project</span><span class="sxs-lookup"><span data-stu-id="c2c2f-212">Project Development Portal</span></span>](https://developer.microsoft.com/en-us/project)
- [<span data-ttu-id="c2c2f-213">Visão geral: Campos personalizados da empresa e tabelas de pesquisa</span><span class="sxs-lookup"><span data-stu-id="c2c2f-213">Overview: Enterprise custom fields and lookup tables</span></span>](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- <span data-ttu-id="c2c2f-214">[Local e campos personalizados da empresa](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="c2c2f-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="c2c2f-215">Adicionar ou editar campos personalizados empresariais no Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2c2f-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

