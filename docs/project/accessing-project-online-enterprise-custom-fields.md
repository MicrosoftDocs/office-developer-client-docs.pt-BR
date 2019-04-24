---
title: Acessar campos personalizados da empresa no Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'O Project Online é um serviço do Office 365 que as empresas podem estender para atender às necessidades de negócios. Uma área de extensão são os Campos Personalizados da Empresa (Enterprise Custom Fields – ECFs). Os ECFs são campos de valores tipados que podem ser adicionados a projetos, recursos e tarefas. A tabela a seguir lista os ECFs que se associam a projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância desse ECF:'
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355080"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="3cbf1-106">Acessar campos personalizados da empresa no Project Online</span><span class="sxs-lookup"><span data-stu-id="3cbf1-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="3cbf1-107">O Project Online é um serviço do Office 365 que as empresas podem estender para atender às necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="3cbf1-108">Uma área de extensão são os Campos Personalizados da Empresa (Enterprise Custom Fields – ECFs).</span><span class="sxs-lookup"><span data-stu-id="3cbf1-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="3cbf1-109">Os ECFs são campos de valores tipados que podem ser adicionados a projetos, recursos e tarefas.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="3cbf1-110">A tabela a seguir lista os ECFs que se associam a projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância desse ECF:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="3cbf1-111">Nome ECF</span><span class="sxs-lookup"><span data-stu-id="3cbf1-111">ECF Name</span></span>|<span data-ttu-id="3cbf1-112">Tipo ECF</span><span class="sxs-lookup"><span data-stu-id="3cbf1-112">ECF Type</span></span>|<span data-ttu-id="3cbf1-113">Association</span><span class="sxs-lookup"><span data-stu-id="3cbf1-113">Association</span></span>|<span data-ttu-id="3cbf1-114">Valor de Exemplo</span><span class="sxs-lookup"><span data-stu-id="3cbf1-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3cbf1-115">Justificação</span><span class="sxs-lookup"><span data-stu-id="3cbf1-115">Justification</span></span>  <br/> |<span data-ttu-id="3cbf1-116">TEXTO</span><span class="sxs-lookup"><span data-stu-id="3cbf1-116">TEXT</span></span>  <br/> |<span data-ttu-id="3cbf1-117">Project</span><span class="sxs-lookup"><span data-stu-id="3cbf1-117">Project</span></span>  <br/> |<span data-ttu-id="3cbf1-118">Um usuário final pode registrar estatísticas vitais e dados sobre a integridade, com resultados que incluem uma avaliação da integridade e um plano de ação individualizado para melhorá-la.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="3cbf1-119">Classificação de risco</span><span class="sxs-lookup"><span data-stu-id="3cbf1-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="3cbf1-120">TEXTO</span><span class="sxs-lookup"><span data-stu-id="3cbf1-120">TEXT</span></span>  <br/> |<span data-ttu-id="3cbf1-121">Project</span><span class="sxs-lookup"><span data-stu-id="3cbf1-121">Project</span></span>  <br/> |<span data-ttu-id="3cbf1-122">Baixo</span><span class="sxs-lookup"><span data-stu-id="3cbf1-122">Low</span></span>  <br/> |
|<span data-ttu-id="3cbf1-123">ROI</span><span class="sxs-lookup"><span data-stu-id="3cbf1-123">ROI</span></span>  <br/> |<span data-ttu-id="3cbf1-124">NÚMERO</span><span class="sxs-lookup"><span data-stu-id="3cbf1-124">NUMBER</span></span>  <br/> |<span data-ttu-id="3cbf1-125">Project</span><span class="sxs-lookup"><span data-stu-id="3cbf1-125">Project</span></span>  <br/> |<span data-ttu-id="3cbf1-126">2,10</span><span class="sxs-lookup"><span data-stu-id="3cbf1-126">2.10</span></span>  <br/> |
|<span data-ttu-id="3cbf1-127">Custo total</span><span class="sxs-lookup"><span data-stu-id="3cbf1-127">Total Cost</span></span>  <br/> |<span data-ttu-id="3cbf1-128">CUSTO</span><span class="sxs-lookup"><span data-stu-id="3cbf1-128">COST</span></span>  <br/> |<span data-ttu-id="3cbf1-129">Project</span><span class="sxs-lookup"><span data-stu-id="3cbf1-129">Project</span></span>  <br/> |<span data-ttu-id="3cbf1-130">US$ 1.031.514</span><span class="sxs-lookup"><span data-stu-id="3cbf1-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="3cbf1-131">Equipe de lançamento</span><span class="sxs-lookup"><span data-stu-id="3cbf1-131">Launch Team</span></span>  <br/> |<span data-ttu-id="3cbf1-132">TEXTO</span><span class="sxs-lookup"><span data-stu-id="3cbf1-132">TEXT</span></span>  <br/> |<span data-ttu-id="3cbf1-133">Recursos</span><span class="sxs-lookup"><span data-stu-id="3cbf1-133">Resources</span></span>  <br/> |<span data-ttu-id="3cbf1-134">Sim</span><span class="sxs-lookup"><span data-stu-id="3cbf1-134">Yes</span></span>  <br/> |
|<span data-ttu-id="3cbf1-135">Função de posição</span><span class="sxs-lookup"><span data-stu-id="3cbf1-135">Position Role</span></span>  <br/> |<span data-ttu-id="3cbf1-136">TEXTO</span><span class="sxs-lookup"><span data-stu-id="3cbf1-136">TEXT</span></span>  <br/> |<span data-ttu-id="3cbf1-137">Recursos</span><span class="sxs-lookup"><span data-stu-id="3cbf1-137">Resources</span></span>  <br/> |<span data-ttu-id="3cbf1-138">Testador</span><span class="sxs-lookup"><span data-stu-id="3cbf1-138">Tester</span></span>  <br/> |
|<span data-ttu-id="3cbf1-139">Status do sinalizador</span><span class="sxs-lookup"><span data-stu-id="3cbf1-139">Flag Status</span></span>  <br/> |<span data-ttu-id="3cbf1-140">SINALIZAR</span><span class="sxs-lookup"><span data-stu-id="3cbf1-140">FLAG</span></span>  <br/> |<span data-ttu-id="3cbf1-141">Tarefa</span><span class="sxs-lookup"><span data-stu-id="3cbf1-141">Task</span></span>  <br/> |<span data-ttu-id="3cbf1-142">Não</span><span class="sxs-lookup"><span data-stu-id="3cbf1-142">No</span></span>  <br/> |
|<span data-ttu-id="3cbf1-143">Integridade</span><span class="sxs-lookup"><span data-stu-id="3cbf1-143">Health</span></span>  <br/> |<span data-ttu-id="3cbf1-144">TEXTO</span><span class="sxs-lookup"><span data-stu-id="3cbf1-144">TEXT</span></span>  <br/> |<span data-ttu-id="3cbf1-145">Tarefa</span><span class="sxs-lookup"><span data-stu-id="3cbf1-145">Task</span></span>  <br/> |<span data-ttu-id="3cbf1-146">Não especificado</span><span class="sxs-lookup"><span data-stu-id="3cbf1-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="3cbf1-147">Os ECFs são definidos na instância externa do Project Web Application (PWA), de qualquer projeto, recurso ou tarefa.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="3cbf1-148">No entanto, eles podem se associar a um projeto, recurso ou tarefa.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="3cbf1-149">Este artigo fornece uma visão introdutória dos campos personalizados usando um aplicativo de exemplo e se concentra na recuperação de valores do ECF.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="3cbf1-150">É possível baixar o exemplo completo em https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-150">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="3cbf1-151">Além disso, o Project Online é compatível com campos personalizados locais como entidades somente leitura específicas para o projeto, recursos ou tarefa específico.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="3cbf1-152">Para saber mais sobre campos personalizados locais, confira o exemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="3cbf1-153">Materiais de tela de fundo</span><span class="sxs-lookup"><span data-stu-id="3cbf1-153">Background materials</span></span>

<span data-ttu-id="3cbf1-154">Um artigo anterior, [Desenvolver um aplicativo do Project Online usando o modelo de objeto do lado do cliente](developing-a-project-online-application-using-the-client-side-object-model.md), fornece o plano de fundo e a orientação inicial para o desenvolvimento de aplicativos usando o CSOM.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="3cbf1-155">Confira este artigo para ver os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="3cbf1-156">Informações sobre o Project, edições autônomas e baseadas na nuvem</span><span class="sxs-lookup"><span data-stu-id="3cbf1-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="3cbf1-157">Ambiente de desenvolvimento (edições do Visual Studio e bibliotecas de software)</span><span class="sxs-lookup"><span data-stu-id="3cbf1-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="3cbf1-158">Instalação do projeto do Visual Studio para um aplicativo .NET usando a biblioteca CSOM</span><span class="sxs-lookup"><span data-stu-id="3cbf1-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="3cbf1-159">Conexão com o serviço do Project Online</span><span class="sxs-lookup"><span data-stu-id="3cbf1-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="3cbf1-160">Preliminares (declarações de nível de classe)</span><span class="sxs-lookup"><span data-stu-id="3cbf1-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="3cbf1-161">A classe deste aplicativo define dois itens de dados: o contexto do projeto e o dicionário pwaECF.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="3cbf1-162">O objeto do contexto do projeto faz parte do CSOM Project e conecta instância PWA e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="3cbf1-163">Todas as solicitações do serviço usam o contexto do projeto.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="3cbf1-164">O contexto precisa do ponto de extremidade de conexão para criar uma instância em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="3cbf1-165">O ponto de extremidade de conexão é a URL de sua instância do PWA.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="3cbf1-166">O dicionário pwaECF armazena os EFCs do projeto definidos no nível do PWA.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="3cbf1-167">O dicionário usa o ECF.InternalName como a chave e o objeto CustomField como o valor.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="3cbf1-168">O dicionário é preenchido no método ListPWACustomFields e, em seguida, é usado como uma referência no método Main.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="3cbf1-169">Método Main</span><span class="sxs-lookup"><span data-stu-id="3cbf1-169">Main method</span></span>

<span data-ttu-id="3cbf1-170">O método Main gerencia o fluxo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-170">The Main method manages the application flow.</span></span> <span data-ttu-id="3cbf1-171">Assim como em outros aplicativos que usam o CSOM do Project Online, o Main inicializa o contexto do projeto.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="3cbf1-172">Recupere e liste os ECFs no PWA do Project Online.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="3cbf1-173">Esse recurso é implementado no método ListPWACustomFields.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="3cbf1-174">Recupere projetos com campos personalizados e campos não personalizados.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="3cbf1-175">Ao recuperar projetos com ECFs, a solicitação de consulta feita ao serviço do Project Online deve incluir os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="3cbf1-176">**IncludeCustomFields** &ndash; Este item solicita que o serviço retorne uma coleção de PublishedProjects, em que cada projeto publicado inclui uma extensão que oferece suporte a campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="3cbf1-177">A menos que este item seja especificado, o Project Online retorna objetos PublishedProject que não incluem dados do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="3cbf1-178">**IncludeCustomFields.CustomFields** &ndash; Este item solicita que o serviço preencha os objetos PublishedProject com dados de CustomFields.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="3cbf1-179">A solicitação a seguir especifica a ID e o nome do projeto, além da extensão do objeto para campos personalizados e os valores do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="3cbf1-180">Examine cada projeto.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-180">Examine each project.</span></span>
    
   <span data-ttu-id="3cbf1-181">Os objetos de projeto usados neste aplicativo são do tipo PublishedProject porque os valores são recuperados e exibidos.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="3cbf1-182">Se você precisar atualizar valores de dados em um ou mais projetos, o projeto que está passando pela atualização passará por check-out e o aplicativo utilizará um objeto DraftProject para recuperar os valores e atualizar o projeto.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="3cbf1-183">Acessar as entradas ECF para um projeto</span><span class="sxs-lookup"><span data-stu-id="3cbf1-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="3cbf1-184">Cada instância do ECF separa o valor do campo do restante das informações do ECF.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="3cbf1-185">O valor do campo é armazenado como parte de um par de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="3cbf1-186">O restante das informações é armazenado em um objeto CustomField.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="3cbf1-187">O acesso a valores do ECF em um projeto consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="3cbf1-188">Passar pela coleção CustomFields</span><span class="sxs-lookup"><span data-stu-id="3cbf1-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="3cbf1-189">Acessar a entrada adequada usando duas construções.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="3cbf1-190">Cada projeto armazena entradas do ECF associadas em dois locais, uma coleção CustomFields que é enumerável e os valores do campo como parte de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="3cbf1-191">Em pares de chave/valor, o internalName é a chave e o valor do campo é o valor.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="3cbf1-192">Use um dicionário para armazenar e acessar os valores do campo.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="3cbf1-193">As propriedades do ECF, além dos valores de campo, são armazenadas em objetos CustomField, um objeto por projeto.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="3cbf1-194">Use uma coleção CustomFields para acessar os ECFs associados a um projeto individual.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="3cbf1-195">Cada projeto armazena os ECFs associados em uma coleção na qual cada entrada do ECF é formada por uma chave, o nome interno do ECF, e um objeto que contém o valor do ECF.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="3cbf1-196">Transfira a coleção para um dicionário para acessar entradas individuais.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="3cbf1-197">A declaração seguirá a transferência.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="3cbf1-198">O valor em uma entrada de dicionário corresponde ao tipo de dados do ECF.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="3cbf1-199">O objeto para cada ECF é mapeado para um dos vários tipos.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="3cbf1-200">A maioria dos ECFs usa tipos simples que se encaixam em variáveis padrão.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="3cbf1-201">O fragmento a seguir mostra que o processamento mínimo está envolvido em vários tipos:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
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

   <span data-ttu-id="3cbf1-202">A tabela de pesquisa de valores de TEXTO, no entanto, requer processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="3cbf1-203">O aplicativo recupera a tabela de consulta apropriada do serviço e gera a instância do ECF (com valores únicos ou múltiplos) percorrendo a tabela de consulta.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="3cbf1-204">O fragmento de código a seguir mostra o processamento de ECFs de TEXTO, incluindo aqueles com valores simples e aqueles que usam tabelas de consulta:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
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

   <span data-ttu-id="3cbf1-205">Este aplicativo simplesmente mostra os valores. No entanto, é possível obter mais significado nos valores de dados.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="3cbf1-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="3cbf1-206">ListPWACustomFields</span></span>

<span data-ttu-id="3cbf1-207">O método ListPWACustomFields recupera e lista ECFs associados a projetos.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="3cbf1-208">Esse método lista ECFs registrados na instância PWA que pode ser associada a projetos individuais.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="3cbf1-209">O ponto de entrada para acessar os ECFs usa o elemento CustomFields do contexto do projeto, como na solicitação de consulta a seguir:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="3cbf1-210">O método não verifica se um projeto usa um ECF específico.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3cbf1-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cbf1-211">See also</span></span>

- [<span data-ttu-id="3cbf1-212">Plataforma de desenvolvimento do Project</span><span class="sxs-lookup"><span data-stu-id="3cbf1-212">Project Development Portal</span></span>](https://developer.microsoft.com/pt-BR/project)
- <span data-ttu-id="3cbf1-213">
  [Visão geral: campos personalizados empresariais e tabelas de pesquisa](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)</span><span class="sxs-lookup"><span data-stu-id="3cbf1-213">[Overview: Enterprise custom fields and lookup tables](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)</span></span>
- <span data-ttu-id="3cbf1-214">[Campos personalizados empresariais e locais](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="3cbf1-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="3cbf1-215">Adicionar ou editar campos personalizados empresariais no Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="3cbf1-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

