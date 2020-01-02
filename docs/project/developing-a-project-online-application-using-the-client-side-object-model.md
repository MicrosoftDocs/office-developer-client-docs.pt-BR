---
title: Desenvolvimento de um aplicativo do Project Online usando o modelo de objeto do cliente
manager: lindalu
ms.date: 12/18/2019
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: 'Este artigo descreve o desenvolvimento de aplicativos do Microsoft Project Online usando o .NET Framework 4.0 e o CSOM. '
localization_priority: Priority
ms.openlocfilehash: 33ddafe2e3a75039bf55381524accf1a25692885
ms.sourcegitcommit: 55205b4ec1376713d31e75d195e031798fb2c6ad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/20/2019
ms.locfileid: "40825769"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model-csom"></a>Desenvolvimento de um aplicativo do Project Online usando o modelo de objeto do cliente (CSOM)

>[!NOTE] 
>Este artigo descreve o desenvolvimento de aplicativos do Microsoft Project Online para usar o CSOM. Recomendamos que você explore como desenvolver aplicativos usando o [novo Project para a Web](https://developer.microsoft.com/pt-BR/office/blogs/developing-applications-and-reports-using-the-new-project/).
  
## <a name="background"></a>Segundo plano

O Microsoft Project começou como um aplicativo da área de trabalho no início da década de 1990. Atualmente o Project é muito mais, o que se comprova por sua variedade:
  
- O Project Standard Edition é um aplicativo da área de trabalho executado como um aplicativo autônomo.
    
- O Project Professional Edition é um aplicativo da área de trabalho que pode interagir e compartilhar dados com um servidor em uma escala maior, além de ter as mesmas funcionalidades do Project Standard Edition.
    
- O Project Online é um serviço hospedado da Microsoft que oferece às empresas uma solução no nível de PMO para coordenar e gerenciar projetos, programas e portfólios. Diferente das edições da área de trabalho, o Project Online pode manter e controlar os detalhes do projeto durante a vigência dele. 
    
- O Project Server é um serviço hospedado pela empresa em que ela gerencia e protege o servidor contendo informações de projetos, programas e portfólios. O Project Server, por proteger o servidor internamente, oferece os recursos orientados a projetos, programas e portfólios do Project Online hospedado externamente com maior capacidade de personalização.
    
O Project Online tem três conjuntos de API online: CSOM (Modelo de Objeto do Cliente), JSOM (Modelo de Objeto do JavaScript) e REST (Transferência de Estado Representacional). 
  
- A implementação do .NET CSOM é a interface preferencial ao desenvolver aplicativos para Windows que interagem com locatários do Project Online. Entre os ambientes típicos de aplicativos voltados para o usuário estão os computadores Windows e os dispositivos Microsoft Surface. Aplicativos de back-end escritos com .NET CSOM podem se conectar a outros servidores como fontes de dados e lógicas corporativas que sejam externas ao Project Online. Solicitações de recuperação no Project Online usam um sistema de consulta equivalente ao LINQ que oferece diversas melhorias em relação às funções básicas de recuperação.
    
- A interface do JSOM (Modelo de Objeto do JavaScript) oferece suporte a navegadores para Suplementos do Project Online. Um suplemento é um aplicativo web que fica armazenado em um locatário do Project Online. Quando um usuário deseja executar um suplemento, o código do suplemento é baixado e executado no navegador do computador do usuário. 
    
- O modelo de REST/Odata proporciona uma comunicação com base em HTTP. Essa interface é recomendável para aplicativos que não estão em ambientes Windows. Pontos de extremidade de comunicações são objetos no site do PWA (Projeto de Aplicativo Web). Os resultados fornecem códigos de status HTTP normal.
    
Este artigo aborda um aplicativo que usa a interface do .NET CSOM.
  
## <a name="prerequisites"></a>Pré-requisitos

Comece com um sistema de base executando o Windows 10 e adicione os seguintes itens:
  
- .NET Framework 4.0 ou posterior – Use a estrutura completa. O site de download é https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- Visual Studio 2013 ou posterior – Qualquer edição é aceitável. A edição da comunidade do Visual Studio 2015 foi usada para desenvolver o aplicativo de exemplo. A edição da comunidade está disponível em https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.
    
- SDK dos Componentes de Clientes do SharePoint – O Project Online e o Project Server estão acima do SharePoint e dos assemblies do SharePoint. Os Componentes do Cliente do SharePoint são incluídos nas edições do Visual Studio Professional e Enterprise. Se você usar a edição Visual Studio Community, a versão mais recente do SDK de Ferramentas de Desenvolvedor do Office estará disponível no seguinte site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Uma conta do Project Online – Fornece acesso ao site de hospedagem. Confira mais informações sobre como obter uma conta do Project Online em https://products.office.com/en-us/Project/project-online-portfolio-management.
    
- Projetos no site de hospedagem que são preenchidos com informações
    
> [!NOTE]
> O .NET Framework padrão (4.0 ou posterior) é a estrutura correta a se usar. Não use o .NET Framework 4 Client Profile. 
  
## <a name="develop-the-application"></a>Desenvolver o aplicativo

Ao desenvolver um aplicativo de área de trabalho para o SharePoint, a interface preferida é o CSOM (Modelo de Objeto do Cliente) do Project. 
  
Você pode baixar os [exemplos de CSOM do Project](https://developer.microsoft.com/project/gallery/?filterBy=Samples,Project) na galeria de recursos do Project Developer no Centro de Desenvolvimento do Office.
  
Os dois primeiros tópicos abordam as questões básicas: a criação de um projeto do Visual Studio com namespaces apropriados e assemblies, e o acesso ao servidor de hospedagem. Os tópicos restantes lidam com a recuperação de informações por meio do CSOM, de um e de diversos objetos. 
  
Recuperar informações do host é um processo de duas ações nos aplicativos cliente. Primeiro o aplicativo especifica e envia uma ou mais solicitações de recuperação para o servidor. Depois o aplicativo emite uma notificação para o servidor executar as consultas enviadas. O servidor responde enviando os resultados da consulta para o cliente.
  
### <a name="set-up-the-visual-studio-project"></a>Configurar o projeto do Visual Studio

A instalação do aplicativo consiste em criar um novo projeto, vincular os assemblies apropriados e declarar os namespaces necessários. O Visual Studio apresenta vários tipos de projetos de desenvolvimento. 
  
#### <a name="select-a-visual-studio-project"></a>Selecionar um projeto do Visual Studio

1. Inicie o Visual Studio e selecione **Iniciar um Novo Projeto** na página inicial. 
    
   A caixa de diálogo Novo Projeto exibe modelos de aplicativos disponíveis e os campos de dados de qualquer modelo selecionado. 
    
2. Para esse aplicativo, especifique os itens a seguir. As palavras-chave da tela têm um atributo em negrito:
    
   1. nos modelos Instalados no painel esquerdo, selecione ** C#** => **Windows** => **Área de trabalho Clássica**. 
    
   2. Na parte superior do painel central, selecione **.NET Framework 4**. 
    
   3. Nos tipos de aplicativo no painel central, escolha **Aplicativo do Console**. 
    
   4. Na seção inferior, especifique o nome e o local do projeto e o nome da solução. 
    
   5. Também na seção inferior, marque a caixa **Criar diretório para a solução**. 
    
3. Clique em **OK** para criar o projeto inicial. 
    
#### <a name="add-assemblies"></a>Adicionar assemblies

A solução VS precisa do assembly ProjectServerClient do SDK do Project 2013, de um conjunto de assemblies do SDK do SharePoint e do assembly .NET Framework System.Security.
  
1. No Explorador de Soluções do VS, clique na entrada Referências e selecione **Adicionar Referência...** no menu de atalho. 
    
2. Verifique a **Microsoft.ProjectServer.Client.dll**. 
    
   Se necessário, clique no botão **Procurar...** na parte inferior da caixa de diálogo e navegue até o diretório de instalação do SDK do Project 2013 para localizar o assembly. 
    
3. Clique em **OK**. 
    
4. Adicione o namespace ProjectServerClient ao arquivo .cs.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Adicione os assemblies de SDK do SharePoint 2013 usando o Console do Gerenciador de Pacotes NuGet. 
  
1. No menu Ferramentas do VS, clique nos seguintes menus: **Ferramentas =\> Gerenciador de Pacotes NuGet =\> Console do Gerenciador de Pacotes**. 
    
2. No Console do Gerenciador de Pacotes, insira o comando a seguir e pressione \<Enter\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   O **Console do Gerenciador de Pacotes** fornece uma descrição de resultados de comandos, e o Explorador de soluções do VS exibe assemblies do SharePoint nas referências do projeto. 
    
3. Adicione os namespaces ao arquivo .cs:
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

O assembly System.Security faz parte do .NET Framework e foi instalado com a estrutura. O aplicativo de exemplo precisa de mais um namespace que forneça uma cadeia de caracteres criptografada ao sistema de hospedagem para efetuar a autenticação. Depois de autenticado, o aplicativo pode acessar projetos no sistema de hospedagem. Adicione o namespace System.Security ao arquivo .cs desta maneira:
  
1. No Explorador de Soluções do VS, clique na entrada Referências e selecione **Adicionar Referência...** no menu de atalho. 
    
2. Selecione **Assemblies =\> Framework** no painel esquerdo da caixa de diálogo Gerenciador de Referências, depois marque **System.Security**. 
    
3. Clique em **OK**. 
    
4. Adicione o namespace System.Security ao arquivo .cs:
    
   ```cs
    using System.Security;
   ```

O início do arquivo .cs deve conter os seguintes namespaces:
  
- System
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>Conecte-se ao sistema de host

O Project Online é um aplicativo do SharePoint, assim, usar a autenticação do SharePoint é a abordagem correta. O fragmento de código a seguir prepara para acessar o ambiente hospedado.
  
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

Entre os preparativos para acessar o ambiente hospedado estão os seguintes itens:
  
1. Criar um objeto de contexto para projetos – ele está contido no código a seguir ao fragmento de código anterior. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   O contexto é herdado pelos outros componentes, permitindo que o sistema gerencie o contexto do modelo de objeto do Project.
    
2. Identificar o site do host – isso é feito no código a seguir ao fragmento de código anterior.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   Ao instanciar o contexto dos projetos, o aplicativo deve fornecer a raiz do conjunto de sites dos Projects. O aplicativo usa uma subcadeia de caracteres da URL da raiz dos Projects. Um instantâneo desse local é realçado com um retângulo vermelho na ilustração a seguir. A autenticação precisa da cadeia de caracteres desde o início pela subcadeia de caracteres "pwa". Na lista de códigos, o aplicativo usa a cadeia "https://XXXXXXXX.sharepoint.com/sites/pwa".
        
   ![Captura de tela da URL do conjunto de sites dos Projects em uma borda vermelha.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Captura de tela da URL do conjunto de sites dos Projects em uma borda vermelha.")
  
3. Definir a senha em uma cadeia de caracteres segura – isso é feito no código a seguir ao fragmento de código anterior.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   A conta de usuário e a senha são as credenciais para acessar o site do host. 
    
4. Adicionar a conta de usuário e senha na parte de credenciais do objeto de contexto – isso é feito no código a seguir ao fragmento de código anterior.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

O contexto de instâncias do projeto está pronto para uso.
  
### <a name="list-all-published-projects"></a>Listar todos os projetos publicados

O Project Online e o Project Server usam proxies para se comunicar com o servidor para criar, relatar, atualizar e excluir operações (CRUD). O host/servidor manipula as solicitações de maneira eficiente e faz o cliente executar as seguintes ações ao se comunicar com o servidor:
  
1. Estabelecer um contexto de comunicação. 
    
   O contexto é usado por conjunto de projetos, bem como outros objetos e coleções por herança, incluindo o conjunto de tarefas, conjunto de atribuições, o objeto estágio e os campos personalizados. 
    
2. Use o modelo de objeto para especificar um objeto, conjunto ou dados a recuperar.
    
   Esta etapa usa LINQ como uma consulta ou método. A especificação controla o que você recebe. Geralmente essa etapa é inserida no corpo do método de Carregamento (etapa 3). 
    
3. Carregue a especificação de recuperação da etapa anterior usando os métodos Load() ou LoadQuery().
    
   Para o carregamento de conjuntos e objetos, use Load(). Para consultas com cláusulas como "where" e "group", use LoadQuery(). 
    
4. Execute a solicitação usando o método de ExecuteQuery().
    
   O método ExecuteQuery() notifica o host de que a consulta ou consultas estão prontas para executar. Quando o host recebe a notificações, executa as consultas e envia os resultados ao cliente. 
    
Com as informações no cliente, o aplicativo pode usá-la. O fragmento de código a seguir percorre projetos publicados e marca o Id e o Nome de cada projeto publicado no host.
  
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

### <a name="make-a-request"></a>fazer uma solicitação

Usando as ações do fragmento de código anterior, o aplicativo recupera a lista de projetos na conta especificada do site de hospedagem. 
  
1. ProjectContext está especificado nos projetos a listar. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Especifique o item a recuperar. 
    
   ```cs
    projContext.Load(projects);
   ```

   Ao simplesmente informar o conjunto, o servidor recupera o conjunto de projetos, preenchendo cada projeto com valores do conjunto padrão de propriedades. Acessar as propriedades que fazem parte do conjunto de propriedades padrão fornece resultados bem-sucedidos. Acessar as propriedades que não fazem parte do conjunto padrão resulta na exceção "Não inicializado".
    
3. Carregue a solicitação (projContext.Load).
    
   Isso faz parte da etapa anterior.
    
4. Execute a consulta (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Recuperar informações de projeto de alto nível

Propriedades que não sejam propriedades padrão devem ser especificadas na solicitação para o servidor. O próximo fragmento de código carrega o contexto do conjunto de projetos, como no exemplo anterior. Em seguida, a especificação solicita propriedades adicionais não padrão a incluir no resultado. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

A instrução de carregamento especifica o contexto de conjuntos de projetos e adiciona DataDeInício, Estágio e Fase ao resultado da consulta. As propriedades adicionais podem ser escalares, objetos ou conjuntos. Itens escalares podem ser acessados diretamente. Objetos e conjuntos exigem processamento adicional, como no próximo fragmento de código.
  
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

### <a name="retrieve-all-tasks-in-a-project"></a>recuperar todas as tarefas em um projeto

Cada projeto tem diversas tarefas. Portanto, extrair as tarefas de um projeto único consiste em:
  
1. estabelecer o contexto do conjunto de projetos.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Recupere informações de projeto, incluindo as propriedades da Tarefa.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Observe que o aplicativo está voltado a projetos publicados. O contexto do projeto atual publicado é pubProj. 
    
3. Estabeleça contexto para o conjunto de tarefas.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   A propriedade `pubProj.Tasks` referencia as tarefas do projeto publicado atual. 
    
4. Carregue a especificação para recuperar o conjunto de Tarefas, incluindo as propriedades não padrão apropriadas.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Execute a consulta para recuperar o conjunto de tarefas com as propriedades apropriadas.
    
   ```cs
    projContext.ExecuteQuery();
   ```

As informações agora são locais. O fragmento de código a seguir processa o conjunto de tarefas publicadas gravando as informações no console.
  
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

### <a name="access-information-at-multiple-levels"></a>acesse as informações em vários níveis

Cada tarefa pode ter uma ou mais pessoas (ou seja, recursos) contribuindo até sua conclusão. Os conjuntos de Tarefas e Recursos contêm essas informações para cada tarefa. 
  
O processamento consiste em:
  
1. obter um contexto para a tarefa do projeto.
    
2. Criar e carregar uma solicitação para as tarefas vinculadas à tarefa. 
    
3. Executar a consulta para as tarefas.
    
4. Criar e carregar a solicitação do recurso associado a uma tarefa individual. 
    
5. Executar a consulta para o recurso.
    
> [!NOTE] 
> - O conjunto de Atribuições é solicitado explicitamente nas informações do servidor porque não é uma propriedade padrão do conjunto de Tarefas. Como um conjunto, é feita uma consulta subsequente para obter o conjunto do servidor. 
> - O Recurso é um objeto. A consulta de uma atribuição inclui o nome do recurso associado à tarefa.
    
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

Saída das tarefas 52, 75 e 76 de um projeto:
  
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

### <a name="access-custom-enterprise-level-fields"></a>acessar campos personalizados de nível empresarial

Existem campos personalizados no Project Online. São os campos de nível empresarial que podem ser associados ao projeto individual. Esta seção descreve como acessar esses campos. 
  
Campos personalizados não estão incluídos no conjunto padrão de propriedades associadas a um projeto. Portanto, eles precisam de identificação explícita na especificação da recuperação. A visão de alto nível do processo consiste nos seguintes itens:
  
1. direcionar para o campo personalizado usando seu nome comum.
    
2. Recuperar o nome do campo personalizado interno.
    
3. Retornar ao contexto global e consultar o sistema usando o nome interno do campo personalizado.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>Direcionar para o campo personalizado, recuperar o nome interno e usá-lo para consultar o sistema

Essa tarefa especifica uma recuperação que usa uma propriedade não padrão com um detalhe adicional.
  
1. Inicie usando o contexto de projetos, como descrito no início deste artigo.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Adicione dois itens na solicitação de recuperação de conjunto de projetos além de quaisquer outras propriedades não padrão a recuperar:
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   A cláusula `p => p.IncludeCustomFields` identifica a necessidade de usar um objeto do projeto que ofereça suporte a campos personalizados. 
    
   A cláusula `p => p.IncludeCustomFields.CustomFields` solicita a inclusão de dados do campo personalizado no resultado da consulta. Essas informações são usadas depois que o nome do campo personalizado interno é recuperado. 
    
3. Carregue a solicitação.
    
   Isso faz parte da etapa anterior.
    
4. Execute a consulta.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Com essas informações no cliente, crie uma solicitação para recuperar campos personalizados associados ao projeto atual.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Localize o campo personalizado apropriado e recupere o nome do campo interno. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   O nome interno do campo personalizado é recuperado. Agora os itens de alto nível 1 e 2 estão concluídos.
    
7. Retorne ao contexto do projeto e recupere o valor do campo personalizado.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > O valor de campo personalizado é recuperado usando o nome interno como índice. 
  
A saída de três projetos que consistem em ID do projeto, Nome do projeto, nome do campo personalizado, nome interno do campo personalizado e valor do campo personalizado.
  
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

Para documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM, confira ao [Portal de desenvolvimento do Project](https://developer.microsoft.com/project).
    

