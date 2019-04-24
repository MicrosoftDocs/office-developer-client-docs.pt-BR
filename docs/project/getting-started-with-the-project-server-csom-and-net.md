---
title: 'Introdução a CSOM e .NET do Project Server '
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Você pode usar o CSOM (modelo de objeto do lado do cliente) do Project Server 2013 para desenvolver soluções locais e do Project Online com o .NET Framework 4. Este artigo descreve como criar um aplicativo de console que usa o CSOM para criar e publicar projetos. Depois de publicar um projeto, o aplicativo aguarda a conclusão do serviço de enfileiramento do Project Server com a ação Publicar e, em seguida, lista os projetos publicados.
localization_priority: Priority
ms.openlocfilehash: b53587ca1959faefdc1b40f08c4adfda4ee11d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360563"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a><span data-ttu-id="30fcf-105">Introdução a CSOM e .NET do Project Server </span><span class="sxs-lookup"><span data-stu-id="30fcf-105">Getting started with the Project Server CSOM and .NET</span></span>

<span data-ttu-id="30fcf-106">Você pode usar o CSOM (modelo de objeto do lado do cliente) do Project Server 2013 para desenvolver soluções locais e do Project Online com o .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="30fcf-106">You can use the Project Server 2013 client-side object model (CSOM) to develop Project Online and on-premises solutions with the .NET Framework 4.</span></span> <span data-ttu-id="30fcf-107">Este artigo descreve como criar um aplicativo de console que usa o CSOM para criar e publicar projetos.</span><span class="sxs-lookup"><span data-stu-id="30fcf-107">This article describes how to create a console application that uses the CSOM to create and publish projects.</span></span> <span data-ttu-id="30fcf-108">Depois de publicar um projeto, o aplicativo aguarda a conclusão do serviço de enfileiramento do Project Server com a ação Publicar e, em seguida, lista os projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="30fcf-108">After publishing a project, the application waits for the Project Server Queue Service to finish with the publish action, and then lists the published projects.</span></span>
  
<span data-ttu-id="30fcf-109">Para uma introdução geral ao CSOM do Project Server, consulte [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="30fcf-109">For a general introduction to the Project Server CSOM, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span> <span data-ttu-id="30fcf-110">Para saber sobre os tópicos de referência no namespace do CSOM, consulte [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx).</span><span class="sxs-lookup"><span data-stu-id="30fcf-110">For reference topics in the CSOM namespace, see [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
## <a name="creating-a-csom-project-in-visual-studio"></a><span data-ttu-id="30fcf-111">Criar um projeto CSOM no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30fcf-111">Creating a CSOM project in Visual Studio</span></span>
<span data-ttu-id="30fcf-112"><a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a></span><span class="sxs-lookup"><span data-stu-id="30fcf-112"></span></span>

<span data-ttu-id="30fcf-113">Você pode usar o Visual Studio 2010 ou o Visual Studio 2012 para desenvolver soluções que usam CSOM do Project Server.</span><span class="sxs-lookup"><span data-stu-id="30fcf-113">You can use Visual Studio 2010 or Visual Studio 2012 to develop solutions that use the Project Server CSOM.</span></span> <span data-ttu-id="30fcf-114">O CSOM do Project Server contém três assemblies para desenvolvimento de aplicativos de clientes, do Microsoft Silverlight e do Windows Phone 8 usando o .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="30fcf-114">The Project Server CSOM includes three assemblies for development of client applications, Microsoft Silverlight applications, and Windows Phone 8 applications by using the .NET Framework 4.</span></span> <span data-ttu-id="30fcf-115">O CSOM também inclui um arquivo JavaScript para desenvolvimento de aplicativos Web, como descrito em [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span><span class="sxs-lookup"><span data-stu-id="30fcf-115">The CSOM also includes a JavaScript file for development of web applications, as described in [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
<span data-ttu-id="30fcf-116">Você pode copiar o assembly necessário do CSOM do computador do Project Server ou do download do SDK do Project 2013 para um computador remoto de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="30fcf-116">You can copy the CSOM assembly that you need from the Project Server computer or from the Project 2013 SDK download to a remote development computer.</span></span> <span data-ttu-id="30fcf-117">O aplicativo de console **QueueCreateProject** que descrevemos neste tópico não é um aplicativo do Silverlight ou do Windows Phone 8, portanto, você precisa do assembly Microsoft.ProjectServer.Client.dll.</span><span class="sxs-lookup"><span data-stu-id="30fcf-117">The **QueueCreateProject** console application that is described in this topic is not a Silverlight application or a Windows Phone 8 application, so you need the Microsoft.ProjectServer.Client.dll assembly.</span></span> <span data-ttu-id="30fcf-118">Como o CSOM é independente da PSI (Interface do Project Server) baseada no ASMX ou no WCF, não é necessário definir as referências de serviço da PSI ou usar o namespace **Microsoft.Office.Project.Server.Library**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-118">Because the CSOM is independent of the WCF-based or ASMX-based Project Server Interface (PSI), you do not have to set service references for the PSI or use the **Microsoft.Office.Project.Server.Library** namespace.</span></span> 
  
<span data-ttu-id="30fcf-119">O aplicativo **QueueCreateProject** usa argumentos de linha de comando no nome do projeto a criar e no limite de tempo da fila.</span><span class="sxs-lookup"><span data-stu-id="30fcf-119">The **QueueCreateProject** application uses command-line arguments for the name of the project to create and for the queue timeout limit.</span></span> <span data-ttu-id="30fcf-120">No procedimento 1, crie o aplicativo de console básico, adicione uma rotina para analisar a linha de comando e adicione uma mensagem de uso, caso haja erros na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="30fcf-120">In Procedure 1, you create the basic console application, add a routine to parse the command line, and add a usage message if there are errors in the command line.</span></span> 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a><span data-ttu-id="30fcf-121">Procedimento 1.</span><span class="sxs-lookup"><span data-stu-id="30fcf-121">Procedure 1.</span></span> <span data-ttu-id="30fcf-122">Para criar um projeto CSOM no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30fcf-122">To create a CSOM project in Visual Studio</span></span>

1. <span data-ttu-id="30fcf-123">Copie o assembly Microsoft.ProjectServer.Client.dll da pasta `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` para o computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="30fcf-123">Copy the Microsoft.ProjectServer.Client.dll assembly from the  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` folder to your development computer.</span></span> <span data-ttu-id="30fcf-124">Copie o assembly para uma pasta conveniente para outros assemblies de referência do Project Server e do SharePoint que você venha a usar, como `C:\Project\Assemblies`.</span><span class="sxs-lookup"><span data-stu-id="30fcf-124">Copy the assembly to a convenient folder for other Project Server and SharePoint reference assemblies that you will use, such as  `C:\Project\Assemblies`.</span></span>
    
2. <span data-ttu-id="30fcf-125">Copie os assemblies Microsoft.SharePoint.Client.dll e Microsoft.SharePoint.Client.Runtime.dll da mesma pasta de origem para o computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="30fcf-125">Copy the Microsoft.SharePoint.Client.dll assembly and the Microsoft.SharePoint.Client.Runtime.dll assembly from the same source folder to your development computer.</span></span> <span data-ttu-id="30fcf-126">O assembly Microsoft.ProjectServer.Client.dll tem dependências nos assemblies relacionados do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="30fcf-126">The Microsoft.ProjectServer.Client.dll assembly has dependencies on the related SharePoint assemblies.</span></span>
    
3. <span data-ttu-id="30fcf-127">No Visual Studio, crie um aplicativo de console do Windows e configure a estrutura de destino para o .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="30fcf-127">In Visual Studio, create a Windows console application, and set the target framework to .NET Framework 4.</span></span> <span data-ttu-id="30fcf-128">Por exemplo, nomeie o aplicativo como QueueCreateProject.</span><span class="sxs-lookup"><span data-stu-id="30fcf-128">For example, name the application QueueCreateProject.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="30fcf-129">Se você esquecer de definir o destino correto, depois que o Visual Studio criar o projeto, abra **Propriedades de QueueCreateProject** no menu **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-129">If you forget to set the correct target, after Visual Studio creates the project, open **QueueCreateProject Properties** in the **Project** menu.</span></span> <span data-ttu-id="30fcf-130">Na guia **Aplicativo**, na lista suspensa **Estrutura de Destino**, escolha **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-130">On the **Application** tab, in the **Target framework** drop-down list, choose **.NET Framework 4**.</span></span> <span data-ttu-id="30fcf-131">Não use **.NET Framework 4 Client Profile**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-131">Do not use the **.NET Framework 4 Client Profile**.</span></span> 
  
4. <span data-ttu-id="30fcf-132">No Gerenciador de Soluções, defina as referências para os seguintes assemblies:</span><span class="sxs-lookup"><span data-stu-id="30fcf-132">In Solution Explorer, set references to the following assemblies:</span></span>
    
   - <span data-ttu-id="30fcf-133">Microsoft.ProjectServer.Client.dll</span><span class="sxs-lookup"><span data-stu-id="30fcf-133">Microsoft.ProjectServer.Client.dll</span></span>
   - <span data-ttu-id="30fcf-134">Microsoft.SharePoint.Client.dll</span><span class="sxs-lookup"><span data-stu-id="30fcf-134">Microsoft.SharePoint.Client.dll</span></span>
   - <span data-ttu-id="30fcf-135">Microsoft.SharePoint.Client.Runtime.dll</span><span class="sxs-lookup"><span data-stu-id="30fcf-135">Microsoft.SharePoint.Client.Runtime.dll</span></span>
    
5. <span data-ttu-id="30fcf-136">No arquivo Program.cs, edite as instruções `using` conforme a seguir.</span><span class="sxs-lookup"><span data-stu-id="30fcf-136">In the Program.cs file, edit the  `using` statements, as follows.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. <span data-ttu-id="30fcf-137">Adicione métodos para analisar os argumentos da linha de comando para o nome do projeto e o número de segundos do tempo limite da fila, para mostrar as informações de uso e para sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30fcf-137">Add methods to parse the command-line arguments for the project name and the number of seconds for queue timeout, show usage information, and exit the application.</span></span> <span data-ttu-id="30fcf-138">Substitua o corpo principal do código no arquivo Program.cs com o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="30fcf-138">Replace the main body of code in the Program.cs file with the following code.</span></span>
    
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

## <a name="getting-the-project-context"></a><span data-ttu-id="30fcf-139">Obter o contexto de projeto</span><span class="sxs-lookup"><span data-stu-id="30fcf-139">Getting the project context</span></span>
<span data-ttu-id="30fcf-140"><a name="pj15_GettingStartedCSOM_GettingContext"> </a></span><span class="sxs-lookup"><span data-stu-id="30fcf-140"></span></span>

<span data-ttu-id="30fcf-141">O desenvolvimento de CSOM requer que o objeto **ProjectContext** seja iniciado com a URL do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="30fcf-141">CSOM development requires the **ProjectContext** object to be initialized with the Project Web App URL.</span></span> <span data-ttu-id="30fcf-142">O código no procedimento 2 usa a constante **pwaPath**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-142">The code in Procedure 2 uses the **pwaPath** constant.</span></span> <span data-ttu-id="30fcf-143">Se você planeja usar o aplicativo para várias instâncias do Project Web App, é possível transformar **pwaPath** em uma variável e adicionar outro argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="30fcf-143">If you plan to use the application for multiple instances of Project Web App, you could make **pwaPath** a variable and add another command-line argument.</span></span> 
  
### <a name="procedure-2-to-get-the-project-context"></a><span data-ttu-id="30fcf-144">Procedimento 2.</span><span class="sxs-lookup"><span data-stu-id="30fcf-144">Procedure 2.</span></span> <span data-ttu-id="30fcf-145">Para obter o contexto do projeto</span><span class="sxs-lookup"><span data-stu-id="30fcf-145">To get the project context</span></span>

1. <span data-ttu-id="30fcf-146">Adicione as variáveis e constantes de classe de **Program** que o aplicativo **QueueCreateProject** usará.</span><span class="sxs-lookup"><span data-stu-id="30fcf-146">Add **Program** class constants and variables that the **QueueCreateProject** application will use.</span></span> <span data-ttu-id="30fcf-147">Além da URL do Project Web App, o aplicativo usa o nome do tipo de projeto empresarial padrão (EPT), o nome do projeto a criar e um tempo limite máximo da fila em segundos.</span><span class="sxs-lookup"><span data-stu-id="30fcf-147">In addition to the Project Web App URL, the application uses the name of the default enterprise project type (EPT), the name of the project to create, and a maximum queue timeout in seconds.</span></span> <span data-ttu-id="30fcf-148">Nesse caso, a variável **timeoutSeconds** permite testar como vários valores de tempo limite afetam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30fcf-148">In this case, the **timeoutSeconds** variable enables you to test how various values for the timeout affect the application.</span></span> <span data-ttu-id="30fcf-149">O objeto **ProjectContext** é o objeto principal para acessar o CSOM.</span><span class="sxs-lookup"><span data-stu-id="30fcf-149">The **ProjectContext** object is the primary object for access to the CSOM.</span></span> 
    
   ```cs
    private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. <span data-ttu-id="30fcf-150">Substitua o comentário `/* Add calls to methods here to get the project context and create a project. */` pelo seguinte código.</span><span class="sxs-lookup"><span data-stu-id="30fcf-150">Replace the  `/* Add calls to methods here to get the project context and create a project. */` comment with the following code.</span></span> <span data-ttu-id="30fcf-151">O objeto **Microsoft.ProjectServer.Client.ProjectContext** inicia com a URL do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="30fcf-151">The **Microsoft.ProjectServer.Client.ProjectContext** object is initialized with the Project Web App URL.</span></span> <span data-ttu-id="30fcf-152">Os métodos **CreateTestProject** e **ListPublishedProjects** são mostrados nos procedimentos 4 e 5.</span><span class="sxs-lookup"><span data-stu-id="30fcf-152">The **CreateTestProject** method and the **ListPublishedProjects** method are shown in Procedure 4 and Procedure 5.</span></span> 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a><span data-ttu-id="30fcf-153">Obter um tipo de projeto empresarial</span><span class="sxs-lookup"><span data-stu-id="30fcf-153">Getting an enterprise project type</span></span>
<span data-ttu-id="30fcf-154"><a name="pj15_GettingStartedCSOM_GettingEPT"> </a></span><span class="sxs-lookup"><span data-stu-id="30fcf-154"></span></span>

<span data-ttu-id="30fcf-155">O aplicativo de exemplo**QueueCreateProject** seleciona explicitamente o EPT de Projeto Empresarial para mostrar como um aplicativo pode selecionar o EPT para um projeto.</span><span class="sxs-lookup"><span data-stu-id="30fcf-155">The **QueueCreateProject** sample application explicitly selects the Enterprise Project EPT, to show how an application can select the EPT for a project.</span></span> <span data-ttu-id="30fcf-156">Se as informações de criação do projeto não especificarem o GUID do EPT, um aplicativo usa o EPT padrão.</span><span class="sxs-lookup"><span data-stu-id="30fcf-156">If the project creation information does not specify the EPT GUID, an application would use the default EPT.</span></span> <span data-ttu-id="30fcf-157">O método **GetEptUid** é usado pelo método **CreateTestProject** descrito no procedimento 4.</span><span class="sxs-lookup"><span data-stu-id="30fcf-157">The **GetEptUid** method is used by the **CreateTestProject** method that is described in Procedure 4.</span></span> 
  
<span data-ttu-id="30fcf-158">O método **GetEptUid** consulta o objeto **ProjectContext** pela coleção de **EnterpriseProjectTypes** em que o nome do EPT representa o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="30fcf-158">The **GetEptUid** method queries the **ProjectContext** object for the collection of **EnterpriseProjectTypes** where the EPT name equals the specified name.</span></span> <span data-ttu-id="30fcf-159">Depois de executar a consulta, a variável **eptUid** é definida como o GUID do primeiro objeto **EnterpriseProjectType** na coleção **eptList**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-159">After executing the query, the **eptUid** variable is set to the GUID of the first **EnterpriseProjectType** object in the **eptList** collection.</span></span> <span data-ttu-id="30fcf-160">Como os nomes de EPTs são exclusivos, há apenas um objeto **EnterpriseProjectType** com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="30fcf-160">Because EPT names are unique, there is only one **EnterpriseProjectType** object that has the specified name.</span></span> 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a><span data-ttu-id="30fcf-161">Procedimento 3.</span><span class="sxs-lookup"><span data-stu-id="30fcf-161">Procedure 3.</span></span> <span data-ttu-id="30fcf-162">Para obter o GUID de um EPT para um novo projeto</span><span class="sxs-lookup"><span data-stu-id="30fcf-162">To get the GUID of an EPT for a new project</span></span>

- <span data-ttu-id="30fcf-163">Adicione o método **GetEptUid** à classe **Program**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-163">Add the **GetEptUid** method to the **Program** class.</span></span> 
    
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

<span data-ttu-id="30fcf-164">Há várias maneiras de criar um GUID de EPT.</span><span class="sxs-lookup"><span data-stu-id="30fcf-164">There are several ways to find the EPT GUID.</span></span> <span data-ttu-id="30fcf-165">A consulta mostrada no método **GetEptUid** é eficiente, pois baixa apenas aquele objeto **EnterpriseProjectType** que corresponde ao nome do EPT.</span><span class="sxs-lookup"><span data-stu-id="30fcf-165">The query shown in the **GetEptUid** method is efficient because it downloads only the one **EnterpriseProjectType** object that matches the EPT name.</span></span> <span data-ttu-id="30fcf-166">A rotina alternativa a seguir é menos eficiente porque baixa toda a lista de EPTs com o aplicativo cliente e percorre a lista.</span><span class="sxs-lookup"><span data-stu-id="30fcf-166">The following alternate routine is less efficient, because it downloads the complete list of EPTs to the client application and iterates through the list.</span></span> 

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

<span data-ttu-id="30fcf-167">A rotina a seguir usa uma consulta LINQ e expressões lambda para selecionar o objeto EPT, mas ainda baixa todos os objetos **EnterpriseProjectType**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-167">The following routine uses a LINQ query and lambda expression to select the EPT object, but still downloads all of the **EnterpriseProjectType** objects.</span></span> 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a><span data-ttu-id="30fcf-168">Definir as informações de criação e publicação do projeto</span><span class="sxs-lookup"><span data-stu-id="30fcf-168">Setting the creation information and publishing the project</span></span>
<span data-ttu-id="30fcf-169"><a name="pj15_GettingStartedCSOM_ProjectCreation"> </a></span><span class="sxs-lookup"><span data-stu-id="30fcf-169"></span></span>

<span data-ttu-id="30fcf-170">O método **CreateTestProject** cria um objeto **ProjectCreationInformation** e especifica as informações necessárias para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="30fcf-170">The **CreateTestProject** method creates a **ProjectCreationInformation** object and specifies the information that is required to create a project.</span></span> <span data-ttu-id="30fcf-171">O nome e o GUID do projeto são necessários; a data de início, a descrição do projeto e o GUID de EPT são opcionais.</span><span class="sxs-lookup"><span data-stu-id="30fcf-171">The project GUID and name are required; the start date, project description, and EPT GUID are optional.</span></span> 
  
<span data-ttu-id="30fcf-172">Depois de configurar as novas propriedades do projeto, o método **Projects.Add** adiciona o projeto à coleção **Projects**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-172">After setting the new project properties, the **Projects.Add** method adds the project to the **Projects** collection.</span></span> <span data-ttu-id="30fcf-173">Para salvar e publicar o projeto, você deve chamar o método **Projects.Update** para enviar uma mensagem à fila do Project Server e criar o projeto.</span><span class="sxs-lookup"><span data-stu-id="30fcf-173">To save and publish the project, you must call the **Projects.Update** method to send a message to the Project Server queue and create the project.</span></span> 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a><span data-ttu-id="30fcf-174">Procedimento 4.</span><span class="sxs-lookup"><span data-stu-id="30fcf-174">Procedure 4.</span></span> <span data-ttu-id="30fcf-175">Para definir as propriedades do novo projeto, criar e publicar o projeto</span><span class="sxs-lookup"><span data-stu-id="30fcf-175">To set the new project properties, create the project, and publish the project</span></span>

1. <span data-ttu-id="30fcf-176">Adicione o método **CreateTestProject** à classe de **Program**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-176">Add the **CreateTestProject** method to the **Program** class.</span></span> <span data-ttu-id="30fcf-177">O código a seguir cria e publica um projeto, mas não aguarda a conclusão do trabalho da fila.</span><span class="sxs-lookup"><span data-stu-id="30fcf-177">The following code creates and publishes a project, but does not wait for the queue job to complete.</span></span> 
    
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

2. <span data-ttu-id="30fcf-178">Substitua o comentário `/* Add code here to wait for the queue. */` pelo seguinte código para aguardar pelo trabalho da fila.</span><span class="sxs-lookup"><span data-stu-id="30fcf-178">Replace the  `/* Add code here to wait for the queue. */` comment with the following code to wait for the queue job.</span></span> <span data-ttu-id="30fcf-179">A rotina espera a quantidade máxima de segundos especificados em **timeoutSeconds** ou continua se o trabalho da fila for concluído antes do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="30fcf-179">The routine waits a maximum of the specified **timeoutSeconds** number of seconds, or proceeds if the queue job completes before the timeout.</span></span> <span data-ttu-id="30fcf-180">Para obter os possíveis estados de trabalho da fila, consulte [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx).</span><span class="sxs-lookup"><span data-stu-id="30fcf-180">For possible queue job states, see [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) .</span></span> 
    
   <span data-ttu-id="30fcf-181">Chamar os métodos **Load** e **ExecuteQuery** para o objeto **QueueJob** é opcional.</span><span class="sxs-lookup"><span data-stu-id="30fcf-181">Calling the **Load** method and the **ExecuteQuery** method for the **QueueJob** object is optional.</span></span> <span data-ttu-id="30fcf-182">Se o objeto **QueueJob** não iniciar ao chamar o método **WaitForQueue**, o Project Server o inicia.</span><span class="sxs-lookup"><span data-stu-id="30fcf-182">If the **QueueJob** object is not initialized when you call the **WaitForQueue** method, Project Server initializes it.</span></span> 
    
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

## <a name="listing-the-published-projects"></a><span data-ttu-id="30fcf-183">Lista de projetos publicados</span><span class="sxs-lookup"><span data-stu-id="30fcf-183">Listing the published projects</span></span>
<span data-ttu-id="30fcf-184"><a name="pj15_GettingStartedCSOM_ListingPublished"> </a></span><span class="sxs-lookup"><span data-stu-id="30fcf-184"></span></span>

<span data-ttu-id="30fcf-185">O método **ListPublishedProjects** obtém a coleção de todos os projetos publicados no Project Web App.</span><span class="sxs-lookup"><span data-stu-id="30fcf-185">The **ListPublishedProjects** method gets the collection of all projects that are published in Project Web App.</span></span> <span data-ttu-id="30fcf-186">Se o trabalho de fila que cria um projeto no procedimento 4 não for concluído com êxito ou se o tempo limite terminar, o novo projeto não será incluído na coleção **Projects**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-186">If the queue job that creates a project in Procedure 4 does not complete successfully or times out, the new project is not included in the **Projects** collection.</span></span> 
  
### <a name="procedure-5-to-list-the-published-projects"></a><span data-ttu-id="30fcf-187">Procedimento 5.</span><span class="sxs-lookup"><span data-stu-id="30fcf-187">Procedure 5.</span></span> <span data-ttu-id="30fcf-188">Para listar os projetos publicados</span><span class="sxs-lookup"><span data-stu-id="30fcf-188">To list the published projects</span></span>

1. <span data-ttu-id="30fcf-189">Adicione o método **ListPublishedProjects** à classe **Program**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-189">Add the **ListPublishedProjects** method to the **Program** class.</span></span> 
    
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

2. <span data-ttu-id="30fcf-190">Configure o valor correto para a URL do Project Web App, compile o aplicativo **QueueCreateProject** e teste o aplicativo conforme o procedimento 6.</span><span class="sxs-lookup"><span data-stu-id="30fcf-190">Set the correct value for your Project Web App URL, compile the **QueueCreateProject** application, and then test the application as in Procedure 6.</span></span> 
    
## <a name="testing-the-queuecreateproject-application"></a><span data-ttu-id="30fcf-191">Teste do aplicativo QueueCreateProject</span><span class="sxs-lookup"><span data-stu-id="30fcf-191">Testing the QueueCreateProject application</span></span>
<span data-ttu-id="30fcf-192"><a name="pj15_GettingStartedCSOM_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="30fcf-192"></span></span>

<span data-ttu-id="30fcf-193">Execute o aplicativo **QueueCreateProject** em uma instância de teste do Project Web App, especialmente se o Project Server estiver instalado em uma máquina virtual; o aplicativo pode precisar de mais tempo para executar do que o limite de tempo padrão da fila de dez segundos.</span><span class="sxs-lookup"><span data-stu-id="30fcf-193">When you first run the **QueueCreateProject** application on a test instance of Project Web App, especially if Project Server is installed on a virtual machine, the application may require more time to run than the default queue timeout of ten seconds.</span></span> 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a><span data-ttu-id="30fcf-194">Procedimento 6.</span><span class="sxs-lookup"><span data-stu-id="30fcf-194">Procedure 6.</span></span> <span data-ttu-id="30fcf-195">Para testar o aplicativo QueueCreateProject</span><span class="sxs-lookup"><span data-stu-id="30fcf-195">To test the QueueCreateProject application</span></span>

1. <span data-ttu-id="30fcf-196">Abra a janela **Propriedades de QueueCreateProject**, selecione a guia **Depurar** e adicione os seguintes argumentos de linha de comando à seção **Opções de inicialização**: `-n "Test proj 1" -t 20`</span><span class="sxs-lookup"><span data-stu-id="30fcf-196">Open the **QueueCreateProject Properties** window, select the **Debug** tab, and then add the following command-line arguments in the **Start Options** section:  `-n "Test proj 1" -t 20`</span></span>
    
   <span data-ttu-id="30fcf-197">Execute o aplicativo (por exemplo, pressione **F5**).</span><span class="sxs-lookup"><span data-stu-id="30fcf-197">Run the application (for example, press **F5**).</span></span> <span data-ttu-id="30fcf-198">Se o valor do tempo limite for grande o suficiente, o aplicativo mostrará o seguinte resultado (se houver outros projetos publicados em sua instância do Project Web App, eles também serão mostrados):</span><span class="sxs-lookup"><span data-stu-id="30fcf-198">If the timeout value is long enough, the application shows the following output (if other published projects exist in your Project Web App instance, they will also be shown):</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. <span data-ttu-id="30fcf-199">Execute outro teste com os seguintes argumentos de linha de comando para usar o tempo limite padrão de 10 segundos da fila: `-n "Test proj 1"`</span><span class="sxs-lookup"><span data-stu-id="30fcf-199">Run another test with the following command-line arguments, to use the default 10-second queue timeout: `-n "Test proj 1"`</span></span>
    
   <span data-ttu-id="30fcf-200">Como Test proj 1 já existe, o aplicativo mostra o resultado a seguir.</span><span class="sxs-lookup"><span data-stu-id="30fcf-200">Because Test proj 1 already exists, the application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. <span data-ttu-id="30fcf-201">Execute outro teste com os seguintes argumentos de linha de comando para usar o tempo limite padrão de 10 segundos da fila: `-n "Test proj 2"`</span><span class="sxs-lookup"><span data-stu-id="30fcf-201">Run another test with the following command-line arguments, to use the default 10-second queue timeout:  `-n "Test proj 2"`</span></span>
    
   <span data-ttu-id="30fcf-202">O aplicativo **QueueCreateProject** cria e publica o projeto chamado Test proj 2.</span><span class="sxs-lookup"><span data-stu-id="30fcf-202">The **QueueCreateProject** application creates and publishes the project named Test proj 2.</span></span> 
    
4. <span data-ttu-id="30fcf-203">Execute outro teste com os seguintes argumentos de linha de comando e configure o tempo limite para ser curto demais para permitir a conclusão do trabalho da fila: `-n "Test proj 3" -t 1`</span><span class="sxs-lookup"><span data-stu-id="30fcf-203">Run another test with the following command-line arguments, and set the timeout to be too short for the queue job to finish:  `-n "Test proj 3" -t 1`</span></span>
    
   <span data-ttu-id="30fcf-204">Como o tempo limite da fila é muito curto, o projeto não é criado.</span><span class="sxs-lookup"><span data-stu-id="30fcf-204">Because the queue timeout is too short, the project is not created.</span></span> <span data-ttu-id="30fcf-205">O aplicativo mostra o resultado a seguir.</span><span class="sxs-lookup"><span data-stu-id="30fcf-205">The application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. <span data-ttu-id="30fcf-206">Modifique o código para que o aplicativo não espere pelo trabalho da fila.</span><span class="sxs-lookup"><span data-stu-id="30fcf-206">Modify the code so that the application does not wait for the queue job.</span></span> <span data-ttu-id="30fcf-207">Por exemplo, retire o comentário do código que aguarda a fila, exceto a linha `projCreated = true`, da maneira a seguir.</span><span class="sxs-lookup"><span data-stu-id="30fcf-207">For example, comment out the code that waits for the queue, except for the  `projCreated = true` line, as follows.</span></span> 
    
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

6. <span data-ttu-id="30fcf-208">Compile novamente o aplicativo e execute outro teste com os seguintes argumentos de linha de comando: `-n "Test proj 4"`</span><span class="sxs-lookup"><span data-stu-id="30fcf-208">Recompile the application and run another test with the following command-line arguments:  `-n "Test proj 4"`</span></span>
    
   <span data-ttu-id="30fcf-209">Como o comentário da rotina **WaitForQueue** foi retirado, o aplicativo não usa o valor do tempo limite padrão.</span><span class="sxs-lookup"><span data-stu-id="30fcf-209">Because the **WaitForQueue** routine is commented out, the application does not use the default timeout value.</span></span> <span data-ttu-id="30fcf-210">Mesmo que o aplicativo não espere pela fila, ele poderá mostrar Test proj 4, se a ação Publicar no Project Server for rápida o suficiente.</span><span class="sxs-lookup"><span data-stu-id="30fcf-210">Even though the application does not wait for the queue, it may show Test proj 4, if the publish action in Project Server is fast enough.</span></span> 
    
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

<span data-ttu-id="30fcf-211">Atualize a página do Central de Projetos no Project Web App (`https://ServerName/ProjectServerName/Projects.aspx`) para mostrar os projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="30fcf-211">Refresh the Project Center page in Project Web App (`https://ServerName/ProjectServerName/Projects.aspx`), to show the published projects.</span></span> <span data-ttu-id="30fcf-212">A figura a seguir mostra os projetos de teste que foram publicados.</span><span class="sxs-lookup"><span data-stu-id="30fcf-212">The following figure shows that the test projects are published.</span></span>

<span data-ttu-id="30fcf-213">**Verificar projetos publicados no Project Web App**</span><span class="sxs-lookup"><span data-stu-id="30fcf-213">**Checking the published projects in Project Web App**</span></span>

<span data-ttu-id="30fcf-214">![Verificar projetos publicados no Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Verificar projetos publicados no Project Web App")</span><span class="sxs-lookup"><span data-stu-id="30fcf-214">![Checking the published projects in Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Checking the published projects in Project Web App")</span></span>
  
<span data-ttu-id="30fcf-215">O aplicativo de amostra **QueueCreateProject** mostra um exemplo comum para criar uma entidade de projeto com o CSOM usando a classe **ProjectCreationInformation**, como adicionar o projeto à coleção publicada, como aguardar um trabalho de fila usando o método **WaitForQueue** e como enumerar a coleção de projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="30fcf-215">The **QueueCreateProject** sample application shows a typical example of how to create a project entity with the CSOM by using the **ProjectCreationInformation** class, how to add the project to the published collection, how to wait for a queue job by using the **WaitForQueue** method, and how to enumerate the collection of published projects.</span></span> 
  
## <a name="complete-code-example"></a><span data-ttu-id="30fcf-216">Exemplo de código completo</span><span class="sxs-lookup"><span data-stu-id="30fcf-216">Complete code example</span></span>
<span data-ttu-id="30fcf-217"><a name="pj15_GettingStartedCSOM_CompleteCode"> </a></span><span class="sxs-lookup"><span data-stu-id="30fcf-217"></span></span>

<span data-ttu-id="30fcf-218">Apresentamos a seguir o código completo para o aplicativo de exemplo **QueueCreateProject**.</span><span class="sxs-lookup"><span data-stu-id="30fcf-218">The following is the complete code for the **QueueCreateProject** sample application.</span></span> <span data-ttu-id="30fcf-219">A referência de classe [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) também inclui o código neste tópico.</span><span class="sxs-lookup"><span data-stu-id="30fcf-219">The [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) class reference also includes the code in this topic.</span></span> 
  
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
        private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
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

## <a name="see-also"></a><span data-ttu-id="30fcf-220">Confira também</span><span class="sxs-lookup"><span data-stu-id="30fcf-220">See also</span></span>

- [<span data-ttu-id="30fcf-221">Atualizações para desenvolvedores do Project 2013</span><span class="sxs-lookup"><span data-stu-id="30fcf-221">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md) 
- [<span data-ttu-id="30fcf-222">Modelo de objeto no lado do cliente (CSOM) para o Project 2013</span><span class="sxs-lookup"><span data-stu-id="30fcf-222">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

