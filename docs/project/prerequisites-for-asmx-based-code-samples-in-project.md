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
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Pré-requisitos para amostras de código com base em ASMX no projeto

Saiba mais informações para ajudá-lo a criar projetos no Visual Studio usando as amostras de código com base em ASMX que estão incluídas nos tópicos de referência do Project Server Interface (PSI).
  
Muitos dos exemplos de código incluídos na [referência do serviço de web e de biblioteca de classe do Project Server 2013](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) foram criados para o Office Project 2007 SDK e usam um formato padrão para serviços web ASMX. As amostras ainda funcionam no Project Server 2013 e são projetadas para serem copiados para um aplicativo de console e executados como uma unidade completa. Exceções são observadas na amostra. 
  
Novos exemplos PSI no Project 2013 SDK seguem um formato que usa os serviços do Windows Communication Foundation (WCF). As amostras com base em ASMX também podem ser adaptadas para usar os serviços WCF. Este artigo mostra como usar as amostras com serviços web ASMX. Para obter informações sobre como usar as amostras com os serviços WCF, consulte [pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> A interface de serviço web ASMX de PSI foi preterido no Project Server 2013, mas ainda é suportado. Se o modelo de objeto do cliente (CSOM) inclui os métodos que seu aplicativo requer, novos aplicativos devem ser desenvolvidos com o CSOM. O CSOM permite que os aplicativos funcionar com o Project Online ou em uma instalação local do Project Server 2013. Caso contrário, se o aplicativo usa a PSI, ele deve usar a interface WCF, que é a tecnologia que a Microsoft recomenda para comunicações de rede. Aplicativos que usam a interface ASMX ou a interface WCF podem trabalhar somente para instalações locais do Project Server 2013. Para obter mais informações sobre o CSOM, consulte [arquitetura do Project Server 2013](project-server-2013-architecture.md) e [o modelo de objeto do lado do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Antes de executar os exemplos de código, você deve configurar o ambiente de desenvolvimento, configure o aplicativo e alterar valores de constantes genéricos para coincidir com o seu ambiente.
  
## <a name="setting-up-the-development-environment"></a>Configurar o ambiente de desenvolvimento
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Configurar um teste de sistema do Project Server**.
    
   Use um teste de sistema do Project Server sempre que você estiver desenvolvendo ou teste. Mesmo quando seu código funciona perfeitamente, dependências interproject, relatórios ou outros fatores ambientais podem causar consequências indesejadas. 
    
   > [!NOTE]
   > Certifique-se de que você é um usuário válido no servidor e verifique se você tem permissões suficientes para as chamadas PSI que usa seu aplicativo. O tópico de referência para cada método PSI inclui uma tabela de permissões do Project Server. Por exemplo, o método [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requer a permissão **NewProject** global e a permissão de **SaveProjectTemplate** . 
  
   Em alguns casos, você pode precisar fazer a depuração remota no servidor. Você também pode ter que configurar um manipulador de eventos instalando um assembly do manipulador de eventos em cada computador do Project Server no farm do SharePoint e, em seguida, configurando o manipulador de eventos para a instância do Project Web App usando a página de configurações do Project Server em geral Configurações de aplicativos da Administração Central do SharePoint.
    
2. **Configure um computador de desenvolvimento.**
    
   Você geralmente pode acessar a PSI através de uma rede. Os exemplos de código são projetados para ser executado em um cliente separado do servidor, exceto onde observado.
    
   1. **Instale a versão correta do Visual Studio.** Exceto quando observado, as amostras de código são escritas em Visual c#. Eles podem ser usados com o Visual Studio 2010 ou Visual Studio 2012. Certifique-se de que você tenha o service pack mais recente instalado. 
        
   2. **Copie DLLs do Project Server no computador de desenvolvimento.** Copie os seguintes assemblies de `[Program Files]\Microsoft Office Servers\15.0\Bin` no computador do Project Server no computador de desenvolvimento: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Para obter informações sobre como compilar e usar o assembly de proxy ProjectServerServices.dll para os serviços da web ASMX na PSI, consulte [usando um assembly de proxy PSI e descrições de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Instale os arquivos IntelliSense.**
    
    Para usar o IntelliSense descrições para classes e membros em assemblies do Project Server, copiar os arquivos XML IntelliSense atualizados do Project 2013 SDK baixar para o mesmo diretório onde os assemblies do Project Server estão localizados. Por exemplo, copie o arquivo de Microsoft.Office.Project.Server.Library.xml para o diretório onde o seu aplicativo será definida uma referência para o assembly Microsoft.Office.Project.Server.Library.dll.
    
    Descrições de IntelliSense para os serviços da web PSI exigem que você crie um assembly de proxy PSI usando o script CompileASMXProxyAssembly.cmd a `Documentation\IntelliSense\WSDL` subdiretório no download do SDK do Project 2013. O script cria o assembly de proxy com base em ASMX ProjectServerServices.dll. Para obter mais informações, consulte o arquivo de [ReadMe_IntelliSense] no download do SDK. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Criando o aplicativo e adicionando uma referência ao serviço web
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Criar um aplicativo de console**.
    
   Quando você cria um aplicativo de console, na lista suspensa da caixa de diálogo **Novo projeto** , selecione o **.NET Framework 4**. Você pode copiar o código de exemplo PSI para o novo aplicativo.
    
2. **Adicione a referência necessária para ASMX.**
    
   No Solution Explorer, adicione uma referência ao **System.Web.Services** (consulte a Figura 1). 
    
   **Figura 1. Adicionando uma referência no Visual Studio**

   ![Adicionando uma referência no Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Adicionando uma referência no Visual Studio")
  
3. **Copie o código**.
    
   Copie o exemplo de código completo para o arquivo de Module. vb do aplicativo de console.
    
4. **Definir o namespace para o aplicativo de amostra**.
    
   Você pode alterar o namespace listado na parte superior da amostra para o namespace padrão de aplicativo, ou alterar o namespace do aplicativo padrão para corresponder a amostra. Você pode alterar o namespace do aplicativo padrão, alterando as propriedades do aplicativo.
    
   Por exemplo, o exemplo de código para [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) tem o namespace **Microsoft.SDK.Project.Samples.RenameProject**. Se o nome do projeto do Visual Studio for **RenameProject**, copie o namespace do arquivo Module. vb e abra o painel de **Propriedades** do projeto (no menu **projeto** , escolha **Propriedades RenameProject**). Na guia **aplicativo** , copie o namespace na caixa de texto **namespace padrão** . 
    
5. **Defina as referências da web**.
    
   A maioria dos exemplos requerem uma referência a um ou mais dos serviços da web PSI. Eles são listados na amostra de si mesmo ou em comentários que precedem a amostra. Para obter o namespace correto de referências web, certifique-se de que, primeiro, você definir o namespace do aplicativo padrão.
    
   Há três maneiras de adicionar uma referência ao serviço web ASMX para a PSI:
    
   - Crie um conjunto de proxy PSI denominado ProjectServerServices.dll e, em seguida, defina uma referência para o assembly. Para obter o IntelliSense, esta é a maneira recomendada para adicionar uma referência PSI. Consulte [usando um assembly de proxy PSI e descrições de IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Adicione um arquivo de proxy de saída wsdl.exe e a solução do Visual Studio. Consulte [Adicionando um arquivo de proxy PSI](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Adicione uma referência de serviço da web usando o Visual Studio. Consulte a [referência de serviço de adição de uma web](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Usando um assembly de proxy PSI e descrições de IntelliSense

É possível criar e usar o assembly de proxy ProjectServerServices.dll para todos os serviços da web baseados em ASMX no PSI, usando o script CompileASMXProxyAssembly.cmd a `Documentation\IntelliSense\WSDL` pasta do download do SDK do Project 2013. Para um link para o download, consulte a [documentação do desenvolvedor do Project 2013](project-2013-developer-documentation.md).
  
> [!NOTE]
> Quando você extrair os arquivos de origem do proxy do Source.zip de arquivo, os arquivos no `Documentation\IntelliSense\WSDL\Source` pasta são atuais a partir da data de publicação do download do SDK do Project 2013. Para gerar atualizado arquivos de origem do proxy PSI, executados o script de GenASMXProxyAssembly.cmd no computador do Project Server. Os scripts no `Documentation\IntelliSense\WCF` pasta não funcionam para aplicativos baseados em ASMX. O script GenWCFProxyAssembly.cmd chama SvcUtil.exe, que gera arquivos código-fonte para os serviços WCF. Os arquivos de proxy WCF incluem atributos diferentes, a interface de canal e uma classe de cliente para cada serviço PSI. Por exemplo, o serviço de recursos com base em WCF inclui a interface **ResourceChannel** , a interface de **recurso** e a classe **ResourceClient** . Web com base em ASMX recurso inclui a classe de **recurso** com algumas propriedades diferentes. 
  
A seguir é o script de GenASMXProxyAssembly.cmd que gera arquivos de saída WSDL para os serviços da web PSI e, em seguida, compila o assembly.
  
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

O script usa o arquivo de ClassList_asmx.txt, que contém a lista dos serviços da web que estão disponíveis para os desenvolvedores de terceiros.
  
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

Os scripts criam um assembly denominado ProjectServerServices.dll. Evite confusa-lo com ProjectServerServices.dll para o assembly com base em WCF. Os nomes de assembly são os mesmos, para habilitar usando qualquer um dos assembly com o arquivo ProjectServerServices.xml IntelliSense.
  
O namespace arbitrário criado pelos scripts para os serviços WCF e os serviços da web ASMX é o mesmo, para que o arquivo de ProjectServerServices.xml IntelliSense funciona com qualquer assembly. Por exemplo, o namespace do serviço de recurso no assembly proxy com base em WCF e no assembly com base em ASMX proxy é **SvcResource**. Obviamente, você pode alterar os nomes de namespace — se você garantir que elas correspondam no assembly proxy e no arquivo ProjectServerServices.xml IntelliSense.
  
Se um exemplo de código usa um nome diferente para um namespace de serviço da web PSI, por exemplo **ProjectWebSvc**, para o IntelliSense funcione, você deve alterar a amostra para usar **SvcProject** para que o namespace corresponde o assembly de proxy. 
  
Uma vantagem de usar o assembly de proxy com base em ASMX é que ele inclua todos os namespaces de serviço de web PSI; Você não precisará criar várias referências da web. Outra vantagem é que, se você adicionar o arquivo ProjectServerServices.xml no mesmo diretório onde você pode definir uma referência para o assembly de proxy ProjectServerServices.dll, você pode obter o IntelliSense descrições para as classes PSI e membros. A Figura 2 mostra o texto do IntelliSense para o método **Project.QueueCreateProject** . Para obter mais informações, consulte o arquivo de [ReadMe_IntelliSense] na pasta IntelliSense do download do SDK do Project 2013. 
  
**Figura 2. Usando o IntelliSense para um método no serviço da web de projeto**

![Usando o Intellisense para um método em um serviço PSI] (media/pj15_PrerequisitesASMX_Intellisense.gif "Usando o Intellisense para um método em um serviço PSI")
  
Desvantagens de usar o assembly de proxy são que a solução é maior e você deve distribuir e instalar o assembly do proxy com a solução. Você também deve usar os mesmos namespaces que estão no assembly de proxy e arquivos IntelliSense, a menos que você altere o script e arquivos ProjectServerServices.xml IntelliSense usar espaços para nome diferentes.
  
### <a name="adding-a-psi-proxy-file"></a>Adicionando um arquivo de proxy PSI
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

O download do SDK do Project 2013 inclui os arquivos de origem gerados pelo comando Wsdl.exe para o assembly de proxy. Os arquivos de origem estão em Source.zip no `Documentation\IntelliSense\ASMX` subdiretório. Em vez de definir uma referência para o assembly de proxy, você pode adicionar um ou mais dos arquivos de origem para uma solução do Visual Studio. Por exemplo, depois de executar o script GenASMXProxyAssembly.cmd, adicione o wsdl. Arquivo Project.cs à solução. Em vez de executar o script, você pode executar os seguintes comandos para gerar um arquivo de origem único, por exemplo: 
  
```MS-DOS
set VDIR=http://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Para definir um objeto **Project** como uma variável de classe denominada **project**, use o código a seguir. O método **AddContextInfo** adiciona as informações de contexto para o objeto de **projeto** para a autenticação do Windows e autenticação baseada em formulários. 
  
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
> Se você usar um assembly de proxy PSI ou adiciona um arquivo de proxy para obter uma referência de serviço do projeto chamado **SvcProject**, você usaria o mesmo código para criar um objeto **project** . 
  
### <a name="adding-a-web-service-reference"></a>Adicionando uma referência ao serviço web
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Se você não usar o assembly de proxy com base em ASMX ou adicionar um arquivo de saída WSDL, você pode definir uma ou mais referências de web individuais. As etapas a seguir mostram como definir uma referência da web usando o Visual Studio 2012.
  
1. No **Solution Explorer**, clique com botão direito na pasta **referências** e escolha **Adicionar referência de serviço**. 
    
2. Na caixa de diálogo **Adicionar referência de serviço** , escolha **Avançado**.
    
3. Na caixa de diálogo **Configurações de referência do serviço** , escolha **Adicionar referência da Web**.
    
4. Na caixa de texto **URL** , digite `http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`e pressione **Enter** ou escolha o ícone **Ir** . Se você tiver instalado Secure Sockets Layer (SSL), você deve usar o protocolo HTTPS, em vez do protocolo HTTP. 

   Por exemplo, use a seguinte URL para o serviço de projeto no `http://MyServer/pwa` site do Project Web App:`http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Ou, abra o navegador da web e navegue até `http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`. Salve o arquivo em um diretório local, como `C:\Project\WebServices\ServiceName.wsdl`. Na caixa de diálogo **Adicionar referência da Web** , de **URL**, digite o protocolo de arquivo e o caminho para o arquivo. Por exemplo, digite `file://C:\Project\WebServices\Project.wsdl`. 
    
5. Depois que a referência resolve, digite o nome de referência na caixa de texto **nome de referência da Web** . Exemplos de código na documentação do desenvolvedor do Project 2013 usam o nome de referência padrão arbitrário **Svc _ServiceName_**. Por exemplo, o serviço web de projeto é denominado **SvcProject** (consulte a Figura 3). 
    
   **Figura 3. Adicionando uma referência ao serviço web ASMX**

   ![Adicionando uma referência ao serviço web ASMX] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adicionando uma referência ao serviço web ASMX")
  
Para componentes de aplicativo que devem ser executado em um computador do Project Server, utilizam a representação, ou ter permissões elevadas, use uma referência de serviço WCF em vez de uma referência de web ASMX. Para obter mais informações, consulte [pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>A definição de outras referências
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Aplicativos do Project Server frequentemente usam outros serviços, como serviços web do SharePoint Server 2013. Se outros serviços são necessários, eles são mencionados no exemplo.
  
Referências locais para o exemplo de código são listadas instruções **using** na parte superior da amostra: 
  
1. No **Solution Explorer**, clique com botão direito na pasta **referências** e escolha **Adicionar referência**.
    
2. Escolha **Procurar**e navegue até o local onde você armazenou DLLs do servidor do projeto que você copiou anteriormente. Escolha as DLLs, você precisa e escolha **Okey**.
    
> [!NOTE]
> Certifique-se de que as versões de montagem no computador de desenvolvimento correspondem exatamente aqueles no computador do Project Server de destino. 
  
## <a name="using-multiple-authentication"></a>Usando a autenticação de vários
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Autenticação de usuários do Project Server no local, pela autenticação do Windows ou a autenticação de formulários, é feita por meio de declarações de processamento no SharePoint Server 2013. Autenticação de vários significa que o aplicativo web no qual o Project Web App é provisionado suporta a autenticação do Windows e autenticação baseada em formulários. Se for esse o caso, uma chamada para um serviço web ASMX que usa a autenticação do Windows irá falhar com o seguinte erro, porque o processo de declarações não consegue determinar qual tipo de usuário para autenticar:
  
`The server was unable to process the request due to an internal error. . . .`

Para corrigir o problema para ASMX, todas as chamadas para os métodos PSI devem ser uma classe derivada que é definida para cada serviço da web PSI. A classe derivada também deve usar a classe **SvcLoginWindows.LoginWindows** para obter um cookie para a classe de serviço PSI derivada. No exemplo a seguir, a classe **ProjectDerived** derivada da classe **SvcProject.Project** . A classe derivada adiciona a propriedade **EnforceWindowsAuth** e substitui o cabeçalho de solicitação da web para cada chamada a um método na classe **Project** . Se a propriedade **EnforceWindowsAuth** for **true**, o método **GetWebRequest** adiciona um cabeçalho que desabilita a autenticação de formulários. Se **EnforceWindowsAuth** for **false**, a autenticação de formulários possa continuar.
  
Para usar o exemplo a seguir **ASMXLogon_MultiAuth** , crie um aplicativo de console, siga as etapas em [criar o aplicativo e adicionar uma referência ao serviço web](#pj15_PrerequisitesASMX_Configure)e, em seguida, adicione o wsdl. Arquivo de proxy LoginWindows.cs e o wsdl. Arquivo de proxy Project.cs. O método **Main** cria a instância da classe **ProjectDerived** do **projeto** . A amostra deve usar a classe derivada de **LoginWindowsDerived** para obter um objeto **CookieContainer** para o projeto **. CookieContainer** propriedade, que distingue a autenticação de formulários de autenticação do Windows. O objeto de **projeto** pode ser usado para fazer chamadas para qualquer método na classe **SvcProject.Project** . 
  
> [!NOTE]
> O serviço de **LoginWindows** é necessário somente para aplicativos ASMX em um ambiente de autenticação múltiplos. No exemplo **ASMXLogon_MultiAuth** , o método **GetLogonCookie** obtém um cookie para o objeto **loginWindows** . O projeto **. CookieContainer** propriedade estiver definida como o valor de **loginWindows.CookieContainer** . 
  
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

Usando a classe derivada de **LoginWindows** e fazer chamadas PSI com um cabeçalho de solicitação da web que desabilita a autenticação de formulários, são necessário para aplicativos que são executados em um ambiente de autenticação múltiplos. Se o Project Server usa apenas a autenticação de declarações, não é necessário derivar de uma classe que adiciona um cabeçalho de solicitação da web. O exemplo anterior é executado em ambos os ambientes. 
  
A correção para um aplicativo baseado em WCF é diferente. Para obter mais informações, consulte a seção *usando a autenticação de vários* [pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Alterando os valores das constantes genéricos
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

A maioria das amostras têm uma ou mais variáveis que precisam ser atualizados para o exemplo funcione corretamente no seu ambiente. No exemplo a seguir, se você tiver SSL instalado, use o protocolo HTTPS, em vez do protocolo HTTP. Substitua _ServerName_ com o nome do servidor que você está usando. Substitua _ProjectServerName_ pelo nome do diretório virtual do seu site do Project Server, como o PWA. 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

Outras variáveis que devem ser alteradas ou outros pré-requisitos são indicados na parte superior do exemplo de código.
  
## <a name="verifying-the-results"></a>Verificando os resultados
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Obtendo e interpretando os resultados de um exemplo de código nem sempre são simples. Por exemplo, se você criar um projeto, você deve publicar o projeto antes que pode aparecer na página Central de projetos no Project Web App.
  
Você pode verificar os resultados de amostra de código de várias maneiras, por exemplo:
  
- Usar o cliente do Project Professional 2013 para abrir o projeto a partir do computador do Project Server e exibir os itens que você deseja.
    
- Exibir projetos publicados na página Central de projetos do Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).
    
- Exiba o log de fila no Project Web App. Abra a página Configurações do servidor (escolha o ícone **configurações** no canto superior direito) e escolha **Meus Trabalhos Enfileirados** sob a seção **Configurações pessoais** ( `http://ServerName/ProjectServerName/MyJobs.aspx`). Na lista suspensa **modo de exibição** , você pode classificar pelo status do trabalho. O status padrão está **em andamento e trabalhos com falha da semana anterior**. 
    
- Use a página Configurações do servidor no Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) para gerenciar todos os trabalhos em fila e excluir ou forçar o check-in de objetos empresariais. Você deve ter permissões administrativas para acessar esses links na página Configurações do servidor.
    
- Use o **Microsoft SQL Server Management Studio** para executar uma consulta em uma tabela do banco de dados do projeto. Por exemplo, use a seguinte consulta para selecionar as 200 linhas superiores da publicação. Tabela MSP_WORKFLOW_STAGE_PDPS para mostrar informações sobre o projeto (PDPs) de páginas de detalhe em estágios do fluxo de trabalho. 
    
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

## <a name="cleaning-up"></a>Limpando
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

Após testar alguns exemplos de códigos, existem objetos da empresa e as configurações que devem ser excluídas ou redefinir. Você pode usar a página Configurações do servidor no Project Web App para gerenciar dados da empresa ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Links na página Configurações do servidor permitem excluir itens antigos, forçar o check-in de projetos, gerenciar a fila de trabalho para todos os usuários e realizar outras tarefas administrativas.
  
A seguir estão alguns dos links na página Configurações do servidor que você pode usar para atividades de limpeza típica após a execução de códigos de exemplo:
  
- **Campos personalizados da empresa e tabelas de pesquisa**
    
- **Gerenciar trabalhos em fila**
    
- **Excluir objetos da empresa**
    
- **Forçar o Check in de objetos empresariais**
    
- **Tipos de projeto corporativo**
    
- **Fases do fluxo de trabalho**
    
- **Estágios do fluxo de trabalho**
    
- **Páginas de detalhes do projeto**
    
- **Períodos de relatório**
    
- **Configurações de quadro de horários e padrões**
    
- **Classificações de linha**
    
Configurações adicionais são gerenciadas pelo SharePoint Server 2013 para cada instância do Project Web App, em vez de uma página específica de configurações de servidor do Project Web App. No aplicativo Administração Central do SharePoint, escolha **Configurações gerais de aplicativos**, escolha **Gerenciar** em **Configurações do Project Server**e, em seguida, escolha a instância do Project Web App na lista suspensa na página Configurações do servidor . Por exemplo, escolha **Manipuladores de eventos no servidor** , adicione ou exclua os manipuladores de eventos para a instância do Project Web App selecionada. 
  
## <a name="see-also"></a>Confira também
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Utilizam a representação com WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Visão geral da referência PSI do Project](project-psi-reference-overview.md)
- [Central de desenvolvedores do SharePoint](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

