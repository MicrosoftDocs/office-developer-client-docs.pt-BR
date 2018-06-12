---
title: Introdução ao Project Server CSOM e .NET
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Você pode usar o modelo de objeto do cliente do Project Server 2013 (CSOM) para desenvolver soluções do Project Online e no local com o .NET Framework 4. Este artigo descreve como criar um aplicativo de console que usa o CSOM para criar e publicar projetos. Após a publicação de um projeto, o aplicativo aguarda o serviço de fila do Project Server concluir com a ação Publicar e, em seguida, lista os projetos publicados.
ms.openlocfilehash: 1815122ce824fcd2f9b8c9119346ca02c720ae89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771065"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a><span data-ttu-id="da190-105">Introdução ao Project Server CSOM e .NET</span><span class="sxs-lookup"><span data-stu-id="da190-105">Getting started with the Project Server CSOM and .NET</span></span>

<span data-ttu-id="da190-106">Você pode usar o modelo de objeto do cliente do Project Server 2013 (CSOM) para desenvolver soluções do Project Online e no local com o .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="da190-106">You can use the Project Server 2013 client-side object model (CSOM) to develop Project Online and on-premises solutions with the .NET Framework 4.</span></span> <span data-ttu-id="da190-107">Este artigo descreve como criar um aplicativo de console que usa o CSOM para criar e publicar projetos.</span><span class="sxs-lookup"><span data-stu-id="da190-107">This article describes how to create a console application that uses the CSOM to create and publish projects.</span></span> <span data-ttu-id="da190-108">Após a publicação de um projeto, o aplicativo aguarda o serviço de fila do Project Server concluir com a ação Publicar e, em seguida, lista os projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="da190-108">After publishing a project, the application waits for the Project Server Queue Service to finish with the publish action, and then lists the published projects.</span></span>
  
<span data-ttu-id="da190-109">Para obter uma introdução geral do Project Server CSOM, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="da190-109">For a general introduction to the Project Server CSOM, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span> <span data-ttu-id="da190-110">Para tópicos de referência no namespace CSOM, consulte [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span><span class="sxs-lookup"><span data-stu-id="da190-110">For reference topics in the CSOM namespace, see [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
## <a name="creating-a-csom-project-in-visual-studio"></a><span data-ttu-id="da190-111">Criando um projeto CSOM no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da190-111">Creating a CSOM project in Visual Studio</span></span>
<span data-ttu-id="da190-112"><a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a></span><span class="sxs-lookup"><span data-stu-id="da190-112"></span></span>

<span data-ttu-id="da190-113">Você pode usar o Visual Studio 2010 ou Visual Studio 2012 para desenvolver soluções que usam o Project Server CSOM.</span><span class="sxs-lookup"><span data-stu-id="da190-113">You can use Visual Studio 2010 or Visual Studio 2012 to develop solutions that use the Project Server CSOM.</span></span> <span data-ttu-id="da190-114">O Project Server CSOM inclui três assemblies para o desenvolvimento de aplicativos clientes, aplicativos do Microsoft Silverlight e Windows Phone 8 aplicativos usando o .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="da190-114">The Project Server CSOM includes three assemblies for development of client applications, Microsoft Silverlight applications, and Windows Phone 8 applications by using the .NET Framework 4.</span></span> <span data-ttu-id="da190-115">O CSOM também inclui um arquivo de JavaScript para o desenvolvimento de aplicativos web, conforme descrito em [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span><span class="sxs-lookup"><span data-stu-id="da190-115">The CSOM also includes a JavaScript file for development of web applications, as described in [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
<span data-ttu-id="da190-116">Você pode copiar o assembly CSOM que você precisa a partir de computador do Project Server ou o download do SDK do Project 2013 para um computador remoto de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="da190-116">You can copy the CSOM assembly that you need from the Project Server computer or from the Project 2013 SDK download to a remote development computer.</span></span> <span data-ttu-id="da190-117">O aplicativo de console **QueueCreateProject** descrita neste tópico não é um aplicativo Silverlight ou um aplicativo do Windows Phone 8, portanto é necessário o assembly Microsoft.ProjectServer.Client.dll.</span><span class="sxs-lookup"><span data-stu-id="da190-117">The **QueueCreateProject** console application that is described in this topic is not a Silverlight application or a Windows Phone 8 application, so you need the Microsoft.ProjectServer.Client.dll assembly.</span></span> <span data-ttu-id="da190-118">Como o CSOM é independente do baseado em ASMX ou WCF Project Server Interface (PSI), você não precisará definir referências de serviço para a PSI ou usar o namespace **Microsoft.Office.Project.Server.Library** .</span><span class="sxs-lookup"><span data-stu-id="da190-118">Because the CSOM is independent of the WCF-based or ASMX-based Project Server Interface (PSI), you do not have to set service references for the PSI or use the **Microsoft.Office.Project.Server.Library** namespace.</span></span> 
  
<span data-ttu-id="da190-119">O aplicativo de **QueueCreateProject** usa argumentos de linha de comando para o nome do projeto para criar e para o limite de tempo limite da fila.</span><span class="sxs-lookup"><span data-stu-id="da190-119">The **QueueCreateProject** application uses command-line arguments for the name of the project to create and for the queue timeout limit.</span></span> <span data-ttu-id="da190-120">No procedimento 1, você cria o aplicativo de console básica, adicione uma rotina para analisar a linha de comando e adicionar uma mensagem de uso, se houver erros na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="da190-120">In Procedure 1, you create the basic console application, add a routine to parse the command line, and add a usage message if there are errors in the command line.</span></span> 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a><span data-ttu-id="da190-121">Procedimento 1.</span><span class="sxs-lookup"><span data-stu-id="da190-121">Procedure 1.</span></span> <span data-ttu-id="da190-122">Para criar um projeto CSOM no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da190-122">To create a CSOM project in Visual Studio</span></span>

1. <span data-ttu-id="da190-123">Copie o assembly Microsoft.ProjectServer.Client.dll a partir do `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` pasta ao seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="da190-123">Copy the Microsoft.ProjectServer.Client.dll assembly from the  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` folder to your development computer.</span></span> <span data-ttu-id="da190-124">Copie o assembly para uma pasta conveniente para outros Project Server e assemblies de referência do SharePoint que você usará, tais como `C:\Project\Assemblies`.</span><span class="sxs-lookup"><span data-stu-id="da190-124">Copy the assembly to a convenient folder for other Project Server and SharePoint reference assemblies that you will use, such as  `C:\Project\Assemblies`.</span></span>
    
2. <span data-ttu-id="da190-125">Copie o assembly Microsoft.SharePoint.Client.dll e o assembly Microsoft.SharePoint.Client.Runtime.dll da mesma pasta de origem para o seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="da190-125">Copy the Microsoft.SharePoint.Client.dll assembly and the Microsoft.SharePoint.Client.Runtime.dll assembly from the same source folder to your development computer.</span></span> <span data-ttu-id="da190-126">O assembly Microsoft.ProjectServer.Client.dll tem dependências nos assemblies do SharePoint relacionados.</span><span class="sxs-lookup"><span data-stu-id="da190-126">The Microsoft.ProjectServer.Client.dll assembly has dependencies on the related SharePoint assemblies.</span></span>
    
3. <span data-ttu-id="da190-127">No Visual Studio, crie um aplicativo de console do Windows e definir a estrutura de destino para o .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="da190-127">In Visual Studio, create a Windows console application, and set the target framework to .NET Framework 4.</span></span> <span data-ttu-id="da190-128">Por exemplo, nomeie o aplicativo QueueCreateProject.</span><span class="sxs-lookup"><span data-stu-id="da190-128">For example, name the application QueueCreateProject.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="da190-129">Se você esquecer definir o destino correto, depois que o projeto do Visual Studio cria, abra **As propriedades de QueueCreateProject** no menu **projeto** .</span><span class="sxs-lookup"><span data-stu-id="da190-129">If you forget to set the correct target, after Visual Studio creates the project, open **QueueCreateProject Properties** in the **Project** menu.</span></span> <span data-ttu-id="da190-130">Na guia **aplicativo** , na lista suspensa **framework de destino** , escolha o **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="da190-130">On the **Application** tab, in the **Target framework** drop-down list, choose **.NET Framework 4**.</span></span> <span data-ttu-id="da190-131">Não use o **.NET Framework 4 Client Profile**.</span><span class="sxs-lookup"><span data-stu-id="da190-131">Do not use the **.NET Framework 4 Client Profile**.</span></span> 
  
4. <span data-ttu-id="da190-132">No Solution Explorer, defina referências a assemblies a seguir:</span><span class="sxs-lookup"><span data-stu-id="da190-132">In Solution Explorer, set references to the following assemblies:</span></span>
    
   - <span data-ttu-id="da190-133">Microsoft.ProjectServer.Client.dll</span><span class="sxs-lookup"><span data-stu-id="da190-133">Microsoft.ProjectServer.Client.dll</span></span>
   - <span data-ttu-id="da190-134">Microsoft.SharePoint.Client.dll</span><span class="sxs-lookup"><span data-stu-id="da190-134">Microsoft.SharePoint.Client.dll</span></span>
   - <span data-ttu-id="da190-135">Microsoft.SharePoint.Client.Runtime.dll</span><span class="sxs-lookup"><span data-stu-id="da190-135">Microsoft.SharePoint.Client.Runtime.dll</span></span>
    
5. <span data-ttu-id="da190-136">No arquivo Module. vb, edite o `using` instruções, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="da190-136">In the Program.cs file, edit the  `using` statements, as follows.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. <span data-ttu-id="da190-137">Adicione métodos para analisar os argumentos de linha de comando para o nome do projeto e o número de segundos para o tempo limite da fila, mostrar informações de uso e sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da190-137">Add methods to parse the command-line arguments for the project name and the number of seconds for queue timeout, show usage information, and exit the application.</span></span> <span data-ttu-id="da190-138">Substitua o corpo principal do código no arquivo Module. vb com o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="da190-138">Replace the main body of code in the Program.cs file with the following code.</span></span>
    
   ```cs
    namespace QueueCreateProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                if (!ParseCommandLine(args))
                {
                    Usage();
                    ExitApp();
                }
                /* Add calls to methods here to get the project context and create a project. */
                ExitApp();
            }
            // Parse the command line. Return true if there are no errors.
            private static bool ParseCommandLine(string[] args)
            {
                bool error = false;
                int argsLen = args.Length;
                try
                {
                    for (int i = 0; i < argsLen; i++)
                    {
                        if (error) break;
                        if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                            args[i] = "*" + args[i].Substring(1).ToLower();
                        switch (args[i])
                        {
                            case "*projname":
                            case "*n":
                                if (++i >= argsLen) return false;
                                projName = args[i];
                                break;
                            case "*timeout":
                            case "*t":
                                if (++i >= argsLen) return false;
                                timeoutSeconds = Convert.ToInt32(args[i]);
                                break;
                            case "*?":
                            default:
                                error = true;
                                break;
                        }
                    }
                }
                catch (FormatException)
                {
                    error = true;
                }
                if (string.IsNullOrEmpty(projName)) error = true;
                return !error;
            }
            private static void Usage()
            {
                string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
                example += "\nExample: QueueCreateProject -n \"My new project\"";
                example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
                Console.WriteLine(example);
            }
            private static void ExitApp()
            {
                Console.Write("\nPress any key to exit... ");
                Console.ReadKey(true);
                Environment.Exit(0);
            }
        }
    }
   ```

## <a name="getting-the-project-context"></a><span data-ttu-id="da190-139">Obtendo o contexto de projeto</span><span class="sxs-lookup"><span data-stu-id="da190-139">Getting the project context</span></span>
<span data-ttu-id="da190-140"><a name="pj15_GettingStartedCSOM_GettingContext"> </a></span><span class="sxs-lookup"><span data-stu-id="da190-140"></span></span>

<span data-ttu-id="da190-141">Desenvolvimento de CSOM requer o objeto **ProjectContext** a ser inicializado com a URL do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="da190-141">CSOM development requires the **ProjectContext** object to be initialized with the Project Web App URL.</span></span> <span data-ttu-id="da190-142">O código no procedimento 2 usa a constante **pwaPath** .</span><span class="sxs-lookup"><span data-stu-id="da190-142">The code in Procedure 2 uses the **pwaPath** constant.</span></span> <span data-ttu-id="da190-143">Se você planeja usar o aplicativo para várias instâncias do Project Web App, você poderia fazer **pwaPath** uma variável e adicione outro argumento da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="da190-143">If you plan to use the application for multiple instances of Project Web App, you could make **pwaPath** a variable and add another command-line argument.</span></span> 
  
### <a name="procedure-2-to-get-the-project-context"></a><span data-ttu-id="da190-144">Procedimento 2.</span><span class="sxs-lookup"><span data-stu-id="da190-144">Procedure 2.</span></span> <span data-ttu-id="da190-145">Para obter o contexto de projeto</span><span class="sxs-lookup"><span data-stu-id="da190-145">To get the project context</span></span>

1. <span data-ttu-id="da190-146">Adicione as constantes de classe de **programa** e variáveis que usará o aplicativo **QueueCreateProject** .</span><span class="sxs-lookup"><span data-stu-id="da190-146">Add **Program** class constants and variables that the **QueueCreateProject** application will use.</span></span> <span data-ttu-id="da190-147">Além da URL do Project Web App, o aplicativo usa o nome do tipo de projeto corporativo padrão (EPT), o nome do projeto para criar e tempo limite máximo da fila em segundos.</span><span class="sxs-lookup"><span data-stu-id="da190-147">In addition to the Project Web App URL, the application uses the name of the default enterprise project type (EPT), the name of the project to create, and a maximum queue timeout in seconds.</span></span> <span data-ttu-id="da190-148">Nesse caso, a variável **timeoutSeconds** permite testar como vários valores para o tempo limite afetam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da190-148">In this case, the **timeoutSeconds** variable enables you to test how various values for the timeout affect the application.</span></span> <span data-ttu-id="da190-149">O objeto **ProjectContext** é o objeto principal para acessar o CSOM.</span><span class="sxs-lookup"><span data-stu-id="da190-149">The **ProjectContext** object is the primary object for access to the CSOM.</span></span> 
    
   ```cs
    private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. <span data-ttu-id="da190-150">Substituir o `/* Add calls to methods here to get the project context and create a project. */` comentário com o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="da190-150">Replace the  `/* Add calls to methods here to get the project context and create a project. */` comment with the following code.</span></span> <span data-ttu-id="da190-151">O objeto **Microsoft.ProjectServer.Client.ProjectContext** é inicializado com a URL do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="da190-151">The **Microsoft.ProjectServer.Client.ProjectContext** object is initialized with the Project Web App URL.</span></span> <span data-ttu-id="da190-152">O método **CreateTestProject** e o método **ListPublishedProjects** são mostrados no procedimento 4 e 5 do procedimento.</span><span class="sxs-lookup"><span data-stu-id="da190-152">The **CreateTestProject** method and the **ListPublishedProjects** method are shown in Procedure 4 and Procedure 5.</span></span> 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a><span data-ttu-id="da190-153">Obtendo um tipo de projeto corporativo</span><span class="sxs-lookup"><span data-stu-id="da190-153">Getting an enterprise project type</span></span>
<span data-ttu-id="da190-154"><a name="pj15_GettingStartedCSOM_GettingEPT"> </a></span><span class="sxs-lookup"><span data-stu-id="da190-154"></span></span>

<span data-ttu-id="da190-155">O aplicativo de amostra **QueueCreateProject** explicitamente seleciona o EPT de projeto corporativo, para mostrar como um aplicativo pode selecionar o EPT para um projeto.</span><span class="sxs-lookup"><span data-stu-id="da190-155">The **QueueCreateProject** sample application explicitly selects the Enterprise Project EPT, to show how an application can select the EPT for a project.</span></span> <span data-ttu-id="da190-156">Se as informações de criação do projeto não especificam o GUID EPT, um aplicativo usaria o EPT padrão.</span><span class="sxs-lookup"><span data-stu-id="da190-156">If the project creation information does not specify the EPT GUID, an application would use the default EPT.</span></span> <span data-ttu-id="da190-157">O método **GetEptUid** é usado pelo método **CreateTestProject** descrito no procedimento 4.</span><span class="sxs-lookup"><span data-stu-id="da190-157">The **GetEptUid** method is used by the **CreateTestProject** method that is described in Procedure 4.</span></span> 
  
<span data-ttu-id="da190-158">O método **GetEptUid** consulta o objeto **ProjectContext** da coleção de **EnterpriseProjectTypes** onde o nome EPT é igual ao nome especificado.</span><span class="sxs-lookup"><span data-stu-id="da190-158">The **GetEptUid** method queries the **ProjectContext** object for the collection of **EnterpriseProjectTypes** where the EPT name equals the specified name.</span></span> <span data-ttu-id="da190-159">Depois de executar a consulta, a variável **eptUid** é definida como o GUID do primeiro objeto na coleção **eptList** **EnterpriseProjectType** .</span><span class="sxs-lookup"><span data-stu-id="da190-159">After executing the query, the **eptUid** variable is set to the GUID of the first **EnterpriseProjectType** object in the **eptList** collection.</span></span> <span data-ttu-id="da190-160">Como os nomes EPT são exclusivos, há apenas um objeto **EnterpriseProjectType** que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="da190-160">Because EPT names are unique, there is only one **EnterpriseProjectType** object that has the specified name.</span></span> 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a><span data-ttu-id="da190-161">3 do procedimento.</span><span class="sxs-lookup"><span data-stu-id="da190-161">Procedure 3.</span></span> <span data-ttu-id="da190-162">Para obter o GUID de uma EPT para um novo projeto</span><span class="sxs-lookup"><span data-stu-id="da190-162">To get the GUID of an EPT for a new project</span></span>

- <span data-ttu-id="da190-163">Adicione o método **GetEptUid** à classe de **programa** .</span><span class="sxs-lookup"><span data-stu-id="da190-163">Add the **GetEptUid** method to the **Program** class.</span></span> 
    
   ```cs
    // Get the GUID of the specified enterprise project type.
    private static Guid GetEptUid(string eptName)
    {
        Guid eptUid = Guid.Empty;
        try
        {
            // Get the list of EPTs that have the specified name. 
            // If the EPT name exists, the list will contain only one EPT.
            var eptList = projContext.LoadQuery(
                projContext.EnterpriseProjectTypes.Where(
                    ept => ept.Name == eptName));
            projContext.ExecuteQuery();
            eptUid = eptList.First().Id;
        }
        catch (Exception ex)
        {
            string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                eptName, ex.GetBaseException().ToString());
            throw new ArgumentException(msg);
        }
        return eptUid;
    }
   ```

<span data-ttu-id="da190-164">Há várias maneiras para localizar o GUID EPT.</span><span class="sxs-lookup"><span data-stu-id="da190-164">There are several ways to find the EPT GUID.</span></span> <span data-ttu-id="da190-165">A consulta mostrada no método **GetEptUid** é eficiente, pois ele baixa apenas o um objeto de **EnterpriseProjectType** que corresponde ao nome EPT.</span><span class="sxs-lookup"><span data-stu-id="da190-165">The query shown in the **GetEptUid** method is efficient because it downloads only the one **EnterpriseProjectType** object that matches the EPT name.</span></span> <span data-ttu-id="da190-166">A seguinte rotina de alternativa é menos eficiente, porque ele baixa a lista completa de EPTs para o aplicativo cliente e itera através da lista.</span><span class="sxs-lookup"><span data-stu-id="da190-166">The following alternate routine is less efficient, because it downloads the complete list of EPTs to the client application and iterates through the list.</span></span> 

```cs
foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
{
    if (ept.Name == eptName)
    {
        eptUid = ept.Id;
        break;
    }
}
```

<span data-ttu-id="da190-167">A seguinte rotina utiliza uma expressão de consulta e lambda LINQ para selecionar o objeto EPT, mas ainda downloads todos os objetos **EnterpriseProjectType** .</span><span class="sxs-lookup"><span data-stu-id="da190-167">The following routine uses a LINQ query and lambda expression to select the EPT object, but still downloads all of the **EnterpriseProjectType** objects.</span></span> 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a><span data-ttu-id="da190-168">Definindo as informações de criação e publicação do projeto</span><span class="sxs-lookup"><span data-stu-id="da190-168">Setting the creation information and publishing the project</span></span>
<span data-ttu-id="da190-169"><a name="pj15_GettingStartedCSOM_ProjectCreation"> </a></span><span class="sxs-lookup"><span data-stu-id="da190-169"></span></span>

<span data-ttu-id="da190-170">O método **CreateTestProject** cria um objeto **ProjectCreationInformation** e especifica as informações necessárias para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="da190-170">The **CreateTestProject** method creates a **ProjectCreationInformation** object and specifies the information that is required to create a project.</span></span> <span data-ttu-id="da190-171">O GUID do projeto e o nome for necessárias; a data de início, a descrição de projeto e o EPT GUID são opcionais.</span><span class="sxs-lookup"><span data-stu-id="da190-171">The project GUID and name are required; the start date, project description, and EPT GUID are optional.</span></span> 
  
<span data-ttu-id="da190-172">Depois de configurar as propriedades do novo projeto, o método **Projects.Add** adiciona o projeto para a coleção **Projects** .</span><span class="sxs-lookup"><span data-stu-id="da190-172">After setting the new project properties, the **Projects.Add** method adds the project to the **Projects** collection.</span></span> <span data-ttu-id="da190-173">Para salvar e publicar o projeto, você deve chamar o método **Projects.Update** para enviar uma mensagem para a fila do Project Server e criar o projeto.</span><span class="sxs-lookup"><span data-stu-id="da190-173">To save and publish the project, you must call the **Projects.Update** method to send a message to the Project Server queue and create the project.</span></span> 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a><span data-ttu-id="da190-174">4 do procedimento.</span><span class="sxs-lookup"><span data-stu-id="da190-174">Procedure 4.</span></span> <span data-ttu-id="da190-175">Para definir as propriedades do novo projeto, o projeto de criar e publicar o projeto</span><span class="sxs-lookup"><span data-stu-id="da190-175">To set the new project properties, create the project, and publish the project</span></span>

1. <span data-ttu-id="da190-176">Adicione o método **CreateTestProject** à classe de **programa** .</span><span class="sxs-lookup"><span data-stu-id="da190-176">Add the **CreateTestProject** method to the **Program** class.</span></span> <span data-ttu-id="da190-177">O código a seguir cria e publica um projeto, mas não espera até que o trabalho em fila ser concluída.</span><span class="sxs-lookup"><span data-stu-id="da190-177">The following code creates and publishes a project, but does not wait for the queue job to complete.</span></span> 
    
   ```cs
    // Create a project.
    private static bool CreateTestProject()
    {
        bool projCreated = false;
        try
        {
            Console.Write("\nCreating project: {0} ...", projName);
            ProjectCreationInformation newProj = new ProjectCreationInformation();
            newProj.Id = Guid.NewGuid();
            newProj.Name = projName;
            newProj.Description = "Test creating a project with CSOM";
            newProj.Start = DateTime.Today.Date;
            // Setting the EPT GUID is optional. If no EPT is specified, Project Server  
            // uses the default EPT. 
            newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
            PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
            QueueJob qJob = projContext.Projects.Update();
            /* Add code here to wait for the queue. */
        }
        catch(Exception ex)
        {
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("\nError: {0}", ex.Message);
            Console.ResetColor();
        }
        return projCreated;
    }
   ```

2. <span data-ttu-id="da190-178">Substituir o `/* Add code here to wait for the queue. */` comentário com o seguinte código para aguardar o trabalho em fila.</span><span class="sxs-lookup"><span data-stu-id="da190-178">Replace the  `/* Add code here to wait for the queue. */` comment with the following code to wait for the queue job.</span></span> <span data-ttu-id="da190-179">A rotina aguarda máximo do número de segundos especificado **timeoutSeconds** ou continua se o trabalho em fila for concluída antes do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="da190-179">The routine waits a maximum of the specified **timeoutSeconds** number of seconds, or proceeds if the queue job completes before the timeout.</span></span> <span data-ttu-id="da190-180">Para estados de trabalho de fila possíveis, consulte [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) .</span><span class="sxs-lookup"><span data-stu-id="da190-180">For possible queue job states, see [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) .</span></span> 
    
   <span data-ttu-id="da190-181">Chamar o método **Load** e o método **ExecuteQuery** para o objeto **QueueJob** é opcional.</span><span class="sxs-lookup"><span data-stu-id="da190-181">Calling the **Load** method and the **ExecuteQuery** method for the **QueueJob** object is optional.</span></span> <span data-ttu-id="da190-182">Se o objeto **QueueJob** não for inicializado quando você chama o método **WaitForQueue** , o Project Server inicializa a ele.</span><span class="sxs-lookup"><span data-stu-id="da190-182">If the **QueueJob** object is not initialized when you call the **WaitForQueue** method, Project Server initializes it.</span></span> 
    
   ```cs
    // Calling Load and ExecuteQuery for the queue job is optional.
    // projContext.Load(qJob);
    // projContext.ExecuteQuery();
    JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    if (jobState == JobState.Success)
    {
        projCreated = true;
    }
    else
    {
        Console.ForegroundColor = ConsoleColor.Yellow;
        Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
            timeoutSeconds);
        Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
        Console.ResetColor();
    }
    Console.WriteLine();
   ```

## <a name="listing-the-published-projects"></a><span data-ttu-id="da190-183">Listar os projetos publicados</span><span class="sxs-lookup"><span data-stu-id="da190-183">Listing the published projects</span></span>
<span data-ttu-id="da190-184"><a name="pj15_GettingStartedCSOM_ListingPublished"> </a></span><span class="sxs-lookup"><span data-stu-id="da190-184"></span></span>

<span data-ttu-id="da190-185">O método **ListPublishedProjects** obtém a coleção de todos os projetos publicados no Project Web App.</span><span class="sxs-lookup"><span data-stu-id="da190-185">The **ListPublishedProjects** method gets the collection of all projects that are published in Project Web App.</span></span> <span data-ttu-id="da190-186">Se o trabalho em fila que cria um projeto no 4 do procedimento não for concluída com êxito ou se esgotar o tempo, o novo projeto não está incluído no conjunto de **projetos** .</span><span class="sxs-lookup"><span data-stu-id="da190-186">If the queue job that creates a project in Procedure 4 does not complete successfully or times out, the new project is not included in the **Projects** collection.</span></span> 
  
### <a name="procedure-5-to-list-the-published-projects"></a><span data-ttu-id="da190-187">Procedimento 5.</span><span class="sxs-lookup"><span data-stu-id="da190-187">Procedure 5.</span></span> <span data-ttu-id="da190-188">Para listar os projetos publicados</span><span class="sxs-lookup"><span data-stu-id="da190-188">To list the published projects</span></span>

1. <span data-ttu-id="da190-189">Adicione o método **ListPublishedProjects** à classe de **programa** .</span><span class="sxs-lookup"><span data-stu-id="da190-189">Add the **ListPublishedProjects** method to the **Program** class.</span></span> 
    
   ```cs
    // List the published projects.
    private static void ListPublishedProjects()
    {
        // Get the list of projects on the server.
        projContext.Load(projContext.Projects);
        projContext.ExecuteQuery();
        Console.WriteLine("\nProject ID : Project name : Created date");
        foreach (PublishedProject pubProj in projContext.Projects)
        {
            Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                pubProj.CreatedDate.ToString());
        }
    }
   ```

2. <span data-ttu-id="da190-190">Defina o valor correto para sua URL do Project Web App, compilar o aplicativo **QueueCreateProject** e, em seguida, o aplicativo como 6 do procedimento de teste.</span><span class="sxs-lookup"><span data-stu-id="da190-190">Set the correct value for your Project Web App URL, compile the **QueueCreateProject** application, and then test the application as in Procedure 6.</span></span> 
    
## <a name="testing-the-queuecreateproject-application"></a><span data-ttu-id="da190-191">Testando o aplicativo QueueCreateProject</span><span class="sxs-lookup"><span data-stu-id="da190-191">Testing the QueueCreateProject application</span></span>
<span data-ttu-id="da190-192"><a name="pj15_GettingStartedCSOM_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="da190-192"></span></span>

<span data-ttu-id="da190-193">Quando você executa o aplicativo **QueueCreateProject** pela primeira vez em uma instância de teste do Project Web App, especialmente se o Project Server está instalado em uma máquina virtual, o aplicativo pode exigir mais tempo para executar que o tempo limite da fila de padrão de dez segundos.</span><span class="sxs-lookup"><span data-stu-id="da190-193">When you first run the **QueueCreateProject** application on a test instance of Project Web App, especially if Project Server is installed on a virtual machine, the application may require more time to run than the default queue timeout of ten seconds.</span></span> 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a><span data-ttu-id="da190-194">Procedimento 6.</span><span class="sxs-lookup"><span data-stu-id="da190-194">Procedure 6.</span></span> <span data-ttu-id="da190-195">Para testar o aplicativo QueueCreateProject</span><span class="sxs-lookup"><span data-stu-id="da190-195">To test the QueueCreateProject application</span></span>

1. <span data-ttu-id="da190-196">Abrir a janela **Propriedades QueueCreateProject** , selecione a guia **Depurar** e adicione os seguintes argumentos de linha de comando na seção **Opções** de inicialização:`-n "Test proj 1" -t 20`</span><span class="sxs-lookup"><span data-stu-id="da190-196">Open the **QueueCreateProject Properties** window, select the **Debug** tab, and then add the following command-line arguments in the **Start Options** section:  `-n "Test proj 1" -t 20`</span></span>
    
   <span data-ttu-id="da190-197">Executar o aplicativo (por exemplo, pressione **F5**).</span><span class="sxs-lookup"><span data-stu-id="da190-197">Run the application (for example, press **F5**).</span></span> <span data-ttu-id="da190-198">Se o valor de tempo limite é grande o suficiente, o aplicativo mostra a seguinte saída (se existirem de outros projetos publicados na sua instância do Project Web App, eles serão também exibidos):</span><span class="sxs-lookup"><span data-stu-id="da190-198">If the timeout value is long enough, the application shows the following output (if other published projects exist in your Project Web App instance, they will also be shown):</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. <span data-ttu-id="da190-199">Execute o teste de outro com os seguintes argumentos de linha de comando, para usar o tempo limite padrão de 10 segundos fila:`-n "Test proj 1"`</span><span class="sxs-lookup"><span data-stu-id="da190-199">Run another test with the following command-line arguments, to use the default 10-second queue timeout: `-n "Test proj 1"`</span></span>
    
   <span data-ttu-id="da190-200">Porque já existe um teste proj 1, o aplicativo mostra a seguinte saída.</span><span class="sxs-lookup"><span data-stu-id="da190-200">Because Test proj 1 already exists, the application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. <span data-ttu-id="da190-201">Execute o teste de outro com os seguintes argumentos de linha de comando, para usar o tempo limite padrão de 10 segundos fila:`-n "Test proj 2"`</span><span class="sxs-lookup"><span data-stu-id="da190-201">Run another test with the following command-line arguments, to use the default 10-second queue timeout:  `-n "Test proj 2"`</span></span>
    
   <span data-ttu-id="da190-202">O aplicativo **QueueCreateProject** cria e publica o projeto chamado Test proj 2.</span><span class="sxs-lookup"><span data-stu-id="da190-202">The **QueueCreateProject** application creates and publishes the project named Test proj 2.</span></span> 
    
4. <span data-ttu-id="da190-203">Executar o teste outra com os seguintes argumentos de linha de comando e defina o tempo limite para ser muito curto para o trabalho em fila para concluir:`-n "Test proj 3" -t 1`</span><span class="sxs-lookup"><span data-stu-id="da190-203">Run another test with the following command-line arguments, and set the timeout to be too short for the queue job to finish:  `-n "Test proj 3" -t 1`</span></span>
    
   <span data-ttu-id="da190-204">Porque o tempo limite da fila for muito curto, o projeto não será criado.</span><span class="sxs-lookup"><span data-stu-id="da190-204">Because the queue timeout is too short, the project is not created.</span></span> <span data-ttu-id="da190-205">O aplicativo mostra a seguinte saída.</span><span class="sxs-lookup"><span data-stu-id="da190-205">The application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. <span data-ttu-id="da190-206">Modificar o código para que o aplicativo não espera até que o trabalho em fila.</span><span class="sxs-lookup"><span data-stu-id="da190-206">Modify the code so that the application does not wait for the queue job.</span></span> <span data-ttu-id="da190-207">Por exemplo, comente o código que aguarda para a fila, exceto para o `projCreated = true` linha, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="da190-207">For example, comment out the code that waits for the queue, except for the  `projCreated = true` line, as follows.</span></span> 
    
   ```cs
    //JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    //if (jobState == JobState.Success)
    //{
    projCreated = true;
    //}
    //else
    //{
    //    Console.ForegroundColor = ConsoleColor.Yellow;
    //    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.",
    //        timeoutSeconds);
    //    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
    //    Console.ResetColor();
    //}
    
   ```

6. <span data-ttu-id="da190-208">Recompilar o aplicativo e execute outro teste com os seguintes argumentos de linha de comando:`-n "Test proj 4"`</span><span class="sxs-lookup"><span data-stu-id="da190-208">Recompile the application and run another test with the following command-line arguments:  `-n "Test proj 4"`</span></span>
    
   <span data-ttu-id="da190-209">Porque a rotina **WaitForQueue** foi comentada, o aplicativo não usa o valor de tempo limite padrão.</span><span class="sxs-lookup"><span data-stu-id="da190-209">Because the **WaitForQueue** routine is commented out, the application does not use the default timeout value.</span></span> <span data-ttu-id="da190-210">Mesmo que o aplicativo não esperar por uma fila, ele poderá mostrar teste proj 4, se a ação de publicação no Project Server for rápida o bastante.</span><span class="sxs-lookup"><span data-stu-id="da190-210">Even though the application does not wait for the queue, it may show Test proj 4, if the publish action in Project Server is fast enough.</span></span> 
    
   ```MS-DOS
    Creating project: Test proj 4 ...
    Project ID : Project name : Created date
            cdd54103-082f-425c-b075-9ff52ac7d4e6 :
            Test proj 2 : 9/25/2011 4:28:55 PM
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
            5c0c73f2-f5dd-499b-8bd8-ebb74bf8c122 :
            Test proj 4 : 9/25/2011 4:39:21 PM
    Press any key to exit...
   ```

<span data-ttu-id="da190-211">Atualize a página da Central de projetos no Project Web App (`http://ServerName/ProjectServerName/Projects.aspx`), para mostrar os projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="da190-211">Refresh the Project Center page in Project Web App (`http://ServerName/ProjectServerName/Projects.aspx`), to show the published projects.</span></span> <span data-ttu-id="da190-212">A figura a seguir mostra que os projetos de teste são publicados.</span><span class="sxs-lookup"><span data-stu-id="da190-212">The following figure shows that the test projects are published.</span></span>

<span data-ttu-id="da190-213">**Verificando os projetos publicados no Project Web App**</span><span class="sxs-lookup"><span data-stu-id="da190-213">**Checking the published projects in Project Web App**</span></span>

<span data-ttu-id="da190-214">![Verificando os projetos publicados no Project Web App] (media/pj15_GetStartedCSOMNET_pwa.gif "Verificando os projetos publicados no Project Web App")</span><span class="sxs-lookup"><span data-stu-id="da190-214">![Checking the published projects in Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Checking the published projects in Project Web App")</span></span>
  
<span data-ttu-id="da190-215">O aplicativo de exemplo **QueueCreateProject** mostra um exemplo típico de como criar uma entidade de projeto com o CSOM, usando a classe **ProjectCreationInformation** , como adicionar o projeto à coleção publicada, como aguardar por um trabalho de fila usando o método **WaitForQueue** e como enumere a coleção de projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="da190-215">The **QueueCreateProject** sample application shows a typical example of how to create a project entity with the CSOM by using the **ProjectCreationInformation** class, how to add the project to the published collection, how to wait for a queue job by using the **WaitForQueue** method, and how to enumerate the collection of published projects.</span></span> 
  
## <a name="complete-code-example"></a><span data-ttu-id="da190-216">Exemplo de código completo</span><span class="sxs-lookup"><span data-stu-id="da190-216">Complete code example</span></span>
<span data-ttu-id="da190-217"><a name="pj15_GettingStartedCSOM_CompleteCode"> </a></span><span class="sxs-lookup"><span data-stu-id="da190-217"></span></span>

<span data-ttu-id="da190-218">Este é o código completo para o aplicativo de exemplo **QueueCreateProject** .</span><span class="sxs-lookup"><span data-stu-id="da190-218">The following is the complete code for the **QueueCreateProject** sample application.</span></span> <span data-ttu-id="da190-219">Referência de classe do [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) também inclui o código neste tópico.</span><span class="sxs-lookup"><span data-stu-id="da190-219">The [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) class reference also includes the code in this topic.</span></span> 
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Microsoft.ProjectServer.Client;
namespace QueueCreateProject
{
    class Program
    {
        private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
        private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
        private static string projName = string.Empty;
        private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
        private static ProjectContext projContext;
        static void Main(string[] args)
        {
            if (!ParseCommandLine(args))
            {
                Usage();
                ExitApp();
            }
            projContext = new ProjectContext(pwaPath);
            if (CreateTestProject())
                ListPublishedProjects();
            else
                Console.WriteLine("\nProject creation failed: {0}", projName);
            ExitApp();
        }
        // Create a project.
        private static bool CreateTestProject()
        {
            bool projCreated = false;
            try
            {
                Console.Write("\nCreating project: {0} ...", projName);
                ProjectCreationInformation newProj = new ProjectCreationInformation();
                newProj.Id = Guid.NewGuid();
                newProj.Name = projName;
                newProj.Description = "Test creating a project with CSOM";
                newProj.Start = DateTime.Today.Date;
                // Setting the EPT GUID is optional. If no EPT is specified, Project Server uses 
                // the default EPT. 
                newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
                PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
                QueueJob qJob = projContext.Projects.Update();
                // Calling Load and ExecuteQuery for the queue job is optional. If qJob is 
                // not initialized when you call WaitForQueue, Project Server initializes it.
                // projContext.Load(qJob);
                // projContext.ExecuteQuery();
                JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
                if (jobState == JobState.Success)
                {
                    projCreated = true;
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
                        timeoutSeconds);
                    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
                    Console.ResetColor();
                }
                Console.WriteLine();
            }
            catch(Exception ex)
            {
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine("\nError: {0}", ex.Message);
                Console.ResetColor();
            }
            return projCreated;
        }
        // Get the GUID of the specified enterprise project type.
        private static Guid GetEptUid(string eptName)
        {
            Guid eptUid = Guid.Empty;
            try
            {
                // Get the list of EPTs that have the specified name. 
                // If the EPT name exists, the list will contain only one EPT.
                var eptList = projContext.LoadQuery(
                    projContext.EnterpriseProjectTypes.Where(
                        ept => ept.Name == eptName));
                projContext.ExecuteQuery();
                eptUid = eptList.First().Id;
                // Alternate routines to find the EPT GUID. Both (a) and (b) download the entire list of EPTs.
                // (a) Using a foreach block:
                //foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
                //{
                //    if (ept.Name == eptName)
                //    {
                //        eptUid = ept.Id;
                //        break;
                //    }
                //}
                // (b) Querying for the EPT list, and then using a lambda expression to select the EPT:
                //var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
                //projContext.ExecuteQuery();
                //eptUid = eptList.First(ept => ept.Name == eptName).Id;
            }
            catch (Exception ex)
            {
                string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                    eptName, ex.GetBaseException().ToString());
                throw new ArgumentException(msg);
            }
            return eptUid;
        }
        // List the published projects.
        private static void ListPublishedProjects()
        {
            // Get the list of projects on the server.
            projContext.Load(projContext.Projects);
            projContext.ExecuteQuery();
            Console.WriteLine("\nProject ID : Project name : Created date");
            foreach (PublishedProject pubProj in projContext.Projects)
            {
                Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                    pubProj.CreatedDate.ToString());
            }
        }
        // Parse the command line. Return true if there are no errors.
        private static bool ParseCommandLine(string[] args)
        {
            bool error = false;
            int argsLen = args.Length;
            try
            {
                for (int i = 0; i < argsLen; i++)
                {
                    if (error) break;
                    if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                        args[i] = "*" + args[i].Substring(1).ToLower();
                    switch (args[i])
                    {
                        case "*projname":
                        case "*n":
                            if (++i >= argsLen) return false;
                            projName = args[i];
                            break;
                        case "*timeout":
                        case "*t":
                            if (++i >= argsLen) return false;
                            timeoutSeconds = Convert.ToInt32(args[i]);
                            break;
                        case "*?":
                        default:
                            error = true;
                            break;
                    }
                }
            }
            catch (FormatException)
            {
                error = true;
            }
            if (string.IsNullOrEmpty(projName)) error = true;
            return !error;
        }
        private static void Usage()
        {
            string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
            example += "\nExample: QueueCreateProject -n \"My new project\"";
            example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
            Console.WriteLine(example);
        }
        private static void ExitApp()
        {
            Console.Write("\nPress any key to exit... ");
            Console.ReadKey(true);
            Environment.Exit(0);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="da190-220">Confira também</span><span class="sxs-lookup"><span data-stu-id="da190-220">See also</span></span>

- [<span data-ttu-id="da190-221">Atualizações para desenvolvedores no Project 2013</span><span class="sxs-lookup"><span data-stu-id="da190-221">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md) 
- [<span data-ttu-id="da190-222">Modelo de objeto do cliente (CSOM) para o Project 2013</span><span class="sxs-lookup"><span data-stu-id="da190-222">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

