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
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Introdução ao Project Server CSOM e .NET

Você pode usar o modelo de objeto do cliente do Project Server 2013 (CSOM) para desenvolver soluções do Project Online e no local com o .NET Framework 4. Este artigo descreve como criar um aplicativo de console que usa o CSOM para criar e publicar projetos. Após a publicação de um projeto, o aplicativo aguarda o serviço de fila do Project Server concluir com a ação Publicar e, em seguida, lista os projetos publicados.
  
Para obter uma introdução geral do Project Server CSOM, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md). Para tópicos de referência no namespace CSOM, consulte [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Criando um projeto CSOM no Visual Studio
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Você pode usar o Visual Studio 2010 ou Visual Studio 2012 para desenvolver soluções que usam o Project Server CSOM. O Project Server CSOM inclui três assemblies para o desenvolvimento de aplicativos clientes, aplicativos do Microsoft Silverlight e Windows Phone 8 aplicativos usando o .NET Framework 4. O CSOM também inclui um arquivo de JavaScript para o desenvolvimento de aplicativos web, conforme descrito em [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Você pode copiar o assembly CSOM que você precisa a partir de computador do Project Server ou o download do SDK do Project 2013 para um computador remoto de desenvolvimento. O aplicativo de console **QueueCreateProject** descrita neste tópico não é um aplicativo Silverlight ou um aplicativo do Windows Phone 8, portanto é necessário o assembly Microsoft.ProjectServer.Client.dll. Como o CSOM é independente do baseado em ASMX ou WCF Project Server Interface (PSI), você não precisará definir referências de serviço para a PSI ou usar o namespace **Microsoft.Office.Project.Server.Library** . 
  
O aplicativo de **QueueCreateProject** usa argumentos de linha de comando para o nome do projeto para criar e para o limite de tempo limite da fila. No procedimento 1, você cria o aplicativo de console básica, adicione uma rotina para analisar a linha de comando e adicionar uma mensagem de uso, se houver erros na linha de comando. 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>Procedimento 1. Para criar um projeto CSOM no Visual Studio

1. Copie o assembly Microsoft.ProjectServer.Client.dll a partir do `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` pasta ao seu computador de desenvolvimento. Copie o assembly para uma pasta conveniente para outros Project Server e assemblies de referência do SharePoint que você usará, tais como `C:\Project\Assemblies`.
    
2. Copie o assembly Microsoft.SharePoint.Client.dll e o assembly Microsoft.SharePoint.Client.Runtime.dll da mesma pasta de origem para o seu computador de desenvolvimento. O assembly Microsoft.ProjectServer.Client.dll tem dependências nos assemblies do SharePoint relacionados.
    
3. No Visual Studio, crie um aplicativo de console do Windows e definir a estrutura de destino para o .NET Framework 4. Por exemplo, nomeie o aplicativo QueueCreateProject.
    
   > [!NOTE]
   > Se você esquecer definir o destino correto, depois que o projeto do Visual Studio cria, abra **As propriedades de QueueCreateProject** no menu **projeto** . Na guia **aplicativo** , na lista suspensa **framework de destino** , escolha o **.NET Framework 4**. Não use o **.NET Framework 4 Client Profile**. 
  
4. No Solution Explorer, defina referências a assemblies a seguir:
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. No arquivo Module. vb, edite o `using` instruções, da seguinte maneira. 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. Adicione métodos para analisar os argumentos de linha de comando para o nome do projeto e o número de segundos para o tempo limite da fila, mostrar informações de uso e sair do aplicativo. Substitua o corpo principal do código no arquivo Module. vb com o código a seguir.
    
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

## <a name="getting-the-project-context"></a>Obtendo o contexto de projeto
<a name="pj15_GettingStartedCSOM_GettingContext"> </a>

Desenvolvimento de CSOM requer o objeto **ProjectContext** a ser inicializado com a URL do Project Web App. O código no procedimento 2 usa a constante **pwaPath** . Se você planeja usar o aplicativo para várias instâncias do Project Web App, você poderia fazer **pwaPath** uma variável e adicione outro argumento da linha de comando. 
  
### <a name="procedure-2-to-get-the-project-context"></a>Procedimento 2. Para obter o contexto de projeto

1. Adicione as constantes de classe de **programa** e variáveis que usará o aplicativo **QueueCreateProject** . Além da URL do Project Web App, o aplicativo usa o nome do tipo de projeto corporativo padrão (EPT), o nome do projeto para criar e tempo limite máximo da fila em segundos. Nesse caso, a variável **timeoutSeconds** permite testar como vários valores para o tempo limite afetam o aplicativo. O objeto **ProjectContext** é o objeto principal para acessar o CSOM. 
    
   ```cs
    private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. Substituir o `/* Add calls to methods here to get the project context and create a project. */` comentário com o código a seguir. O objeto **Microsoft.ProjectServer.Client.ProjectContext** é inicializado com a URL do Project Web App. O método **CreateTestProject** e o método **ListPublishedProjects** são mostrados no procedimento 4 e 5 do procedimento. 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a>Obtendo um tipo de projeto corporativo
<a name="pj15_GettingStartedCSOM_GettingEPT"> </a>

O aplicativo de amostra **QueueCreateProject** explicitamente seleciona o EPT de projeto corporativo, para mostrar como um aplicativo pode selecionar o EPT para um projeto. Se as informações de criação do projeto não especificam o GUID EPT, um aplicativo usaria o EPT padrão. O método **GetEptUid** é usado pelo método **CreateTestProject** descrito no procedimento 4. 
  
O método **GetEptUid** consulta o objeto **ProjectContext** da coleção de **EnterpriseProjectTypes** onde o nome EPT é igual ao nome especificado. Depois de executar a consulta, a variável **eptUid** é definida como o GUID do primeiro objeto na coleção **eptList** **EnterpriseProjectType** . Como os nomes EPT são exclusivos, há apenas um objeto **EnterpriseProjectType** que tem o nome especificado. 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>3 do procedimento. Para obter o GUID de uma EPT para um novo projeto

- Adicione o método **GetEptUid** à classe de **programa** . 
    
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

Há várias maneiras para localizar o GUID EPT. A consulta mostrada no método **GetEptUid** é eficiente, pois ele baixa apenas o um objeto de **EnterpriseProjectType** que corresponde ao nome EPT. A seguinte rotina de alternativa é menos eficiente, porque ele baixa a lista completa de EPTs para o aplicativo cliente e itera através da lista. 

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

A seguinte rotina utiliza uma expressão de consulta e lambda LINQ para selecionar o objeto EPT, mas ainda downloads todos os objetos **EnterpriseProjectType** . 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>Definindo as informações de criação e publicação do projeto
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

O método **CreateTestProject** cria um objeto **ProjectCreationInformation** e especifica as informações necessárias para criar um projeto. O GUID do projeto e o nome for necessárias; a data de início, a descrição de projeto e o EPT GUID são opcionais. 
  
Depois de configurar as propriedades do novo projeto, o método **Projects.Add** adiciona o projeto para a coleção **Projects** . Para salvar e publicar o projeto, você deve chamar o método **Projects.Update** para enviar uma mensagem para a fila do Project Server e criar o projeto. 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>4 do procedimento. Para definir as propriedades do novo projeto, o projeto de criar e publicar o projeto

1. Adicione o método **CreateTestProject** à classe de **programa** . O código a seguir cria e publica um projeto, mas não espera até que o trabalho em fila ser concluída. 
    
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

2. Substituir o `/* Add code here to wait for the queue. */` comentário com o seguinte código para aguardar o trabalho em fila. A rotina aguarda máximo do número de segundos especificado **timeoutSeconds** ou continua se o trabalho em fila for concluída antes do tempo limite. Para estados de trabalho de fila possíveis, consulte [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) . 
    
   Chamar o método **Load** e o método **ExecuteQuery** para o objeto **QueueJob** é opcional. Se o objeto **QueueJob** não for inicializado quando você chama o método **WaitForQueue** , o Project Server inicializa a ele. 
    
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

## <a name="listing-the-published-projects"></a>Listar os projetos publicados
<a name="pj15_GettingStartedCSOM_ListingPublished"> </a>

O método **ListPublishedProjects** obtém a coleção de todos os projetos publicados no Project Web App. Se o trabalho em fila que cria um projeto no 4 do procedimento não for concluída com êxito ou se esgotar o tempo, o novo projeto não está incluído no conjunto de **projetos** . 
  
### <a name="procedure-5-to-list-the-published-projects"></a>Procedimento 5. Para listar os projetos publicados

1. Adicione o método **ListPublishedProjects** à classe de **programa** . 
    
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

2. Defina o valor correto para sua URL do Project Web App, compilar o aplicativo **QueueCreateProject** e, em seguida, o aplicativo como 6 do procedimento de teste. 
    
## <a name="testing-the-queuecreateproject-application"></a>Testando o aplicativo QueueCreateProject
<a name="pj15_GettingStartedCSOM_Testing"> </a>

Quando você executa o aplicativo **QueueCreateProject** pela primeira vez em uma instância de teste do Project Web App, especialmente se o Project Server está instalado em uma máquina virtual, o aplicativo pode exigir mais tempo para executar que o tempo limite da fila de padrão de dez segundos. 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>Procedimento 6. Para testar o aplicativo QueueCreateProject

1. Abrir a janela **Propriedades QueueCreateProject** , selecione a guia **Depurar** e adicione os seguintes argumentos de linha de comando na seção **Opções** de inicialização:`-n "Test proj 1" -t 20`
    
   Executar o aplicativo (por exemplo, pressione **F5**). Se o valor de tempo limite é grande o suficiente, o aplicativo mostra a seguinte saída (se existirem de outros projetos publicados na sua instância do Project Web App, eles serão também exibidos):
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. Execute o teste de outro com os seguintes argumentos de linha de comando, para usar o tempo limite padrão de 10 segundos fila:`-n "Test proj 1"`
    
   Porque já existe um teste proj 1, o aplicativo mostra a seguinte saída.
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. Execute o teste de outro com os seguintes argumentos de linha de comando, para usar o tempo limite padrão de 10 segundos fila:`-n "Test proj 2"`
    
   O aplicativo **QueueCreateProject** cria e publica o projeto chamado Test proj 2. 
    
4. Executar o teste outra com os seguintes argumentos de linha de comando e defina o tempo limite para ser muito curto para o trabalho em fila para concluir:`-n "Test proj 3" -t 1`
    
   Porque o tempo limite da fila for muito curto, o projeto não será criado. O aplicativo mostra a seguinte saída.
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. Modificar o código para que o aplicativo não espera até que o trabalho em fila. Por exemplo, comente o código que aguarda para a fila, exceto para o `projCreated = true` linha, da seguinte maneira. 
    
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

6. Recompilar o aplicativo e execute outro teste com os seguintes argumentos de linha de comando:`-n "Test proj 4"`
    
   Porque a rotina **WaitForQueue** foi comentada, o aplicativo não usa o valor de tempo limite padrão. Mesmo que o aplicativo não esperar por uma fila, ele poderá mostrar teste proj 4, se a ação de publicação no Project Server for rápida o bastante. 
    
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

Atualize a página da Central de projetos no Project Web App (`http://ServerName/ProjectServerName/Projects.aspx`), para mostrar os projetos publicados. A figura a seguir mostra que os projetos de teste são publicados.

**Verificando os projetos publicados no Project Web App**

![Verificando os projetos publicados no Project Web App] (media/pj15_GetStartedCSOMNET_pwa.gif "Verificando os projetos publicados no Project Web App")
  
O aplicativo de exemplo **QueueCreateProject** mostra um exemplo típico de como criar uma entidade de projeto com o CSOM, usando a classe **ProjectCreationInformation** , como adicionar o projeto à coleção publicada, como aguardar por um trabalho de fila usando o método **WaitForQueue** e como enumere a coleção de projetos publicados. 
  
## <a name="complete-code-example"></a>Exemplo de código completo
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

Este é o código completo para o aplicativo de exemplo **QueueCreateProject** . Referência de classe do [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) também inclui o código neste tópico. 
  
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

## <a name="see-also"></a>Confira também

- [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md) 
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)
    

