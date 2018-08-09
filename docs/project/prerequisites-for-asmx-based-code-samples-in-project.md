---
title: Pré-requisitos para amostras de código com base em ASMX no projeto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- amostras de código, o servidor de projeto, Project Server, programação, PSI, amostras de código, PSI, de compilação de programação
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Saiba mais informações para ajudá-lo a criar projetos no Visual Studio usando as amostras de código com base em ASMX que estão incluídas nos tópicos de referência do Project Server Interface (PSI).
ms.openlocfilehash: 73d097211dc3c68e1066c2ea1ad8d51a616184d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771181"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="ccdee-104">Pré-requisitos para amostras de código com base em ASMX no projeto</span><span class="sxs-lookup"><span data-stu-id="ccdee-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="ccdee-105">Saiba mais informações para ajudá-lo a criar projetos no Visual Studio usando as amostras de código com base em ASMX que estão incluídas nos tópicos de referência do Project Server Interface (PSI).</span><span class="sxs-lookup"><span data-stu-id="ccdee-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="ccdee-106">Muitos dos exemplos de código incluídos na [referência do serviço de web e de biblioteca de classe do Project Server 2013](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) foram criados para o Office Project 2007 SDK e usam um formato padrão para serviços web ASMX.</span><span class="sxs-lookup"><span data-stu-id="ccdee-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="ccdee-107">As amostras ainda funcionam no Project Server 2013 e são projetadas para serem copiados para um aplicativo de console e executados como uma unidade completa.</span><span class="sxs-lookup"><span data-stu-id="ccdee-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="ccdee-108">Exceções são observadas na amostra.</span><span class="sxs-lookup"><span data-stu-id="ccdee-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="ccdee-109">Novos exemplos PSI no Project 2013 SDK seguem um formato que usa os serviços do Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="ccdee-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="ccdee-110">As amostras com base em ASMX também podem ser adaptadas para usar os serviços WCF.</span><span class="sxs-lookup"><span data-stu-id="ccdee-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="ccdee-111">Este artigo mostra como usar as amostras com serviços web ASMX.</span><span class="sxs-lookup"><span data-stu-id="ccdee-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="ccdee-112">Para obter informações sobre como usar as amostras com os serviços WCF, consulte [pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="ccdee-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ccdee-113">A interface de serviço web ASMX de PSI foi preterido no Project Server 2013, mas ainda é suportado.</span><span class="sxs-lookup"><span data-stu-id="ccdee-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="ccdee-114">Se o modelo de objeto do cliente (CSOM) inclui os métodos que seu aplicativo requer, novos aplicativos devem ser desenvolvidos com o CSOM.</span><span class="sxs-lookup"><span data-stu-id="ccdee-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="ccdee-115">O CSOM permite que os aplicativos funcionar com o Project Online ou em uma instalação local do Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="ccdee-116">Caso contrário, se o aplicativo usa a PSI, ele deve usar a interface WCF, que é a tecnologia que a Microsoft recomenda para comunicações de rede.</span><span class="sxs-lookup"><span data-stu-id="ccdee-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="ccdee-117">Aplicativos que usam a interface ASMX ou a interface WCF podem trabalhar somente para instalações locais do Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="ccdee-118">Para obter mais informações sobre o CSOM, consulte [arquitetura do Project Server 2013](project-server-2013-architecture.md) e [o modelo de objeto do lado do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="ccdee-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="ccdee-119">Antes de executar os exemplos de código, você deve configurar o ambiente de desenvolvimento, configure o aplicativo e alterar valores de constantes genéricos para coincidir com o seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="ccdee-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="ccdee-120">Configurar o ambiente de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="ccdee-120">Setting up the development environment</span></span>
<span data-ttu-id="ccdee-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-121"></span></span>

1. <span data-ttu-id="ccdee-122">**Configurar um teste de sistema do Project Server**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="ccdee-123">Use um teste de sistema do Project Server sempre que você estiver desenvolvendo ou teste.</span><span class="sxs-lookup"><span data-stu-id="ccdee-123">Use a test Project Server system whenever you are developing or testing.</span></span> <span data-ttu-id="ccdee-124">Mesmo quando seu código funciona perfeitamente, dependências interproject, relatórios ou outros fatores ambientais podem causar consequências indesejadas.</span><span class="sxs-lookup"><span data-stu-id="ccdee-124">Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="ccdee-125">Certifique-se de que você é um usuário válido no servidor e verifique se você tem permissões suficientes para as chamadas PSI que usa seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ccdee-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="ccdee-126">O tópico de referência para cada método PSI inclui uma tabela de permissões do Project Server.</span><span class="sxs-lookup"><span data-stu-id="ccdee-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="ccdee-127">Por exemplo, o método [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requer a permissão **NewProject** global e a permissão de **SaveProjectTemplate** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="ccdee-128">Em alguns casos, você pode precisar fazer a depuração remota no servidor.</span><span class="sxs-lookup"><span data-stu-id="ccdee-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="ccdee-129">Você também pode ter que configurar um manipulador de eventos instalando um assembly do manipulador de eventos em cada computador do Project Server no farm do SharePoint e, em seguida, configurando o manipulador de eventos para a instância do Project Web App usando a página de configurações do Project Server em geral Configurações de aplicativos da Administração Central do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ccdee-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="ccdee-130">**Configure um computador de desenvolvimento.**</span><span class="sxs-lookup"><span data-stu-id="ccdee-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="ccdee-131">Você geralmente pode acessar a PSI através de uma rede.</span><span class="sxs-lookup"><span data-stu-id="ccdee-131">You usually access the PSI through a network.</span></span> <span data-ttu-id="ccdee-132">Os exemplos de código são projetados para ser executado em um cliente separado do servidor, exceto onde observado.</span><span class="sxs-lookup"><span data-stu-id="ccdee-132">The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="ccdee-133">**Instale a versão correta do Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="ccdee-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="ccdee-134">Exceto quando observado, as amostras de código são escritas em Visual c#.</span><span class="sxs-lookup"><span data-stu-id="ccdee-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="ccdee-135">Eles podem ser usados com o Visual Studio 2010 ou Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="ccdee-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="ccdee-136">Certifique-se de que você tenha o service pack mais recente instalado.</span><span class="sxs-lookup"><span data-stu-id="ccdee-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="ccdee-137">**Copie DLLs do Project Server no computador de desenvolvimento.**</span><span class="sxs-lookup"><span data-stu-id="ccdee-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="ccdee-138">Copie os seguintes assemblies de `[Program Files]\Microsoft Office Servers\15.0\Bin` no computador do Project Server no computador de desenvolvimento:</span><span class="sxs-lookup"><span data-stu-id="ccdee-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="ccdee-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="ccdee-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="ccdee-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="ccdee-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="ccdee-141">Para obter informações sobre como compilar e usar o assembly de proxy ProjectServerServices.dll para os serviços da web ASMX na PSI, consulte [usando um assembly de proxy PSI e descrições de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="ccdee-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="ccdee-142">**Instale os arquivos IntelliSense.**</span><span class="sxs-lookup"><span data-stu-id="ccdee-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="ccdee-143">Para usar o IntelliSense descrições para classes e membros em assemblies do Project Server, copiar os arquivos XML IntelliSense atualizados do Project 2013 SDK baixar para o mesmo diretório onde os assemblies do Project Server estão localizados.</span><span class="sxs-lookup"><span data-stu-id="ccdee-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="ccdee-144">Por exemplo, copie o arquivo de Microsoft.Office.Project.Server.Library.xml para o diretório onde o seu aplicativo será definida uma referência para o assembly Microsoft.Office.Project.Server.Library.dll.</span><span class="sxs-lookup"><span data-stu-id="ccdee-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="ccdee-145">Descrições de IntelliSense para os serviços da web PSI exigem que você crie um assembly de proxy PSI usando o script CompileASMXProxyAssembly.cmd a `Documentation\IntelliSense\WSDL` subdiretório no download do SDK do Project 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="ccdee-146">O script cria o assembly de proxy com base em ASMX ProjectServerServices.dll.</span><span class="sxs-lookup"><span data-stu-id="ccdee-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="ccdee-147">Para obter mais informações, consulte o arquivo de [ReadMe_IntelliSense] no download do SDK.</span><span class="sxs-lookup"><span data-stu-id="ccdee-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="ccdee-148">Criando o aplicativo e adicionando uma referência ao serviço web</span><span class="sxs-lookup"><span data-stu-id="ccdee-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="ccdee-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-149"></span></span>

1. <span data-ttu-id="ccdee-150">**Criar um aplicativo de console**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="ccdee-151">Quando você cria um aplicativo de console, na lista suspensa da caixa de diálogo **Novo projeto** , selecione o **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-151">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**.</span></span> <span data-ttu-id="ccdee-152">Você pode copiar o código de exemplo PSI para o novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ccdee-152">You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="ccdee-153">**Adicione a referência necessária para ASMX.**</span><span class="sxs-lookup"><span data-stu-id="ccdee-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="ccdee-154">No Solution Explorer, adicione uma referência ao **System.Web.Services** (consulte a Figura 1).</span><span class="sxs-lookup"><span data-stu-id="ccdee-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="ccdee-155">**Figura 1. Adicionando uma referência no Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="ccdee-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="ccdee-156">![Adicionando uma referência no Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Adicionando uma referência no Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="ccdee-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="ccdee-157">**Copie o código**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="ccdee-158">Copie o exemplo de código completo para o arquivo de Module. vb do aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="ccdee-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="ccdee-159">**Definir o namespace para o aplicativo de amostra**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="ccdee-160">Você pode alterar o namespace listado na parte superior da amostra para o namespace padrão de aplicativo, ou alterar o namespace do aplicativo padrão para corresponder a amostra.</span><span class="sxs-lookup"><span data-stu-id="ccdee-160">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample.</span></span> <span data-ttu-id="ccdee-161">Você pode alterar o namespace do aplicativo padrão, alterando as propriedades do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ccdee-161">You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="ccdee-162">Por exemplo, o exemplo de código para [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) tem o namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="ccdee-163">Se o nome do projeto do Visual Studio for **RenameProject**, copie o namespace do arquivo Module. vb e abra o painel de **Propriedades** do projeto (no menu **projeto** , escolha **Propriedades RenameProject**).</span><span class="sxs-lookup"><span data-stu-id="ccdee-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="ccdee-164">Na guia **aplicativo** , copie o namespace na caixa de texto **namespace padrão** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="ccdee-165">**Defina as referências da web**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="ccdee-166">A maioria dos exemplos requerem uma referência a um ou mais dos serviços da web PSI.</span><span class="sxs-lookup"><span data-stu-id="ccdee-166">Most examples require a reference to one or more of the PSI web services.</span></span> <span data-ttu-id="ccdee-167">Eles são listados na amostra de si mesmo ou em comentários que precedem a amostra.</span><span class="sxs-lookup"><span data-stu-id="ccdee-167">These are listed in the sample itself or in comments that precede the sample.</span></span> <span data-ttu-id="ccdee-168">Para obter o namespace correto de referências web, certifique-se de que, primeiro, você definir o namespace do aplicativo padrão.</span><span class="sxs-lookup"><span data-stu-id="ccdee-168">To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="ccdee-169">Há três maneiras de adicionar uma referência ao serviço web ASMX para a PSI:</span><span class="sxs-lookup"><span data-stu-id="ccdee-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="ccdee-170">Crie um conjunto de proxy PSI denominado ProjectServerServices.dll e, em seguida, defina uma referência para o assembly.</span><span class="sxs-lookup"><span data-stu-id="ccdee-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="ccdee-171">Para obter o IntelliSense, esta é a maneira recomendada para adicionar uma referência PSI.</span><span class="sxs-lookup"><span data-stu-id="ccdee-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="ccdee-172">Consulte [usando um assembly de proxy PSI e descrições de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="ccdee-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="ccdee-173">Adicione um arquivo de proxy de saída wsdl.exe e a solução do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ccdee-173">Add a proxy file from the wsdl.exe output to the Visual Studio solution.</span></span> <span data-ttu-id="ccdee-174">Consulte [Adicionando um arquivo de proxy PSI](#pj15_PrerequisitesASMX_AddingProxyFile).</span><span class="sxs-lookup"><span data-stu-id="ccdee-174">See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="ccdee-175">Adicione uma referência de serviço da web usando o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ccdee-175">Add a web service reference by using Visual Studio.</span></span> <span data-ttu-id="ccdee-176">Consulte a [referência de serviço de adição de uma web](#pj15_PrerequisitesASMX_AddingServiceReference).</span><span class="sxs-lookup"><span data-stu-id="ccdee-176">See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="ccdee-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-177"></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="ccdee-178">Usando um assembly de proxy PSI e descrições de IntelliSense</span><span class="sxs-lookup"><span data-stu-id="ccdee-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="ccdee-179">É possível criar e usar o assembly de proxy ProjectServerServices.dll para todos os serviços da web baseados em ASMX no PSI, usando o script CompileASMXProxyAssembly.cmd a `Documentation\IntelliSense\WSDL` pasta do download do SDK do Project 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="ccdee-180">Para um link para o download, consulte a [documentação do desenvolvedor do Project 2013](project-2013-developer-documentation.md).</span><span class="sxs-lookup"><span data-stu-id="ccdee-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ccdee-181">Quando você extrair os arquivos de origem do proxy do Source.zip de arquivo, os arquivos no `Documentation\IntelliSense\WSDL\Source` pasta são atuais a partir da data de publicação do download do SDK do Project 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="ccdee-182">Para gerar atualizado arquivos de origem do proxy PSI, executados o script de GenASMXProxyAssembly.cmd no computador do Project Server.</span><span class="sxs-lookup"><span data-stu-id="ccdee-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="ccdee-183">Os scripts no `Documentation\IntelliSense\WCF` pasta não funcionam para aplicativos baseados em ASMX.</span><span class="sxs-lookup"><span data-stu-id="ccdee-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="ccdee-184">O script GenWCFProxyAssembly.cmd chama SvcUtil.exe, que gera arquivos código-fonte para os serviços WCF.</span><span class="sxs-lookup"><span data-stu-id="ccdee-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="ccdee-185">Os arquivos de proxy WCF incluem atributos diferentes, a interface de canal e uma classe de cliente para cada serviço PSI.</span><span class="sxs-lookup"><span data-stu-id="ccdee-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="ccdee-186">Por exemplo, o serviço de recursos com base em WCF inclui a interface **ResourceChannel** , a interface de **recurso** e a classe **ResourceClient** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="ccdee-187">Web com base em ASMX recurso inclui a classe de **recurso** com algumas propriedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="ccdee-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="ccdee-188">A seguir é o script de GenASMXProxyAssembly.cmd que gera arquivos de saída WSDL para os serviços da web PSI e, em seguida, compila o assembly.</span><span class="sxs-lookup"><span data-stu-id="ccdee-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=http://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

<span data-ttu-id="ccdee-189">O script usa o arquivo de ClassList_asmx.txt, que contém a lista dos serviços da web que estão disponíveis para os desenvolvedores de terceiros.</span><span class="sxs-lookup"><span data-stu-id="ccdee-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

<span data-ttu-id="ccdee-190">Os scripts criam um assembly denominado ProjectServerServices.dll.</span><span class="sxs-lookup"><span data-stu-id="ccdee-190">The scripts create an assembly named ProjectServerServices.dll.</span></span> <span data-ttu-id="ccdee-191">Evite confusa-lo com ProjectServerServices.dll para o assembly com base em WCF.</span><span class="sxs-lookup"><span data-stu-id="ccdee-191">Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly.</span></span> <span data-ttu-id="ccdee-192">Os nomes de assembly são os mesmos, para habilitar usando qualquer um dos assembly com o arquivo ProjectServerServices.xml IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="ccdee-192">The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="ccdee-193">O namespace arbitrário criado pelos scripts para os serviços WCF e os serviços da web ASMX é o mesmo, para que o arquivo de ProjectServerServices.xml IntelliSense funciona com qualquer assembly.</span><span class="sxs-lookup"><span data-stu-id="ccdee-193">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly.</span></span> <span data-ttu-id="ccdee-194">Por exemplo, o namespace do serviço de recurso no assembly proxy com base em WCF e no assembly com base em ASMX proxy é **SvcResource**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-194">For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**.</span></span> <span data-ttu-id="ccdee-195">Obviamente, você pode alterar os nomes de namespace — se você garantir que elas correspondam no assembly proxy e no arquivo ProjectServerServices.xml IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="ccdee-195">You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="ccdee-196">Se um exemplo de código usa um nome diferente para um namespace de serviço da web PSI, por exemplo **ProjectWebSvc**, para o IntelliSense funcione, você deve alterar a amostra para usar **SvcProject** para que o namespace corresponde o assembly de proxy.</span><span class="sxs-lookup"><span data-stu-id="ccdee-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="ccdee-197">Uma vantagem de usar o assembly de proxy com base em ASMX é que ele inclua todos os namespaces de serviço de web PSI; Você não precisará criar várias referências da web.</span><span class="sxs-lookup"><span data-stu-id="ccdee-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="ccdee-198">Outra vantagem é que, se você adicionar o arquivo ProjectServerServices.xml no mesmo diretório onde você pode definir uma referência para o assembly de proxy ProjectServerServices.dll, você pode obter o IntelliSense descrições para as classes PSI e membros.</span><span class="sxs-lookup"><span data-stu-id="ccdee-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="ccdee-199">A Figura 2 mostra o texto do IntelliSense para o método **Project.QueueCreateProject** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="ccdee-200">Para obter mais informações, consulte o arquivo de [ReadMe_IntelliSense] na pasta IntelliSense do download do SDK do Project 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="ccdee-201">**Figura 2. Usando o IntelliSense para um método no serviço da web de projeto**</span><span class="sxs-lookup"><span data-stu-id="ccdee-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="ccdee-202">![Usando o Intellisense para um método em um serviço PSI] (media/pj15_PrerequisitesASMX_Intellisense.gif "Usando o Intellisense para um método em um serviço PSI")</span><span class="sxs-lookup"><span data-stu-id="ccdee-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="ccdee-203">Desvantagens de usar o assembly de proxy são que a solução é maior e você deve distribuir e instalar o assembly do proxy com a solução.</span><span class="sxs-lookup"><span data-stu-id="ccdee-203">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution.</span></span> <span data-ttu-id="ccdee-204">Você também deve usar os mesmos namespaces que estão no assembly de proxy e arquivos IntelliSense, a menos que você altere o script e arquivos ProjectServerServices.xml IntelliSense usar espaços para nome diferentes.</span><span class="sxs-lookup"><span data-stu-id="ccdee-204">You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="ccdee-205">Adicionando um arquivo de proxy PSI</span><span class="sxs-lookup"><span data-stu-id="ccdee-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="ccdee-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-206"></span></span>

<span data-ttu-id="ccdee-207">O download do SDK do Project 2013 inclui os arquivos de origem gerados pelo comando Wsdl.exe para o assembly de proxy.</span><span class="sxs-lookup"><span data-stu-id="ccdee-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="ccdee-208">Os arquivos de origem estão em Source.zip no `Documentation\IntelliSense\ASMX` subdiretório.</span><span class="sxs-lookup"><span data-stu-id="ccdee-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="ccdee-209">Em vez de definir uma referência para o assembly de proxy, você pode adicionar um ou mais dos arquivos de origem para uma solução do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ccdee-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="ccdee-210">Por exemplo, depois de executar o script GenASMXProxyAssembly.cmd, adicione o wsdl. Arquivo Project.cs à solução.</span><span class="sxs-lookup"><span data-stu-id="ccdee-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="ccdee-211">Em vez de executar o script, você pode executar os seguintes comandos para gerar um arquivo de origem único, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ccdee-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=http://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="ccdee-212">Para definir um objeto **Project** como uma variável de classe denominada **project**, use o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccdee-212">To define a **Project** object as a class variable named **project**, use the following code.</span></span> <span data-ttu-id="ccdee-213">O método **AddContextInfo** adiciona as informações de contexto para o objeto de **projeto** para a autenticação do Windows e autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="ccdee-213">The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "http://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> <span data-ttu-id="ccdee-214">Se você usar um assembly de proxy PSI ou adiciona um arquivo de proxy para obter uma referência de serviço do projeto chamado **SvcProject**, você usaria o mesmo código para criar um objeto **project** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="ccdee-215">Adicionando uma referência ao serviço web</span><span class="sxs-lookup"><span data-stu-id="ccdee-215">Adding a web service reference</span></span>
<span data-ttu-id="ccdee-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-216"></span></span>

<span data-ttu-id="ccdee-217">Se você não usar o assembly de proxy com base em ASMX ou adicionar um arquivo de saída WSDL, você pode definir uma ou mais referências de web individuais.</span><span class="sxs-lookup"><span data-stu-id="ccdee-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="ccdee-218">As etapas a seguir mostram como definir uma referência da web usando o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="ccdee-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="ccdee-219">No **Solution Explorer**, clique com botão direito na pasta **referências** e escolha **Adicionar referência de serviço**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="ccdee-220">Na caixa de diálogo **Adicionar referência de serviço** , escolha **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="ccdee-221">Na caixa de diálogo **Configurações de referência do serviço** , escolha **Adicionar referência da Web**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="ccdee-222">Na caixa de texto **URL** , digite `http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`e pressione **Enter** ou escolha o ícone **Ir** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-222">In the **URL** text box, type `http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="ccdee-223">Se você tiver instalado Secure Sockets Layer (SSL), você deve usar o protocolo HTTPS, em vez do protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="ccdee-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="ccdee-224">Por exemplo, use a seguinte URL para o serviço de projeto no `http://MyServer/pwa` site do Project Web App:`http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="ccdee-224">For example, use the following URL for the Project service on the  `http://MyServer/pwa` site for Project Web App: `http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="ccdee-225">Ou, abra o navegador da web e navegue até `http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span><span class="sxs-lookup"><span data-stu-id="ccdee-225">Or, open your web browser, and navigate to `http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="ccdee-226">Salve o arquivo em um diretório local, como `C:\Project\WebServices\ServiceName.wsdl`.</span><span class="sxs-lookup"><span data-stu-id="ccdee-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="ccdee-227">Na caixa de diálogo **Adicionar referência da Web** , de **URL**, digite o protocolo de arquivo e o caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ccdee-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="ccdee-228">Por exemplo, digite `file://C:\Project\WebServices\Project.wsdl`.</span><span class="sxs-lookup"><span data-stu-id="ccdee-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="ccdee-229">Depois que a referência resolve, digite o nome de referência na caixa de texto **nome de referência da Web** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="ccdee-230">Exemplos de código na documentação do desenvolvedor do Project 2013 usam o nome de referência padrão arbitrário **Svc _ServiceName_**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="ccdee-231">Por exemplo, o serviço web de projeto é denominado **SvcProject** (consulte a Figura 3).</span><span class="sxs-lookup"><span data-stu-id="ccdee-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="ccdee-232">**Figura 3. Adicionando uma referência ao serviço web ASMX**</span><span class="sxs-lookup"><span data-stu-id="ccdee-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="ccdee-233">![Adicionando uma referência ao serviço web ASMX] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adicionando uma referência ao serviço web ASMX")</span><span class="sxs-lookup"><span data-stu-id="ccdee-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="ccdee-234">Para componentes de aplicativo que devem ser executado em um computador do Project Server, utilizam a representação, ou ter permissões elevadas, use uma referência de serviço WCF em vez de uma referência de web ASMX.</span><span class="sxs-lookup"><span data-stu-id="ccdee-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="ccdee-235">Para obter mais informações, consulte [pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="ccdee-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="ccdee-236">A definição de outras referências</span><span class="sxs-lookup"><span data-stu-id="ccdee-236">Setting other references</span></span>
<span data-ttu-id="ccdee-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-237"></span></span>

<span data-ttu-id="ccdee-238">Aplicativos do Project Server frequentemente usam outros serviços, como serviços web do SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="ccdee-239">Se outros serviços são necessários, eles são mencionados no exemplo.</span><span class="sxs-lookup"><span data-stu-id="ccdee-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="ccdee-240">Referências locais para o exemplo de código são listadas instruções **using** na parte superior da amostra:</span><span class="sxs-lookup"><span data-stu-id="ccdee-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="ccdee-241">No **Solution Explorer**, clique com botão direito na pasta **referências** e escolha **Adicionar referência**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="ccdee-242">Escolha **Procurar**e navegue até o local onde você armazenou DLLs do servidor do projeto que você copiou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ccdee-242">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously.</span></span> <span data-ttu-id="ccdee-243">Escolha as DLLs, você precisa e escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-243">Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ccdee-244">Certifique-se de que as versões de montagem no computador de desenvolvimento correspondem exatamente aqueles no computador do Project Server de destino.</span><span class="sxs-lookup"><span data-stu-id="ccdee-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="ccdee-245">Usando a autenticação de vários</span><span class="sxs-lookup"><span data-stu-id="ccdee-245">Using multiple authentication</span></span>
<span data-ttu-id="ccdee-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-246"></span></span>

<span data-ttu-id="ccdee-247">Autenticação de usuários do Project Server no local, pela autenticação do Windows ou a autenticação de formulários, é feita por meio de declarações de processamento no SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ccdee-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="ccdee-248">Autenticação de vários significa que o aplicativo web no qual o Project Web App é provisionado suporta a autenticação do Windows e autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="ccdee-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="ccdee-249">Se for esse o caso, uma chamada para um serviço web ASMX que usa a autenticação do Windows irá falhar com o seguinte erro, porque o processo de declarações não consegue determinar qual tipo de usuário para autenticar:</span><span class="sxs-lookup"><span data-stu-id="ccdee-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="ccdee-250">Para corrigir o problema para ASMX, todas as chamadas para os métodos PSI devem ser uma classe derivada que é definida para cada serviço da web PSI.</span><span class="sxs-lookup"><span data-stu-id="ccdee-250">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service.</span></span> <span data-ttu-id="ccdee-251">A classe derivada também deve usar a classe **SvcLoginWindows.LoginWindows** para obter um cookie para a classe de serviço PSI derivada.</span><span class="sxs-lookup"><span data-stu-id="ccdee-251">The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class.</span></span> <span data-ttu-id="ccdee-252">No exemplo a seguir, a classe **ProjectDerived** derivada da classe **SvcProject.Project** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-252">In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class.</span></span> <span data-ttu-id="ccdee-253">A classe derivada adiciona a propriedade **EnforceWindowsAuth** e substitui o cabeçalho de solicitação da web para cada chamada a um método na classe **Project** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-253">The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class.</span></span> <span data-ttu-id="ccdee-254">Se a propriedade **EnforceWindowsAuth** for **true**, o método **GetWebRequest** adiciona um cabeçalho que desabilita a autenticação de formulários.</span><span class="sxs-lookup"><span data-stu-id="ccdee-254">If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication.</span></span> <span data-ttu-id="ccdee-255">Se **EnforceWindowsAuth** for **false**, a autenticação de formulários possa continuar.</span><span class="sxs-lookup"><span data-stu-id="ccdee-255">If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="ccdee-256">Para usar o exemplo a seguir **ASMXLogon_MultiAuth** , crie um aplicativo de console, siga as etapas em [criar o aplicativo e adicionar uma referência ao serviço web](#pj15_PrerequisitesASMX_Configure)e, em seguida, adicione o wsdl. Arquivo de proxy LoginWindows.cs e o wsdl. Arquivo de proxy Project.cs.</span><span class="sxs-lookup"><span data-stu-id="ccdee-256">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file.</span></span> <span data-ttu-id="ccdee-257">O método **Main** cria a instância da classe **ProjectDerived** do **projeto** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-257">The **Main** method creates the **project** instance of the **ProjectDerived** class.</span></span> <span data-ttu-id="ccdee-258">A amostra deve usar a classe derivada de **LoginWindowsDerived** para obter um objeto **CookieContainer** para o projeto **. CookieContainer** propriedade, que distingue a autenticação de formulários de autenticação do Windows.</span><span class="sxs-lookup"><span data-stu-id="ccdee-258">The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication.</span></span> <span data-ttu-id="ccdee-259">O objeto de **projeto** pode ser usado para fazer chamadas para qualquer método na classe **SvcProject.Project** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-259">The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ccdee-260">O serviço de **LoginWindows** é necessário somente para aplicativos ASMX em um ambiente de autenticação múltiplos.</span><span class="sxs-lookup"><span data-stu-id="ccdee-260">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment.</span></span> <span data-ttu-id="ccdee-261">No exemplo **ASMXLogon_MultiAuth** , o método **GetLogonCookie** obtém um cookie para o objeto **loginWindows** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-261">In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object.</span></span> <span data-ttu-id="ccdee-262">O projeto **. CookieContainer** propriedade estiver definida como o valor de **loginWindows.CookieContainer** .</span><span class="sxs-lookup"><span data-stu-id="ccdee-262">The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "http://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

<span data-ttu-id="ccdee-263">Usando a classe derivada de **LoginWindows** e fazer chamadas PSI com um cabeçalho de solicitação da web que desabilita a autenticação de formulários, são necessário para aplicativos que são executados em um ambiente de autenticação múltiplos.</span><span class="sxs-lookup"><span data-stu-id="ccdee-263">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment.</span></span> <span data-ttu-id="ccdee-264">Se o Project Server usa apenas a autenticação de declarações, não é necessário derivar de uma classe que adiciona um cabeçalho de solicitação da web.</span><span class="sxs-lookup"><span data-stu-id="ccdee-264">If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header.</span></span> <span data-ttu-id="ccdee-265">O exemplo anterior é executado em ambos os ambientes.</span><span class="sxs-lookup"><span data-stu-id="ccdee-265">The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="ccdee-266">A correção para um aplicativo baseado em WCF é diferente.</span><span class="sxs-lookup"><span data-stu-id="ccdee-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="ccdee-267">Para obter mais informações, consulte a seção *usando a autenticação de vários* [pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="ccdee-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="ccdee-268">Alterando os valores das constantes genéricos</span><span class="sxs-lookup"><span data-stu-id="ccdee-268">Changing the values of generic constants</span></span>
<span data-ttu-id="ccdee-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-269"></span></span>

<span data-ttu-id="ccdee-270">A maioria das amostras têm uma ou mais variáveis que precisam ser atualizados para o exemplo funcione corretamente no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="ccdee-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="ccdee-271">No exemplo a seguir, se você tiver SSL instalado, use o protocolo HTTPS, em vez do protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="ccdee-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="ccdee-272">Substitua _ServerName_ com o nome do servidor que você está usando.</span><span class="sxs-lookup"><span data-stu-id="ccdee-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="ccdee-273">Substitua _ProjectServerName_ pelo nome do diretório virtual do seu site do Project Server, como o PWA.</span><span class="sxs-lookup"><span data-stu-id="ccdee-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

<span data-ttu-id="ccdee-274">Outras variáveis que devem ser alteradas ou outros pré-requisitos são indicados na parte superior do exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="ccdee-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="ccdee-275">Verificando os resultados</span><span class="sxs-lookup"><span data-stu-id="ccdee-275">Verifying the results</span></span>
<span data-ttu-id="ccdee-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-276"></span></span>

<span data-ttu-id="ccdee-277">Obtendo e interpretando os resultados de um exemplo de código nem sempre são simples.</span><span class="sxs-lookup"><span data-stu-id="ccdee-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="ccdee-278">Por exemplo, se você criar um projeto, você deve publicar o projeto antes que pode aparecer na página Central de projetos no Project Web App.</span><span class="sxs-lookup"><span data-stu-id="ccdee-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="ccdee-279">Você pode verificar os resultados de amostra de código de várias maneiras, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ccdee-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="ccdee-280">Usar o cliente do Project Professional 2013 para abrir o projeto a partir do computador do Project Server e exibir os itens que você deseja.</span><span class="sxs-lookup"><span data-stu-id="ccdee-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="ccdee-281">Exibir projetos publicados na página Central de projetos do Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).</span><span class="sxs-lookup"><span data-stu-id="ccdee-281">View published projects on the Project Center page of Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="ccdee-282">Exiba o log de fila no Project Web App.</span><span class="sxs-lookup"><span data-stu-id="ccdee-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="ccdee-283">Abra a página Configurações do servidor (escolha o ícone **configurações** no canto superior direito) e escolha **Meus Trabalhos Enfileirados** sob a seção **Configurações pessoais** ( `http://ServerName/ProjectServerName/MyJobs.aspx`).</span><span class="sxs-lookup"><span data-stu-id="ccdee-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `http://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="ccdee-284">Na lista suspensa **modo de exibição** , você pode classificar pelo status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccdee-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="ccdee-285">O status padrão está **em andamento e trabalhos com falha da semana anterior**.</span><span class="sxs-lookup"><span data-stu-id="ccdee-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="ccdee-286">Use a página Configurações do servidor no Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) para gerenciar todos os trabalhos em fila e excluir ou forçar o check-in de objetos empresariais.</span><span class="sxs-lookup"><span data-stu-id="ccdee-286">Use the Server Settings page in Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="ccdee-287">Você deve ter permissões administrativas para acessar esses links na página Configurações do servidor.</span><span class="sxs-lookup"><span data-stu-id="ccdee-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="ccdee-288">Use o **Microsoft SQL Server Management Studio** para executar uma consulta em uma tabela do banco de dados do projeto.</span><span class="sxs-lookup"><span data-stu-id="ccdee-288">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database.</span></span> <span data-ttu-id="ccdee-289">Por exemplo, use a seguinte consulta para selecionar as 200 linhas superiores da publicação. Tabela MSP_WORKFLOW_STAGE_PDPS para mostrar informações sobre o projeto (PDPs) de páginas de detalhe em estágios do fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccdee-289">For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
   ```sql
    SELECT TOP 200 [STAGE_UID]
            ,[PDP_UID]
            ,[PDP_NAME]
            ,[PDP_POSITION]
            ,[PDP_ID]
            ,[PDP_STAGE_DESCRIPTION]
            ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
   ```

## <a name="cleaning-up"></a><span data-ttu-id="ccdee-290">Limpando</span><span class="sxs-lookup"><span data-stu-id="ccdee-290">Cleaning up</span></span>
<span data-ttu-id="ccdee-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-291"></span></span>

<span data-ttu-id="ccdee-292">Após testar alguns exemplos de códigos, existem objetos da empresa e as configurações que devem ser excluídas ou redefinir.</span><span class="sxs-lookup"><span data-stu-id="ccdee-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="ccdee-293">Você pode usar a página Configurações do servidor no Project Web App para gerenciar dados da empresa ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span><span class="sxs-lookup"><span data-stu-id="ccdee-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="ccdee-294">Links na página Configurações do servidor permitem excluir itens antigos, forçar o check-in de projetos, gerenciar a fila de trabalho para todos os usuários e realizar outras tarefas administrativas.</span><span class="sxs-lookup"><span data-stu-id="ccdee-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="ccdee-295">A seguir estão alguns dos links na página Configurações do servidor que você pode usar para atividades de limpeza típica após a execução de códigos de exemplo:</span><span class="sxs-lookup"><span data-stu-id="ccdee-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="ccdee-296">**Campos personalizados da empresa e tabelas de pesquisa**</span><span class="sxs-lookup"><span data-stu-id="ccdee-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="ccdee-297">**Gerenciar trabalhos em fila**</span><span class="sxs-lookup"><span data-stu-id="ccdee-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="ccdee-298">**Excluir objetos da empresa**</span><span class="sxs-lookup"><span data-stu-id="ccdee-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="ccdee-299">**Forçar o Check in de objetos empresariais**</span><span class="sxs-lookup"><span data-stu-id="ccdee-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="ccdee-300">**Tipos de projeto corporativo**</span><span class="sxs-lookup"><span data-stu-id="ccdee-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="ccdee-301">**Fases do fluxo de trabalho**</span><span class="sxs-lookup"><span data-stu-id="ccdee-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="ccdee-302">**Estágios do fluxo de trabalho**</span><span class="sxs-lookup"><span data-stu-id="ccdee-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="ccdee-303">**Páginas de detalhes do projeto**</span><span class="sxs-lookup"><span data-stu-id="ccdee-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="ccdee-304">**Períodos de relatório**</span><span class="sxs-lookup"><span data-stu-id="ccdee-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="ccdee-305">**Configurações de quadro de horários e padrões**</span><span class="sxs-lookup"><span data-stu-id="ccdee-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="ccdee-306">**Classificações de linha**</span><span class="sxs-lookup"><span data-stu-id="ccdee-306">**Line Classifications**</span></span>
    
<span data-ttu-id="ccdee-307">Configurações adicionais são gerenciadas pelo SharePoint Server 2013 para cada instância do Project Web App, em vez de uma página específica de configurações de servidor do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="ccdee-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="ccdee-308">No aplicativo Administração Central do SharePoint, escolha **Configurações gerais de aplicativos**, escolha **Gerenciar** em **Configurações do Project Server**e, em seguida, escolha a instância do Project Web App na lista suspensa na página Configurações do servidor .</span><span class="sxs-lookup"><span data-stu-id="ccdee-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="ccdee-309">Por exemplo, escolha **Manipuladores de eventos no servidor** , adicione ou exclua os manipuladores de eventos para a instância do Project Web App selecionada.</span><span class="sxs-lookup"><span data-stu-id="ccdee-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ccdee-310">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccdee-310">See also</span></span>
<span data-ttu-id="ccdee-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="ccdee-311"></span></span>

- [<span data-ttu-id="ccdee-312">Pré-requisitos para amostras de código com base em WCF no projeto</span><span class="sxs-lookup"><span data-stu-id="ccdee-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="ccdee-313">Utilizam a representação com WCF</span><span class="sxs-lookup"><span data-stu-id="ccdee-313">Use Impersonation with WCF</span></span>](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="ccdee-314">Visão geral da referência PSI do Project</span><span class="sxs-lookup"><span data-stu-id="ccdee-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="ccdee-315">Central de desenvolvedores do SharePoint</span><span class="sxs-lookup"><span data-stu-id="ccdee-315">SharePoint Developer Center</span></span>](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

