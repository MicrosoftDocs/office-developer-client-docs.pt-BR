---
title: Desenvolvendo um aplicativo do Project Online usando o modelo de objeto do cliente
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: Este artigo descreve o Microsoft Project Online desenvolvimento de aplicativos para aplicativos de área de trabalho usando o .NET Framework 4.0. O aplicativo descrito neste artigo recupera informações do servidor de hospedagem.
ms.openlocfilehash: a0a2b4042d4db127c56c5ba873ebe25418344571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771056"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a>Desenvolvendo um aplicativo do Project Online usando o modelo de objeto do cliente

Este artigo descreve o Microsoft Project Online desenvolvimento de aplicativos para aplicativos de área de trabalho usando o .NET Framework 4.0. O aplicativo descrito neste artigo recupera informações do servidor de hospedagem. 
  
## <a name="background"></a>Background

Microsoft Project iniciado como aplicativo da área de trabalho da década de 1990 antecipado. Atualmente, o projeto é muito mais, como confirmar suas diversas variedades:
  
- Project standard edition é um aplicativo de área de trabalho que é executado como um aplicativo autônomo.
    
- Edição de Project professional é um aplicativo de desktop que pode interagir e compartilhar dados com um servidor em uma escala maior, bem como executar a funcionalidade encontrada no Project standard edition.
    
- Project Online é um serviço hospedado pela Microsoft oferece às empresas uma solução no nível PMO para coordenar e gerenciar projetos, programas e portfólios. Uma oferta de diferente que as edições da área de trabalho, o Project Online pode manter e rastrear detalhes do projeto em toda a duração de um projeto. 
    
- Project Server é um serviço hospedado enterprise no qual a empresa gerencia e protege o servidor que contém o projeto, programa e informações de portfólio. Project Server, em virtude protegendo o servidor interno, oferece o projeto, programa e recursos de portfólio orientada a do hospedado externamente Project Online com uma maior capacidade de personalização.
    
Project Online tem três conjuntos de APIs online: modelo de objeto do cliente (CSOM), o modelo de objeto JavaScript (JSOM) e transferência de estado representacional (REST). 
  
- A implementação do .NET CSOM é a interface preferida ao desenvolver aplicativos do Windows que interagem com locatários Project Online. Ambientes típicos para aplicativos centrados no usuário incluem áreas de trabalho do Windows e dispositivos Microsoft Surface. Aplicativos back-end grafados com .NET CSOM podem se conectar a outros servidores para fontes de dados e lógica corporativos que são externos para o Project Online. Solicitações de recuperação para o Project Online usam um sistema de consulta do tipo LINQ que oferece vários aprimoramentos em relação de funções de recuperação básica.
    
- A interface do modelo de objeto JavaScript (JSOM) oferece suporte a vários navegadores para suplementos Project Online. Um suplemento é um aplicativo web que é armazenado no Project Online inquilino. Quando um usuário quiser executar um add-in, o código para o suplemento baixa e executa no navegador na máquina do usuário. 
    
- O modelo do REST/Odata fornece comunicação baseada em HTTP, esta interface é recomendado para aplicativos em ambientes de não-Windows. Pontos de extremidade de comunicação são os objetos no site do Project Web Application (PWA). Resultados fornecem os códigos de status HTTP normais.
    
Este artigo concentra-se em um aplicativo que usa a interface CSOM do .NET.
  
## <a name="prerequisites"></a>Pré-requisitos

Comece com um sistema de base executando Windows 10 e, em seguida, adicione os seguintes itens:
  
- .NET framework 4.0 ou posterior – usam o framework completo. O site de download está https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.
    
- Visual Studio 2013 ou posterior – qualquer edição é aceitável. A edição de comunidade do Visual Studio de 2015 foi usada para desenvolver o aplicativo de amostra. A edição de comunidade está disponível em https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.
    
- Componentes de cliente do SharePoint SDK – Project Online e Project Server ficam na parte superior do SharePoint e o SharePoint assemblies. Os componentes de cliente do SharePoint estão incluídos no Visual Studio Professional e Enterprise Edition. Se você usar a edição da comunidade do Visual Studio, a versão mais recente do Office Developer Tools SDK está disponível no seguinte site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Uma conta de Project Online fornece acesso ao site de hospedagem. Para obter mais informações sobre como adquirir uma conta do Project Online, consulte https://products.office.com/en-us/Project/project-online-portfolio-management.
    
- Projetos no site de hospedagem que são preenchidos com informações
    
> [!NOTE]
> O padrão (4.0 ou posterior) do .NET Framework é o correto framework usar. Não use o .NET Framework 4 Client Profile. 
  
## <a name="develop-the-application"></a>Desenvolver o aplicativo

Desenvolver um aplicativo de área de trabalho para o SharePoint, a interface preferencial é o modelo de objeto do lado do projeto cliente (CSOM). 
  
Você pode baixar o exemplo completo em https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.
  
Os dois primeiros tópicos cobrem problemas básicos: Criando um projeto do Visual Studio com namespaces apropriados e assemblies e acessando o servidor de hospedagem. Os tópicos restantes lidam com Recuperando informações por meio de CSOM, de um e muitos objetos. 
  
Recuperar informações do host é um processo de ação de dois de aplicativos do cliente. Primeiro, o aplicativo especifica e envia uma ou mais solicitações de recuperação para o servidor. Em segundo lugar, o aplicativo emite uma notificação para o servidor para executar as consultas enviadas. O servidor responde enviando os resultados da consulta para o cliente.
  
### <a name="set-up-the-visual-studio-project"></a>Configurar o projeto do Visual Studio

A instalação do aplicativo consiste em criar um novo projeto, vinculando os assemblies apropriados e declarando os namespaces necessários. O Visual Studio apresenta vários tipos de projetos de desenvolvimento. 
  
#### <a name="select-a-visual-studio-project"></a>Selecione um projeto do Visual Studio

1. Inicie o Visual Studio e selecione **Iniciar um novo projeto** , na página inicial. 
    
   A caixa de diálogo Novo projeto exibe modelos de aplicativos disponíveis e campos de dados para qualquer modelo selecionado. 
    
2. Para este aplicativo, especifique os seguintes itens. Palavras-chave, encontradas na tela tem um atributo negrito:
    
   1. A partir de modelos de Installed no painel esquerdo, selecione **c#** => **Windows** => **desktop clássico**. 
    
   2. Na parte superior do painel central, selecione o **.NET Framework 4**. 
    
   3. A partir de tipos de aplicativos, no painel central, escolha o **Aplicativo de Console**. 
    
   4. Na seção inferior, especifique um nome e local para o projeto e o nome da solução. 
    
   5. Também na seção inferior, marque a caixa de **criar diretório para a solução** . 
    
3. Clique em **Okey** para criar o projeto inicial. 
    
#### <a name="add-assemblies"></a>Adicionar assemblies

A solução VERSUS precisa o assembly ProjectServerClient do projeto 2103 SDK, algumas de assemblies do SDK do SharePoint e o assembly System. Security do .NET Framework.
  
1. No Solution Explorer VERSUS, com o botão direito na entrada referências e selecione **Adicionar referência...** no menu de atalho. 
    
2. Verifique o **Microsoft.ProjectServer.Client.dll**. 
    
   Se necessário, clique no que **Procurar...** botão na parte inferior da caixa de diálogo e navegue até o diretório de instalação do SDK do Project 2013 para localizar o assembly. 
    
3. Clique em **OK**. 
    
4. Adicione o namespace do cliente PrjoctServer ao arquivo. cs.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Adicione os assemblies do SDK do SharePoint 2013 usando o Console do Gerenciador de pacotes do NuGet. 
  
1. No menu Ferramentas do VS, clique nos seguintes menus: **ferramentas =\> NuGet Package Manager =\> Package Manager Console**. 
    
2. No Console do Gerenciador de pacotes, digite o seguinte comando e pressione \<ENTER\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   O **Console do Gerenciador de pacote** fornece uma descrição dos resultados do comando; e, então, VERSUS Solution Explorer exibe os assemblies do SharePoint nas referências de projeto. 
    
3. Adicione os espaços para nome para o arquivo. cs:
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

O assembly System. Security faz parte do .NET Framework e foi instalado com o framework. O aplicativo de amostra precisa mais um namespace que fornece uma cadeia de caracteres criptografada para o sistema de hospedagem para autenticação. Uma vez autenticado, o aplicativo pode acessar os projetos no sistema de hospedagem. Adicione o namespace System. Security ao arquivo. cs desta forma:
  
1. No Solution Explorer VERSUS, com o botão direito na entrada referências e selecione **Adicionar referência...** no menu de atalho. 
    
2. Selecione **Assemblies =\> Framework** no painel à esquerda da caixa de diálogo Gerenciador de referências, verifique se **System. Security**. 
    
3. Clique em **OK**. 
    
4. Adicione o namespace System. Security ao arquivo. cs:
    
   ```cs
    using System.Security;
   ```

O início do arquivo. cs deve conter os seguintes namespaces:
  
- System
    
- System.Collections.Generic
    
- System. Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System. Security
    
### <a name="connect-to-the-host-system"></a>Conectar ao sistema de host

Project Online é um aplicativo do SharePoint, portanto, usando a autenticação do SharePoint é a abordagem correta. O fragmento de código a seguir se prepara para acessar o ambiente hospedado.
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

Preparações para acessar o ambiente hospedado incluem os seguintes itens:
  
1. Crie um objeto de contexto para os projetos – isso está contido no código a seguir do fragmento de código anterior. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   O contexto é herdado por outros componentes, permitindo que o sistema gerenciar o contexto do modelo de objeto do projeto.
    
2. Identificar o site do host--isso é feito no código a seguir no fragmento de código anterior.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   Ao instanciar o contexto de projetos, o aplicativo precisa fornecer a raiz do conjunto de sites de projetos. O aplicativo usa uma subcadeia de caracteres da URL da raiz dos projetos. Um instantâneo deste local é realçado com um retângulo vermelho na ilustração a seguir. A autenticação precisa a cadeia de caracteres de seu início por meio de subcadeia de caracteres "pwa". Na listagem de código, o aplicativo usa a cadeia de caracteres "https://XXXXXXXX.sharepoint.com/sites/pwa".
        
   ![Captura de tela da URL do conjunto de sites de projetos dentro de uma borda vermelha.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Conjunto dentro de uma borda vermelha de sites de captura de tela da URL dos projetos")
  
3. Colocar a senha em uma cadeia de caracteres segura--isso é feito no código a seguir no fragmento de código anterior.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   A conta de usuário e senha são as credenciais para acessar o site do host. 
    
4. Adicionar a conta de usuário e senha para a parte de credenciais do objeto contexto – isso é feito no código a seguir no fragmento de código anterior.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

O contexto de projeto instanciadas está pronto para uso.
  
### <a name="list-all-published-projects"></a>Listar projetos publicados tudo

Project Online e ProjectServer usam proxies para se comunicar com o servidor para criar, relatório, atualizar e excluir operações (CRUD). Servidor/host processa solicitações de maneira eficiente e tem o cliente a executar as seguintes ações na comunicação com o servidor:
  
1. Estabelece um contexto para comunicação. 
    
   O contexto é usado pelo conjunto de projetos, bem como outros objetos e coleções por meio de herança, incluindo a coleção tasks, coleção assignments, o objeto stage e campos personalizados. 
    
2. Use o modelo de objeto para especificar um objeto, coleção ou dados a serem recuperados.
    
   Esta etapa usa LINQ como uma consulta ou como um método. A especificação controla o que você recebe. Muitas vezes, esta etapa é incorporada como o corpo do método Load (etapa 3). 
    
3. Carregar a especificação de recuperação da etapa anterior usando o método Load () ou LoadQuery().
    
   Para carregar os objetos e coleções, use Load (). Para consultas com cláusulas como "where" e "grupo", use LoadQuery(). 
    
4. Execute a solicitação usando o método ExecuteQuery ().
    
   O método ExecuteQuery () notifica o host que estão prontas para execução da consulta ou consultas. Depois que o host recebe uma notificação, ela executa as consultas e envia os resultados para o cliente. 
    
Com as informações no cliente, o aplicativo pode usá-lo. O fragmento de código a seguir percorre os projetos publicados e imprime a Id e o nome para cada projeto publicado no host.
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

Saída:
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>Fazer uma solicitação

Usando as ações de fragmento de código anterior, o aplicativo recupera a lista de projetos na conta especificada no site de hospedagem. 
  
1. O ProjectContext for especificado para listar os projetos. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Especifique o item a ser recuperado. 
    
   ```cs
    projContext.Load(projects);
   ```

   Por informando apenas a coleção, o servidor recupera a coleção de projetos, preenchendo a cada projeto com valores para o conjunto de propriedades padrão. Acesso às propriedades que fazem parte do conjunto de propriedades padrão concede resultados bem-sucedidos. Acesso às propriedades que não fazem parte do padrão definir resultados em uma exceção "Não inicializado".
    
3. Carregar a solicitação (projContext.Load).
    
   Isso é parte da etapa anterior.
    
4. Executa a consulta (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Recuperar informações de projeto de alto nível

Propriedades que não são propriedades padrão devem ser especificadas na solicitação ao servidor. O próximo fragmento de código carrega o contexto do conjunto de projetos do exemplo anterior. Em seguida, a especificação solicita propriedades adicionais de não-padrão para incluir no resultado. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

A instrução de carga Especifica o contexto do conjunto de projetos e adiciona o StartDate, fase e estágio para o resultado da consulta. As propriedades adicionais podem ser escalares, objetos ou coleções. Escalares itens podem ser acessados diretamente. Objetos e coleções exigem processamento adicional, como o fragmento de código a seguir.
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

Saída dos três primeiros projetos:
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a>Recuperar todas as tarefas em um projeto

Cada projeto tem muitas tarefas. Portanto, desligar as tarefas para um único projeto consiste das seguintes opções:
  
1. Estabelece o contexto do conjunto de projetos.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Recupere as informações de projeto, incluindo as propriedades da tarefa.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Observe que o aplicativo está lidando com projetos publicados. O contexto para o projeto publicado atual é pubProj. 
    
3. Estabelece o contexto de coleção Tasks.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   O `pubProj.Tasks` propriedade referencia as tarefas do projeto atual publicado. 
    
4. Carregar a especificação para recuperar o conjunto de tarefa, incluindo as propriedades adequadas de não-padrão.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Executa a consulta para recuperar a coleção de tarefa com as propriedades adequadas.
    
   ```cs
    projContext.ExecuteQuery();
   ```

Agora, a informação é local. O fragmento de código a seguir processa a coleção tasks publicado escrevendo as informações no console.
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

Saída de tarefas para um projeto:
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a>Informações de acesso em vários níveis

Cada tarefa pode ter uma ou mais pessoas (também conhecido como recurso) contribuindo rumo à sua conclusão. Os conjuntos de recursos e atribuições contenham essas informações para cada tarefa. 
  
O processamento consiste no seguinte:
  
1. Obtendo um contexto para a tarefa do projeto.
    
2. Crie uma solicitação e carregar a solicitação para as atribuições vinculadas à tarefa. 
    
3. Executa a consulta para as atribuições.
    
4. Crie uma solicitação e carregar a solicitação para o recurso associado a uma atribuição individual. 
    
5. Executa a consulta para o recurso.
    
> [!NOTE] 
> - A coleção Assignments é solicitada explicitamente as informações do servidor porque ele não é uma propriedade padrão da coleção Tasks. Como um conjunto, será feita uma consulta subsequente retire o conjunto do servidor. 
> - O recurso é um objeto. A consulta para uma atribuição inclui o nome do recurso associado à atribuição.
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

Saída para tarefas 52, 75 e 76 de um projeto:
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a>Campos personalizados de nível empresarial acesso

Campos personalizados existirem para o Project Online. Esses são os campos de nível empresarial que podem ser associados ao projeto individual. Esta seção descreve como acessar esses campos. 
  
Campos personalizados não são incluídos no conjunto padrão das propriedades associadas a um projeto. Portanto, elas precisam identificação explícita na especificação da recuperação. O modo de exibição de alto nível do processo consiste dos seguintes itens:
  
1. Túnel para o campo personalizado usando seu nome comum.
    
2. Recupere o nome interno do campo personalizado.
    
3. Volte para o contexto global e o sistema utilizando o nome interno do campo personalizado de consulta.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>Campo personalizado de túnel, recuperar seu nome interno e utilizou para o sistema de consulta

Essa tarefa especifica uma recuperação que usa uma propriedade de não-padrão com um detalhe adicionado.
  
1. Comece usando o contexto de projetos, conforme descrito no início deste artigo.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Adicione dois itens para a solicitação de recuperação de conjunto de projetos além de quaisquer outras propriedades de não-padrão para recuperar:
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   O `p => p.IncludeCustomFields` cláusula identifica a necessidade de usar um objeto de projeto que ofereça suporte a campos personalizados. 
    
   O `p => p.IncludeCustomFields.CustomFields` cláusula solicita a inclusão de dados de campo personalizado no resultado da consulta. Essa informação é usada após o nome interno de campo personalizado é recuperado. 
    
3. Carregar a solicitação.
    
   Isso é parte da etapa anterior.
    
4. Execute a consulta.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Com essas informações no cliente, crie uma solicitação para recuperar os campos personalizados associados ao projeto atual.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Localize o campo personalizado apropriado e recuperar o nome interno do campo. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   O nome interno do campo personalizado é recuperado. Itens de alto nível 1 e 2 agora estão concluídas.
    
7. Volte para o contexto de projeto e recuperar o valor do campo personalizado.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > O valor do campo personalizado é recuperado usando o nome interno como um índice. 
  
Saída de três projetos, consistindo em ID do projeto, nome do projeto, nome do campo personalizado, nome interno de campo personalizado e valor do campo personalizado.
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a>Confira também

Para documentação e exemplos relacionados ao Project Online e desenvolvimento de aplicativos usando CSOM, consulte o [Portal de desenvolvimento do Project](http://dev.office.com/project.aspx).
    

