---
title: Pré-requisitos para amostras de código com base em WCF no projeto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Saiba mais informações para ajudá-lo a criar projetos no Visual Studio usando as amostras de código com base em WCF que estão incluídas nos tópicos de referência do Project Server Interface (PSI).
ms.openlocfilehash: 43700a9db4445dacf366c7ca2efe1bfb10914372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771178"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Pré-requisitos para amostras de código com base em WCF no projeto

Saiba mais informações para ajudá-lo a criar projetos no Visual Studio usando as amostras de código com base em WCF que estão incluídas nos tópicos de referência do Project Server Interface (PSI).
   
Muitos dos exemplos de código com base em WCF incluídos na [referência do serviço de web e de biblioteca de classe do Project Server 2013](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) foram criados para a documentação do desenvolvedor do Project 2010 e usam um formato padrão para serviços web do WCF. As amostras ainda funcionam no Project Server 2013 e são projetadas para serem copiados para um aplicativo de console e executados como uma unidade completa. Exceções são observadas na amostra. 
  
Exemplos de código na documentação do desenvolvedor do Project 2013 permanecem inalterados a partir dos exemplos desenvolvidos para o Office Project Server 2007 usam serviços Web ASMX. As amostras com base em ASMX também podem ser adaptadas para usar os serviços WCF. Este artigo mostra como usar as amostras com os serviços WCF. Para obter informações sobre como usar as amostras com serviços da web ASMX, consulte [pré-requisitos para amostras de código com base em ASMX no projeto](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Se o modelo de objeto do cliente (CSOM) inclui os métodos que seu aplicativo requer, novos aplicativos devem ser desenvolvidos com o CSOM. O CSOM permite que os aplicativos funcionar com o Project Online ou em uma instalação local do Project Server 2013. Caso contrário, se o aplicativo usa a PSI, ele deve usar a interface WCF, que é a tecnologia que a Microsoft recomenda para comunicações de rede. Aplicativos que usam a interface ASMX ou a interface WCF podem trabalhar somente para instalações locais do Project Server 2013. 
>
> Para obter mais informações sobre o CSOM, consulte [arquitetura do Project Server 2013](project-server-2013-architecture.md) e [o modelo de objeto do lado do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Antes de executar os exemplos de código, você deve configurar o ambiente de desenvolvimento, configure o aplicativo, adicione um arquivo de configuração do serviço (ou configurar os serviços WCF programaticamente) e alterar valores de constantes genéricos para coincidir com o seu ambiente.
  
## <a name="setting-up-the-development-environment"></a>Configurar o ambiente de desenvolvimento
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Configure um teste de sistema do Project Server.**
    
    Use um teste de sistema do Project Server sempre que você estiver desenvolvendo ou teste. Mesmo quando seu código funciona perfeitamente, dependências interproject, relatórios ou outros fatores ambientais podem causar consequências indesejadas. 
    
    > [!NOTE]
    > Certifique-se de que você é um usuário válido no servidor e verifique se você tem permissões suficientes para as chamadas PSI que usa seu aplicativo. O tópico de documentação do desenvolvedor para cada método PSI inclui uma tabela de permissões do Project Server. Por exemplo, o método [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requer a permissão **NewProject** global e a permissão de **SaveProjectTemplate** . 
  
    Em alguns casos, você pode precisar fazer a depuração remota no servidor. Você também pode ter que configurar um manipulador de eventos instalando um assembly do manipulador de eventos em cada computador do Project Server no farm do SharePoint e, em seguida, configurando o manipulador de eventos para a instância do Project Web App usando a página de configurações do Project Server em geral Configurações de aplicativos da Administração Central do SharePoint.
    
2. **Configure um computador de desenvolvimento.**
    
    Você geralmente pode acessar a PSI através de uma rede. Os exemplos de código são projetados para ser executado em um cliente separado do servidor, exceto onde observado.
    
    1. **Instale a versão correta do Visual Studio.** Exceto quando observado, as amostras de código são escritas em Visual c#. Eles podem ser usados com o Visual Studio 2010 ou Visual Studio 2012. Certifique-se de que você tenha o service pack mais recente instalado. 
    
    2. **Copie DLLs do Project Server no computador de desenvolvimento.** Copie os seguintes assemblies de `[Program Files]\Microsoft Office Servers\15.0\Bin` no computador do Project Server no computador de desenvolvimento: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Para obter informações sobre como compilar e usar o assembly de proxy ProjectServerServices.dll para os serviços WCF na PSI, consulte [usando um assembly de proxy PSI e descrições de IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Instale os arquivos IntelliSense.**
    
    Para usar o IntelliSense descrições para classes e membros em assemblies do Project Server, copiar os arquivos XML IntelliSense atualizados do Project 2013 SDK baixar para o mesmo diretório onde os assemblies do Project Server estão localizados. Por exemplo, copie o arquivo de Microsoft.Office.Project.Server.Library.xml para o diretório onde o seu aplicativo será definida uma referência para o assembly Microsoft.Office.Project.Server.Library.dll.
    
    Descrições de IntelliSense para os serviços PSI exigem que você crie um assembly de proxy PSI usando o script CompileWCFProxyAssembly.cmd a `Documentation\IntelliSense\WCF` subdiretório no download do SDK do Project 2013. O script cria o assembly de proxy ProjectServerServices.dll com base em WCF. Para obter mais informações, consulte o arquivo. mht [ReadMe_IntelliSense] no download do SDK. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Criando o aplicativo e adicionando uma referência de serviço
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Crie um aplicativo de console.**
    
    Quando você cria um aplicativo de console, na lista suspensa da caixa de diálogo **Novo projeto** , selecione o **.NET Framework 4**. Você pode copiar o código de exemplo PSI para o novo aplicativo.
    
2. **Adicione referências necessárias para WCF.**
    
    No Solution Explorer, adicione uma referência ao **ServiceModel** (consulte a Figura 1). **System.ServiceModel.Web**deverão ser usadas por um aplicativo web.
    
    Também adicione uma referência ao **System.Runtime.Serialization**.
    
    **Figura 1. Adicionando as referências no Visual Studio para um aplicativo baseado em WCF**

    ![Adicionar referências para WCF] (media/pj15_PrerequisitesWCF_AddReference.gif "Adicionar referências para WCF")
  
3. **Copie o código**.
    
    Copie o exemplo de código completo para o arquivo de Module. vb do aplicativo de console.
    
4. **Defina o namespace para o aplicativo de exemplo.**
    
    Você pode alterar o namespace listado na parte superior da amostra para o namespace padrão de aplicativo, ou alterar o namespace do aplicativo padrão para corresponder a amostra. Você pode alterar o namespace do aplicativo padrão, alterando as propriedades do aplicativo. 
    
    Por exemplo, o exemplo de código para [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) tem o namespace **Microsoft.SDK.Project.Samples.CreateResourceTest**. Se o nome do projeto do Visual Studio for **ResourceTest**, copie o namespace do arquivo Module. vb e abra o painel de **Propriedades** do projeto (no menu **projeto** , escolha **Propriedades ResourceTest**). Na guia **aplicativo** , copie o namespace na caixa de texto **namespace padrão** . 
    
5. **Defina as referências de serviço.**
    
    Exemplos de muitos requerem uma referência a um ou mais dos serviços PSI. Eles são listados na amostra de si mesmo ou em comentários que precedem a amostra. Para obter o namespace correto das referências de serviço, certifique-se de que, primeiro, você definir o namespace do aplicativo padrão.
    
    Há três maneiras de adicionar uma referência de serviço WCF:
    
    - Crie um conjunto de proxy PSI denominado ProjectServerServices.dll e, em seguida, defina uma referência para o assembly. Consulte [usando um assembly de proxy PSI e descrições de IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Adicione um arquivo de proxy de saída svcutil.exe e a solução do Visual Studio. Consulte [Adicionando um arquivo de proxy PSI](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Adicione uma referência de serviço usando o Visual Studio. Consulte [Adicionando uma referência de serviço](#pj15_PrerequisitesWCF_AddingServiceReference).
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Usando um assembly de proxy PSI e descrições de IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Você pode usar um assembly de proxy para todos os serviços WCF públicos na PSI. Compilar o assembly de proxy ProjectServerServices.dll usando o `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` script no download do SDK do Project 2013 e, em seguida, copie o assembly de proxy para seu computador de desenvolvimento. Copie o arquivo de ProjectServerServices.xml para IntelliSense no mesmo local. No Visual Studio, defina uma referência para o assembly de proxy ProjectServerServices.dll. 
  
Para o Project Server service packs e atualizações, você pode atualizar os arquivos de origem de proxy e criar um novo conjunto de proxy usando o script GenWCFProxyAssembly.cmd na mesma pasta de download do SDK. Para um link para o download do SDK, consulte a [documentação do desenvolvedor do Project 2013](project-2013-developer-documentation.md). Para obter mais informações, consulte a seção [Adicionando uma referência de serviço](#pj15_PrerequisitesWCF_AddingServiceReference) . 
  
> [!NOTE]
> Quando você extrair os arquivos de origem do proxy do Source.zip de arquivo, os arquivos no `Documentation\IntelliSense\WCF\Source` pasta são atuais a partir da data de publicação do download do SDK do Project 2013. Para gerar atualizado arquivos de origem do proxy PSI, executados o script de GenASMXProxyAssembly.cmd no computador do Project Server. Para obter mais informações, consulte [Adicionando uma referência de serviço](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Os scripts no `Documentation\IntelliSense\ASMX` pasta não funcionam para aplicativos baseados no WCF. O script GenASMXProxyAssembly.cmd chama Wsdl.exe, que gera arquivos código-fonte para os serviços ASMX. Os arquivos de proxy ASMX incluem diferentes classes e propriedades. Por exemplo, o serviço da web com base em ASMX recurso inclui a classe de **recurso** , enquanto o serviço de recursos com base em WCF inclui a interface de **recurso** , a interface **ResourceChannel** e a classe **ResourceClient** . 
  
Os espaços para nome arbitrários criados para os serviços WCF e os serviços da web ASMX são os mesmos, para que o arquivo de ProjectServerServices.xml para IntelliSense funciona com qualquer assembly. Por exemplo, o namespace do serviço de recurso no assembly proxy com base em WCF e no assembly com base em ASMX proxy é **SvcResource**. Obviamente, você pode alterar os nomes de namespace — se você garantir que elas correspondam no assembly proxy e no arquivo ProjectServerServices.xml IntelliSense.
  
Se um exemplo de código usa um nome diferente para um namespace de serviço PSI, por exemplo **ProjectWebSvc**, para o IntelliSense funcione, você deve alterar a amostra para usar **SvcProject** para que o namespace corresponde o assembly de proxy. 
  
As vantagens de usar o assembly de proxy com base em WCF incluem o seguinte:
  
- Você pode desenvolver a maioria das soluções com o assembly de proxy em um computador diferente do computador do Project Server. Definindo uma referência de serviço individuais requer o desenvolvimento no computador do Project Server.
    
- O assembly de proxy inclui todos os namespaces de serviço PSI, portanto você não precisa adicionar vários arquivos de proxy.
    
- Se você adicionar o arquivo ProjectServerServices.xml no mesmo diretório onde você pode definir uma referência para o assembly de proxy ProjectServerServices.dll, você pode obter descrições IntelliSense para as classes PSI e membros. Para obter mais informações, consulte o arquivo [ReadMe_IntelliSense] no `Documentation\IntelliSense` pasta do download do SDK do Project 2013. 
    
**Figura 2. Usando o IntelliSense para um método no serviço de recurso**

![Usando o Intellisense para o método ReadResource] (media/pj15_PrerequisitesWCF_Intellisense.gif "Usando o Intellisense para o método ReadResource")
  
Desvantagens de usar o assembly de proxy são que a solução é maior e você deve distribuir e instalar o assembly do proxy com a solução. Você também deve usar os mesmos namespaces que estão no assembly de proxy e arquivos IntelliSense, a menos que você altere o script para criar um assembly de proxy e alterar o arquivo de ProjectServerServices.xml IntelliSense para usar espaços para nome diferentes.
  
### <a name="adding-a-psi-proxy-file"></a>Adicionando um arquivo de proxy PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

O download do SDK do Project 2013 inclui os arquivos de origem que são gerados pelo comando SvcUtil.exe para o assembly de proxy. Os arquivos de origem estão no arquivo Source.zip no `Documentation\IntelliSense\WCF` subdiretório. Em vez de definir uma referência para o assembly de proxy, você pode adicionar um ou mais dos arquivos de origem para uma solução do Visual Studio. Por exemplo, para usar o serviço de projeto e o serviço de recursos, adicione o wcf. Project.cs e wcf. Arquivos de Resource.cs à solução. 
  
No WCF, a classe principal em cada serviço PSI é definida por uma interface e implementada em uma classe de cliente para o acesso aos membros. Por exemplo, a interface de **SvcProject.Resource** é implementada na classe **SvcProject.ResourceClient** . Para definir um objeto **ResourceClient** como uma variável de classe denominada **resourceClient**, por exemplo, use o código a seguir. No exemplo, o método **SetClientEndpoints** cria um objeto de **resourceClient** que usa o ponto de extremidade **basicHttp_Project** , que é definido no arquivo App. config XML. Para obter mais informações sobre o arquivo App, consulte a seção [Adicionando um arquivo de configuração do serviço](#pj15_PrerequisitesWCF_AddConfig) . 
  
```cs
private static SvcResource.ResourceClient resourceClient;
. . .
private static void SetClientEndpoints()
{
  resourceClient = new SvcResource.ResourceClient("basicHttp_Resource");
  . . .
}
public void DisposeClients()
{
  resourceClient.Close();
  . . .
}
```

> [!NOTE]
> Se você usar um assembly de proxy PSI ou adiciona um arquivo de proxy para obter uma referência de serviço do projeto chamado **SvcResource**, você usaria o mesmo código para criar e dispor de um objeto **resourceClient** . 
  
### <a name="adding-a-service-reference"></a>Adding a service reference
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Se você não usar o assembly de proxy com base em WCF ou adicionar um arquivo de proxy para um serviço PSI, você pode definir uma ou mais referências de serviço individuais diretamente no Visual Studio. Você também pode usar a etapa 1 do procedimento a seguir para criar arquivos de proxy atualizados, para preparar o `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` script ou seja incluído no download do SDK do Project 2013. 
  
> [!NOTE]
> Para definir uma referência de serviço, você deve usar o Visual Studio no computador do Project Server. Recomendamos que você use o assembly de proxy ProjectServerServices.dll ou adiciona arquivos de origem de proxy, em vez de diretamente adicionando referências de serviço no Visual Studio. 
  
As etapas a seguir mostram como definir uma referência de serviço usando o Visual Studio 2012 em um computador executando uma instalação de teste do Project Server:
  
1. Para obter acesso aos serviços WCF back-end, execute o Visual Studio no computador do Project Server.
    
2. No **Solution Explorer**, clique com botão direito na pasta **referências** e escolha **Adicionar referência de serviço**. 
    
3. Na caixa de diálogo **Adicionar referência de serviço** , na caixa de texto **endereço** , digite http://localhost:32843/ . svc do _GUID_/psi/ _ServiceName_e pressione **Enter**. Substitua o _GUID_ com o nome do diretório virtual do aplicativo de serviço do Project Server, como 534c37eb00d74ccfadcecf9827e95239. Substitua _ServiceName_ o nome do serviço, como o recurso (consulte a Figura 3). 
    
   Você pode obter o nome do diretório virtual do serviço do Project Server em uma das seguintes maneiras:
    
   - Abra o aplicativo de Administração Central do SharePoint 2013 no seu navegador. Escolha **Gerenciar aplicativos de serviço**e escolha o aplicativo de serviço do Project Server PSI desejado. Por exemplo, escolha **ProjectServerService**. A URL da página Gerenciar Project Web App Sites contém o nome do diretório virtual. Por exemplo, em `http://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, é o nome do diretório virtual `534c37eb00d74ccfadcecf9827e95239` (o nome do diretório não contém nenhum traços). 
    
   - Abra a caixa de diálogo **Gerenciador de serviços de informações da Internet (IIS)** no computador do Project Server. Expanda o nó **Serviços Web do SharePoint** no painel **conexões** e os diretórios virtuais do serviço abaixo, expanda até encontrar o diretório que inclui uma pasta PSI. Selecione o diretório, escolha **Configurações avançadas** no painel **ações** e copie o nome do diretório no campo **Caminho Virtual** . 
    
      > [!NOTE]
      > Pode haver mais de um diretório virtual do serviço do Project Server. Certifique-se de que você escolha o diretório virtual que contém a instância do Project Web App desejado. 
  
   - Use o cmdlet **get-SPServiceApplication** no Windows PowerShell que é instalado com o SharePoint 2013. No menu **Iniciar** da barra de tarefas, escolha **Todos os programas**, escolha **Produtos Microsoft SharePoint 2013**e, em seguida, escolha **Shell de gerenciamento do SharePoint 2013**. A seguir é o comando e os resultados na janela do **Shell de gerenciamento do SharePoint 2013get -** para os aplicativos de serviço definidos (seus GUIDs serão diferentes). Copie o GUID para o aplicativo de serviço do Project Server. 
    
        ```powershell
            PS > get-SPServiceApplication
            DisplayName          TypeName             Id
            -----------          --------             --
            State Service        State Service        04041cfa-4ab3-4473-8bc8-3967b02eff39
            ProjectServerSer...  Project Server PS... 534c37eb-00d7-4ccf-adce-cf9827e95239
            Security Token Se... Security Token Se... 7243732e-edea-405d-8cc8-1716b99faef5
            Application Disco... Application Disco... 3bfbdeb0-bc20-4a21-801c-cc6f1ce6c643
            SharePoint Server... SharePoint Server... 09912f49-3b72-462f-a44c-6533b578286a  
        ```

      Se você souber o nome completo do aplicativo de serviço do Project Server, você pode usá-lo para obter o valor GUID, por exemplo:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Remova os hífens na GUID para obter o nome do diretório virtual. 
  
   URLs como `http://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` são padrão para serviços do Project Server. 
    
4. Depois que a referência de serviço resolve, digite o nome de referência na caixa de texto de **Namespace** . Exemplos de código na documentação do desenvolvedor do Project 2013 usam o nome do namespace arbitrário **Svc _ServiceName_**. Por exemplo, o serviço de recursos nos exemplos de código é nomeado **SvcResource**.
    
    **Figura 3. Adicionando a referência de serviço de recursos com base em WCF**

    ![Adicionando a referência de serviço de recursos com base em WCF] (media/pj15_PrerequisitesWCF_AddSvcReference.gif "Adicionando a referência de serviço de recursos com base em WCF")
  
5. Substitua o arquivo Web. config temporário no diretório de serviço do projeto original (renomeado no Web. config) e, em seguida, execute novamente `iisreset`.
    
## <a name="setting-other-references"></a>A definição de outras referências
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Aplicativos do Project Server frequentemente usam outros serviços, como serviços web do SharePoint 2013. Se outros serviços ou referências forem necessárias, elas são mencionadas no exemplo de código.
  
Referências locais para o exemplo de código são listadas em instruções **using** na parte superior da amostra. 
  
1. No **Solution Explorer**, clique com botão direito na pasta **referências** e escolha **Adicionar referência**.
    
2. Escolha **Procurar**e navegue até o local onde você armazenou DLLs do servidor do projeto que você copiou anteriormente. Escolha as DLLs desejado e escolha **Okey**.
    
> [!NOTE]
> Certifique-se de que as versões de montagem no computador de desenvolvimento correspondem exatamente aqueles no computador do Project Server de destino. 
  
## <a name="adding-a-service-configuration-file"></a>Adicionando um arquivo de configuração de serviço
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Se um aplicativo programaticamente configura os serviços WCF, ele não usa um arquivo de configuração do serviço. Caso contrário, um aplicativo do Windows ou um aplicativo de console usa o elemento **ServiceModel** em um arquivo de App; um aplicativo web inclui **ServiceModel** no Web. config. Para obter mais informações sobre como usar um arquivo App. config ou programaticamente Configurando os serviços WCF, consulte [passo a passo: aplicativos de PSI desenvolvendo usando o WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Quando ele gera um arquivo de origem do proxy de serviço, o comando SvcUtil.exe também cria um arquivo que é a base para o elemento de **ServiceModel** padrão em um arquivo de App Output ou o arquivo Web. config. O download do SDK do Project 2013 inclui um arquivo de Output amostra em `Documentation\IntelliSense\WCF\Source.zip`. Por exemplo, Output arquivo padrão que cria SvcUtil.exe para o serviço de recurso inclui duas ligações, denominadas **BasicHttpBinding_Resource** e **BasicHttpBinding_Resource1**. O elemento do **cliente** inclui dois pontos de extremidade padrão. Um ponto de extremidade é para o acesso seguro para o endereço HTTP na porta 32843 e a outra é para acesso normal na porta 32843, da seguinte maneira: 
  
```XML
<client>
    <endpoint address="http://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="http://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

Configuração do serviço PSI não usa as vinculações padrão e pontos de extremidade. Project Server requer que aplicativos acessar serviços PSI por meio de ProjectServer.svc o front-end, que atua como um roteador de chamadas para os serviços de back-end. Para criar o arquivo App, execute as seguintes etapas:
  
1. Se você define uma referência para o assembly de proxy ProjectServerServices.dll ou adiciona o arquivo de origem de proxy para um serviço, o aplicativo não contém um arquivo App. config. Adicione um novo item ao projeto do Visual Studio. Na caixa de diálogo **Adicionar Novo Item** , selecione o modelo de **Arquivo de configuração de aplicativo** , nomeie-App. config e escolha **Adicionar**.
    
2. Exclua todo o texto no arquivo App. config XML e copie o código a seguir para o arquivo. Você pode usar a mesma associação, por exemplo `basicHttpConf`, para cada ponto de extremidade de serviço. Se você quiser usar mais de uma associação, por exemplo, para vincular os protocolos HTTP e HTTPS, você deve criar uma ligação para cada protocolo.
    
    ```XML
        <?xml version="1.0" encoding="utf-8" ?>
        <configuration>
            <system.serviceModel>
                <behaviors>
                    <endpointBehaviors>
                        <behavior name="basicHttpBehavior">
                            <clientCredentials>
                                <windows allowedImpersonationLevel="Impersonation" />
                            </clientCredentials>
                        </behavior>
                    </endpointBehaviors>
                </behaviors>
                <bindings>
                    <basicHttpBinding>
                        <binding name="basicHttpConf" sendTimeout="01:00:00" 
                            maxBufferSize="500000000" maxReceivedMessageSize="500000000">
                            <readerQuotas maxDepth="32" maxStringContentLength="8192" 
                                maxArrayLength="16384" maxBytesPerRead="4096" 
                                maxNameTableCharCount="500000000" />
                            <security mode="TransportCredentialOnly">
                                <transport clientCredentialType="Ntlm" realm="http://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="http://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Substituir `ServerName/ProjectServerName` no endereço do ponto de extremidade do cliente com o nome do seu servidor e a instância do Project Web App. 
    
4. Substituir `ServiceName` com o nome do serviço PSI, como o recurso. Certifique-se de que você substitua todas as instâncias de três do nome do serviço, por exemplo:
    
    ```XML
        <endpoint address="http://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Para usar mais do que o serviço de um PSI, crie um elemento de **ponto de extremidade** para cada serviço e para cada elemento de **ligação** que usa o serviço. Por exemplo, os seguintes pontos de extremidade configurar o cliente para usar a ligação HTTP básica para o serviço do Project e o serviço QueueSystem. 
    
    > [!NOTE]
    > Se você executa um aplicativo e obter um erro se o servidor está muito ocupado ou que a solicitação HTTP é autorizada, certifique-se de que os endereços de ponto de extremidade estão corretos no arquivo App. config XML. 
  
    ```XML
        <client>
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Você pode editar um arquivo App. config, usando o **Editor de configuração do serviço WCF** no Visual Studio (no menu **Ferramentas** ). Figura 4 mostra como definir o elemento de **contrato** na caixa de diálogo **Editor de configuração de serviço do Microsoft** . Se a solução está usando o assembly de proxy PSI, abra ProjectServerServices.dll no `bin\debug` diretório da solução Visual Studio. A caixa de diálogo de **Navegador do tipo de contrato** mostra todos os contratos de serviço WCF (consulte a Figura 5). 
  
**Figura 4. Usando o Editor de configuração do serviço WCF**

![Usando o Editor de configuração do serviço WCF] (media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Usando o Editor de configuração do serviço WCF")
  
Se a solução está usando um arquivo de proxy de serviço, como wcfResource.cs, compilar o aplicativo e abra o arquivo executável no `bin\debug` directory. Para obter mais informações sobre como editar o arquivo App, consulte [passo a passo: aplicativos de PSI desenvolvendo usando o WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Figura 5. Usando o navegador de tipo de contrato no Editor de configuração de serviço do WCF**

![Usando o navegador do tipo de contrato] (media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Usando o navegador do tipo de contrato")
  
## <a name="using-multiple-authentication"></a>Usando a autenticação de vários
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Autenticação de usuários do Project Server no local, pela autenticação do Windows ou a autenticação de formulários, é feita por meio de declarações de processamento no SharePoint. Autenticação de vários significa que o aplicativo web no qual o Project Web App é provisionado suporta a autenticação do Windows e autenticação baseada em formulários. Se for esse o caso, qualquer chamada para um serviço WCF que usa a autenticação do Windows irá falhar com o seguinte erro, porque o processo de declarações não consegue determinar qual tipo de usuário para autenticar:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Para corrigir o problema para WCF, todas as chamadas para os métodos PSI devem estar dentro um **OperationContextScope** que é definido para cada serviço PSI. Não aninhar escopos para vários serviços; Por exemplo, ao usar as chamadas para os serviços de recurso e projeto, cada conjunto de chamadas deve ser dentro de seu próprio escopo. 
  
No exemplo a seguir, o método **DisableFormsAuth** pode ser chamado a partir de cada seção **OperationContextScope** em um aplicativo. O método remove qualquer valor de cabeçalho que desabilitado anteriormente a autenticação de formulários, para a autenticação de formulários pode continuar se o parâmetro _isWindowsAuth_ for **false**. Se _isWindowsAuth_ for **true**, o método **DisableFormsAuth** desabilitará a autenticação de formulários. 
  
No método **WcfSample** , o objeto **projectClient** é uma instância da classe PSI **SvcProject.ProjectClient** . 
  
```cs
// Class variable that determines whether to disable Forms authentication.
private bool isWindowsUser = true;
public void DisableFormsAuth(bool isWindowsAuth)
{
    WebOperationContext.Current.OutgoingRequest.Headers.Remove(
        "X-FORMS_BASED_AUTH_ACCEPTED");
    if (isWindowsAuth)
    {
        // Disable Forms authentication, to enable Windows authentication.
        WebOperationContext.Current.OutgoingRequest.Headers.Add(
            "X-FORMS_BASED_AUTH_ACCEPTED", "f");
    }
}
private void WcfSample()
{
    // Limit the scope of WCF calls to the client channel. 
    using (OperationContextScope scope = new OperationContextScope(projectClient.InnerChannel))
    {
        // Add a web request header to enable Windows authentication in 
        // multiple authentication installations.
        DisableFormsAuth(isWindowsUser);
        // Add calls to the projectClient methods here:
        // . . .
    }
}
```

> [!NOTE]
> Fazendo chamadas PSI dentro de um **OperationContextScope** é necessário apenas para aplicativos que são executados em um ambiente de autenticação múltiplos. Se o Project Server usa a autenticação do Windows, não é necessário definir um escopo e adicionar um cabeçalho de solicitação da web que desabilita a autenticação de formulários. 
> 
> A correção para um aplicativo baseado em ASMX é diferente. Para obter mais informações, consulte a seção de *autenticação usando vários* em [pré-requisitos para amostras de código com base em ASMX no projeto](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Alterando os valores das constantes genéricos
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

A maioria das amostras têm uma ou mais variáveis que precisam ser atualizados para o exemplo funcione corretamente no seu ambiente. No exemplo a seguir, se você tiver SSL instalado, use o protocolo HTTPS, em vez do protocolo HTTP. Substitua _ServerName_ com o nome do servidor que você está usando. Substitua _ProjectServerName_ com o nome do diretório virtual do seu site do project server, como o PWA. 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

Outras variáveis que você deve alterar são indicados na parte superior do exemplo de código.
  
## <a name="verifying-the-results"></a>Verificando os resultados
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Obtendo e interpretando os resultados de um exemplo de código nem sempre são simples. Por exemplo, se você criar um projeto, você deve publicar o projeto antes que pode aparecer na página Central de projetos no Project Web App.
  
Você pode verificar os resultados de amostra de código de várias maneiras, por exemplo:
  
- Usar o cliente do Project Professional 2013 para abrir o projeto a partir do computador do Project Server e exibir os itens que você deseja.
    
- Exibir projetos publicados na página Central de projetos do Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).
    
- Exiba o log de fila no Project Web App. Abra a página Configurações do servidor (escolha o ícone **configurações** no canto superior direito) e escolha **Meus Trabalhos Enfileirados** sob a seção **Configurações pessoais** ( `http://ServerName/ProjectServerName/MyJobs.aspx`). Na lista suspensa **modo de exibição** , você pode classificar pelo status do trabalho. O status padrão está **em andamento e trabalhos com falha da semana anterior**. 
    
- Use a página Configurações do servidor no Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) para gerenciar todos os trabalhos em fila e excluir ou forçar o check-in de objetos empresariais. Você deve ter permissões administrativas para acessar esses links na página Configurações do servidor.
    
- Use o **Microsoft SQL Server Management Studio** para executar uma consulta em uma tabela de um banco de dados do Project Server. Por exemplo, use a seguinte consulta para selecionar as 200 linhas superiores da tabela MSP_WORKFLOW_STAGE_PDPS para mostrar informações sobre as páginas de detalhes do projeto (PDPs) em estágios do fluxo de trabalho. 
    
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
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

Após testar alguns exemplos de códigos, existem objetos da empresa e as configurações que devem ser excluídas ou redefinir. Você pode usar a página Configurações do servidor no Project Web App para gerenciar dados da empresa ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Links na página Configurações do servidor permitem excluir itens antigos, forçar o check-in de projetos, gerenciar a fila de trabalho para todos os usuários e realizar outras tarefas administrativas.
  
A seguir estão alguns dos links na página Configurações do servidor a ser usado para atividades de limpeza típica após a execução de códigos de exemplo:
  
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

- [Pré-requisitos para amostras de código com base em ASMX no projeto](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Passo a passo: Desenvolvendo aplicativos PSI usando o WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Utilizam a representação com WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Visão geral da referência PSI do Project](project-psi-reference-overview.md) 
- [Central de desenvolvedores do SharePoint](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

