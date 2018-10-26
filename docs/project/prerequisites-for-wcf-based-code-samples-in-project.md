---
title: Pré-requisitos para exemplos de código baseados em WCF no Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Conheça as informações para ajudá-lo a criar projetos no Visual Studio, usando os exemplos de código baseados em WCF que estão inclusos nos tópicos de referência da Interface do Project Server (PSI).
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383377"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>Pré-requisitos para exemplos de código baseados em WCF no Project

Conheça as informações para ajudá-lo a criar projetos no Visual Studio, usando os exemplos de código baseados em WCF que estão inclusos nos tópicos de referência da Interface do Project Server (PSI).
   
Muitos dos exemplos de código baseados em WCF inclusos na [Referência do serviço Web e da biblioteca de classe do Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) foram criados originalmente para a documentação do desenvolvedor do Project 2010 e usam um formato padrão para serviços Web do WCF. Os exemplos ainda funcionam no Project Server 2013 e foram projetados para serem copiados em um aplicativo de console e executados como uma unidade completa. As exceções estão listadas no exemplo. 
  
Os exemplos de código na documentação do desenvolvedor do Project 2013, que estão inalterados em relação aos exemplos desenvolvidos para o Office Project Server 2007, usam serviços Web ASMX. Os exemplos baseados em ASMX também podem ser adaptados para uso com os serviços do WCF. Este artigo mostra como usar os exemplos com serviços Web WCF. Para saber mais sobre como usar os exemplos com serviços ASMX, consulte [Pré-requisitos para exemplos de código baseados em ASMX no Project](prerequisites-for-asmx-based-code-samples-in-project.md).
  
> [!NOTE]
> Se o modelo de objeto do lado do cliente (CSOM) inclui os métodos exigidos pelo aplicativo, os novos aplicativos devem ser desenvolvidos com o CSOM. O CSOM permite que os aplicativos trabalhem com o Project Online ou com uma instalação local do Project Server 2013. Caso contrário, se o aplicativo usar a PSI, ele deve usar a interface WCF, que é a tecnologia que recomendamos para comunicações de rede. Aplicativos que usam a interface ASMX ou WCF podem trabalhar apenas nas instalações locais do Project Server 2013. 
>
> Para saber mais sobre o CSOM, consulte [Arquitetura do Project Server 2013](project-server-2013-architecture.md) e [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Antes de executar os exemplos de código, é necessário configurar o ambiente de desenvolvimento, o aplicativo, adicionar um arquivo de configuração de serviço (ou configurar os serviços do WCF via programação) e alterar os valores constantes genéricos para corresponder ao seu ambiente.
  
## <a name="setting-up-the-development-environment"></a>Configurar o ambiente de desenvolvimento
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **Configurar um teste do sistema do Project Server.**
    
    Use um teste de sistema do Project Server sempre que for desenvolver ou testar. Mesmo quando o código funciona perfeitamente, as dependências entre projetos, os relatórios ou outros fatores do ambiente podem causar consequências indesejadas. 
    
    > [!NOTE]
    > Certifique-se de que você seja um usuário válido no servidor e verifique se tem permissões suficientes para as chamadas da PSI usadas pelo aplicativo. O tópico de documentação do desenvolvedor para cada método da PSI inclui uma tabela de permissões do Project Server. Por exemplo, o método [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) requer a permissão global **NewProject** e a permissão **SaveProjectTemplate**. 
  
    Em alguns casos, você precisa fazer depuração remota no servidor. Você também pode ter que configurar um manipulador de eventos instalando um assembly de manipulador de eventos em cada computador do Project Server no farm do SharePoint e, em seguida, configurar o manipulador de eventos para a instância do Project Web App usando a página Configurações do Project Server em Configurações Gerais de Aplicativos da Administração Central do SharePoint.
    
2. **Configure um computador de desenvolvimento.**
    
    Normalmente você acessa a PSI por uma rede. Os exemplos de código foram projetados para serem executados em um cliente separado do servidor, exceto quando indicado.
    
    1. **Instale a versão correta do Visual Studio.** Exceto quando indicado, os exemplos de código são escritos em Visual C#. Eles podem ser usados no Visual Studio 2010 ou Visual Studio 2012. Certifique-se de ter o service pack mais recente instalado. 
    
    2. **Copie as DLLs do Project Server para o computador de desenvolvimento.** Copie os seguintes assemblies de `[Program Files]\Microsoft Office Servers\15.0\Bin` no computador do Project Server para o computador de desenvolvimento: 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. Para saber mais sobre como compilar e usar o assembly de proxy ProjectServerServices.dll para os serviços do WCF na PSI, consulte [Usar um assembly de proxy da PSI e as descrições do IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
3. **Instale os arquivos do IntelliSense.**
    
    Para usar as descrições do IntelliSense para classes e membros em assemblies do Project Server, copie os arquivos XML atualizados do IntelliSense do download do SDK no Project 2013 para o mesmo diretório em que estão localizados os assemblies do Project Server. Por exemplo, copie o arquivo Microsoft.Office.Project.Server.Library.xml para o diretório em que o aplicativo definirá uma referência para o assembly Microsoft.Office.Project.Server.Library.dll.
    
    As descrições do IntelliSense para serviços da PSI exigem que você crie um assembly de proxy da PSI usando o script CompileWCFProxyAssembly.cmd no subdiretório `Documentation\IntelliSense\WCF` no download do SDK do Project 2013. O script cria o assembly de proxy ProjectServerServices.dll baseado no WCF. Para saber mais, consulte o arquivo [ReadMe_IntelliSense].mht no download do SDK. 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>Criar o aplicativo e adicionar uma referência ao serviço
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **Crie um aplicativo de console.**
    
    Ao criar um aplicativo de console, na lista suspensa da caixa de diálogo **Novo projeto**, selecione **.NET Framework 4**. Você pode copiar o código de exemplo da PSI para o novo aplicativo.
    
2. **Adicione as referências necessárias para WCF.**
    
    No Gerenciador de Soluções, adicione uma referência para **System.ServiceModel** (veja a Figura 1). Um aplicativo Web usaria **System.ServiceModel.Web**.
    
    Também adicione uma referência a **System.Runtime.Serialization**.
    
    **Figura 1. Adicionar as referências no Visual Studio para um aplicativo baseado em WCF**

    ![Adicionar referências para WCF](media/pj15_PrerequisitesWCF_AddReference.gif "Adicionar referências para WCF")
  
3. **Copie o código**.
    
    Copie o exemplo de código completo no arquivo Program.cs do aplicativo de console.
    
4. **Configure o namespace do aplicativo de exemplo.**
    
    É possível alterar o namespace listado na parte superior do exemplo para o namespace padrão do aplicativo, ou alterar o namespace do aplicativo padrão para corresponder ao exemplo. É possível alterar o namespace do aplicativo padrão alterando as propriedades do aplicativo. 
    
    Por exemplo, o código de exemplo [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) tem o namespace **Microsoft.SDK.Project.Samples.CreateResourceTest**. Se o nome do projeto do Visual Studio for **ResourceTest**, copie o namespace do arquivo Program.cs e abra o painel **Propriedades** do projeto (no menu **Projetos**, escolha **Propriedades de ResourceTest**). Na guia **Aplicativo**, copie o namespace na caixa de texto **Namespace padrão**. 
    
5. **Defina as referências de serviço.**
    
    Muitos exemplos exigem uma referência a um ou mais dos serviços da PSI. Eles estão listados no próprio exemplo ou nos comentários que precedem o exemplo. Para obter o namespace correto das referências de serviço, certifique-se de primeiro definir o namespace de aplicativo padrão.
    
    Há três maneiras de adicionar uma referência de serviço WCF:
    
    - Compilar um assembly de proxy da PSI denominado ProjectServerServices.dll e definir uma referência para o assembly. Consulte [Usar um assembly de proxy da PSI e as descrições do IntelliSense](#pj15_PrerequisitesWCF_BuildingProxy).
    
    - Adicionar um arquivo de proxy de saída svcutil.exe à solução do Visual Studio. Consulte [Adicionar um arquivo de proxy da PSI](#pj15_PrerequisitesWCF_AddingProxyFile).
    
    - Adicionar uma referência de serviço usando o Visual Studio. Consulte [Adicionar uma referência de serviço](#pj15_PrerequisitesWCF_AddingServiceReference).
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Usar um assembly de proxy da PSI e as descrições do IntelliSense
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

Você pode usar um assembly de proxy para todos os serviços do WCF públicos na PSI. Compile o assembly de proxy ProjectServerServices.dll usando o script `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` no download do SDK do Project 2013 e copie o assembly de proxy no computador de desenvolvimento. Copie o arquivo ProjectServerServices.xml para o IntelliSense no mesmo local. No Visual Studio, defina uma referência para o assembly de proxy ProjectServerServices.dll. 
  
Para os service packs e as atualizações do Project Server, você pode atualizar os arquivos de origem do proxy e criar um novo assembly de proxy usando o script GenWCFProxyAssembly.cmd na mesma pasta de download do SDK. Para obter um link para baixar o SDK, consulte [Documentação de desenvolvedor do Project 2013](project-2013-developer-documentation.md). Para saber mais, consulte a seção [Adicionar uma referência de serviço](#pj15_PrerequisitesWCF_AddingServiceReference). 
  
> [!NOTE]
> Ao extrair os arquivos de proxy de origem do arquivo Source.zip, os arquivos na pasta `Documentation\IntelliSense\WCF\Source` são atualizados a partir da data de publicação do download do SDK do Project 2013. Para gerar os arquivos de proxy de origem atualizados da PSI, execute o script GenASMXProxyAssembly.cmd no computador do Project Server. Para saber mais, consulte [Adicionar uma referência de serviço](#pj15_PrerequisitesWCF_AddingServiceReference). 
> 
> Os scripts na pasta `Documentation\IntelliSense\ASMX` não funcionam para aplicativos baseados em WCF. O script GenASMXProxyAssembly.cmd chama o Wsdl.exe, que gera os arquivos de código de origem para os serviços ASMX. Os arquivos de proxy ASMX incluem classes e propriedades diferentes. Por exemplo, o serviço Web Resource baseado em ASMX inclui a classe **Resource**, enquanto que o serviço Resource baseado em WCF inclui a interface **Resource**, a interface **ResourceChannel** e a classe **ResourceClient**. 
  
O namespace arbitrário criado para os serviços Web ASMX e WCF é o mesmo, para que o arquivo ProjectServerServices.xml para o IntelliSense funcione com ambos os assemblies. Por exemplo, o namespace do serviço Resource no assembly de proxy baseado em WCF e no assembly de proxy baseado no ASMX é **SvcResource**. Claro que você pode alterar os nomes dos namespaces, se garantir que eles correspondam no assembly de proxy e no arquivo ProjectServerServices.xml do IntelliSense.
  
Se um exemplo de código usa um nome diferente para um namespace de serviço da PSI, por exemplo, **ProjectWebSvc**, para o IntelliSense funcionar, você deve alterar o exemplo para usar **SvcProject** de modo que o namespace corresponda no assembly de proxy. 
  
As vantagens de usar o assembly de proxy com base em WCF incluem o seguinte:
  
- A maioria das soluções pode ser desenvolvida com o assembly do proxy em um computador diferente do computador do Project Server. Definir uma referência individual de serviços exige o desenvolvimento no computador do Project Server.
    
- O assembly de proxy inclui todos os namespaces de serviço da PSI, para que você não precise adicionar vários arquivos de proxy.
    
- Se você adicionar o arquivo ProjectServerServices.xml no mesmo diretório em que definiu uma referência para o assembly de proxy ProjectServerServices.dll, pode obter as descrições do IntelliSense para membros e classes da PSI. Para saber mais, consulte o arquivo [ReadMe_IntelliSense] na pasta `Documentation\IntelliSense` do download do SDK do Project 2013. 
    
**Figura 2. Usar o IntelliSense para um método no serviço Resource**

![Usar o Intellisense para o método ReadResource](media/pj15_PrerequisitesWCF_Intellisense.gif "Usar o Intellisense para o método ReadResource")
  
As desvantagens de usar o assembly de proxy são que a solução é maior e você deve distribuir e instalar o assembly de proxy com a solução. Também é preciso usar os mesmos namespaces contidos nos arquivos do IntelliSense e do assembly de proxy, a menos que você altere o script para criar um assembly de proxy e altere o arquivo ProjectServerServices.xml do IntelliSense para usar namespaces diferentes.
  
### <a name="adding-a-psi-proxy-file"></a>Adicionar um arquivo de proxy da PSI
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

O download de SDK do Project 2013 inclui os arquivos de origem gerados pelo comando SvcUtil.exe para o assembly de proxy. Os arquivos de origem estão no arquivo Source.zip, na subpasta `Documentation\IntelliSense\WCF`. Ao invés de definir uma referência para o assembly de proxy, é possível adicionar um ou mais arquivos de origem à solução do Visual Studio. Por exemplo, para usar os serviços Project e Resource, adicione os arquivos wcf.Project.cs e wcf.Resource.cs à solução. 
  
No WCF, a classe primária em cada serviço da PSI é definida por uma interface e implementada em uma classe de cliente para dar acesso aos membros. Por exemplo, a interface **SvcProject.Resource** foi implementada na classe **SvcProject.ResourceClient**. Para definir um objeto **ResourceClient** como uma variável de classe chamada **resourceClient**, por exemplo, use o seguinte código. No exemplo, o método **SetClientEndpoints** cria um objeto **resourceClient**, que usa o ponto de extremidade **basicHttp_Project** definido no arquivo app.config. Para saber mais sobre o arquivo app.config, consulte a seção [Adicionar um arquivo de configuração do serviço](#pj15_PrerequisitesWCF_AddConfig). 
  
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
> Se você usar um assembly de proxy da PSI ou adicionar um arquivo de proxy a uma referência de serviço do Project chamada **SvcResource**, deve usar o mesmo código para criar e descartar um objeto **resourceClient**. 
  
### <a name="adding-a-service-reference"></a>Adicionar uma referência de serviço
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

Se você não usar um assembly de proxy com base em WCF ou adicionar um arquivo de proxy a um serviço da PSI, defina uma ou mais referências individuais de serviço diretamente no Visual Studio. Você também pode usar a etapa 1 do procedimento a seguir para criar arquivos de proxy atualizados para se preparar para o script `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd`, que acompanha o download do SDK do Project 2013. 
  
> [!NOTE]
> Para definir uma referência de serviço, você deve usar o Visual Studio no computador do Project Server. Recomendamos usar o assembly de proxy ProjectServerServices.dll ou adicionar arquivos de origem de proxy, ao invés de adicionar referências de serviço diretamente no Visual Studio. 
  
As etapas a seguir mostram como definir uma referência de serviço usando o Visual Studio 2012 em um computador que executa uma instalação de teste do Project Server:
  
1. Para ter acesso aos serviços de back-end do WCF, execute o Visual Studio no computador do Project Server.
    
2. No **Gerenciador de Soluções**, clique com botão direito do mouse na pasta **Referências** e, em seguida, escolha **Adicionar Referência de Serviço**. 
    
3. Na caixa de diálogo **Adicionar Referência de Serviço**, na caixa de texto **Endereço**, digite https://localhost:32843/ _GUID_/psi/ _NomeServiço_.svc e pressione **Enter**. Substitua _GUID_ pelo nome o diretório virtual do aplicativo de serviço do Project Server, por exemplo, 534c37eb00d74ccfadcecf9827e95239. Substitua _NomeServiço_ pelo nome do serviço, por exemplo, Resource (consulte a Figura 3). 
    
   Você pode obter o nome do diretório virtual do Serviço do Project Server das seguintes maneiras:
    
   - Abra o aplicativo Administração Central do SharePoint 2013 no navegador. Escolha **Gerenciar aplicativos de serviço** e escolha o aplicativo de serviço da PSI do Project Server que desejar. Por exemplo, escolha **ProjectServerService**. A URL da página Gerenciar Sites do Project Web App contém o nome do diretório virtual. Por exemplo, em `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, o nome do diretório virtual é `534c37eb00d74ccfadcecf9827e95239` (o nome do diretório não contém traços). 
    
   - Abra a caixa de diálogo **Gerenciador dos Serviços de Informações da Internet (IIS)** no computador do Project Server. Expanda o nó **Serviços Web do SharePoint** no painel **Conexões** e expanda os diretórios virtuais de serviço abaixo dele até encontrar o diretório que inclui uma pasta PSI. Selecione o diretório, escolha **Configurações Avançadas** no painel **Ações** e copie o nome do diretório no campo **Caminho Virtual**. 
    
      > [!NOTE]
      > Pode haver mais de um diretório virtual do Serviço do Project Server. Escolha o diretório virtual que contém a instância do Project Web App que você deseja. 
  
   - Use o cmdlet **get-SPServiceApplication** no Windows PowerShell que é instalado com o SharePoint 2013. No menu **Iniciar** da barra de tarefas, escolha **Todos os Programas**, escolha **Produtos do Microsoft SharePoint 2013** e, em seguida, escolha **Shell de Gerenciamento do SharePoint 2013 **. Veja a seguir o comando e os resultados na janela **SharePoint 2013get- Management Shell** para os aplicativos de serviço definidos (seu GUIDs serão diferentes). Copie o GUID para o aplicativo do Serviço do Project Server. 
    
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

      Se souber o nome completo do aplicativo de serviço do Project Server, use-o para obter o valor de GUID, por exemplo:
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > Remova os traços no GUID para obter o nome do diretório virtual. 
  
   URLs como `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` são padrão para os serviços do Project Server. 
    
4. Depois que a referência de serviço for resolvida, digite o nome da referência na caixa de texto **Namespace**. Os exemplos de código na documentação do desenvolvedor do Project 2013 usam o nome de namespace arbitrário **Svc _ServiceName_**. Por exemplo, o serviço Resource nos exemplos de código é chamado de **SvcResource**.
    
    **Figura 3. Adicionar a referência de serviço Resource baseada em WCF**

    ![Adicionar a referência de serviço Resource baseada em WCF](media/pj15_PrerequisitesWCF_AddSvcReference.gif "Adicionar a referência de serviço Resource baseada em WCF")
  
5. Substitua o arquivo temporário web.config no diretório de serviço do Project pelo original (renomeado para web.config) e execute novamente o `iisreset`.
    
## <a name="setting-other-references"></a>Definir outras referências
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Aplicativos do Project Server geralmente usam outros serviços, como serviços Web do SharePoint 2013. Se forem necessários outros serviços ou referências, eles serão detalhados no exemplo de código.
  
As referências locais para o exemplo de código são listadas nas instruções **using** na parte superior do exemplo. 
  
1. No **Gerenciador de Soluções**, clique com botão direito do mouse na pasta **Referências** e, em seguida, escolha **Adicionar Referência**.
    
2. Escolha **Procurar** e, em seguida, navegue até o local onde armazenou as DLLs do Project Server copiadas anteriormente. Escolha as DLLs desejadas e escolha **OK**.
    
> [!NOTE]
> Certifique-se de que as versões de assembly no computador de desenvolvimento são exatamente iguais àquelas no computador do Project Server de destino. 
  
## <a name="adding-a-service-configuration-file"></a>Adicionar um arquivo de configuração de serviço
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

Se um aplicativo configurar via programação os serviços do WCF, ele não usará um arquivo de configuração do serviço. Caso contrário, um aplicativo ou console do Windows usa o elemento **system.serviceModel** em um arquivo app.config; um aplicativo Web inclui **system.serviceModel** no web.config. Para saber mais sobre como usar um arquivo app.config ou como configurar os serviços do WCF via programação, consulte [Passo a passo: desenvolver aplicativos da PSI usando o WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
Quando gera um arquivo de origem de proxy de serviço, o comando SvcUtil.exe também cria um arquivo output.config, que é a base para o elemento **system.serviceModel** padrão em um arquivo app.config ou web.config. O download do SDK do Project 2013 inclui um arquivo output.config de exemplo no `Documentation\IntelliSense\WCF\Source.zip`. Por exemplo, o arquivo output.config padrão que o SvcUtil.exe cria para o serviço Resource inclui duas associações chamadas **BasicHttpBinding_Resource** e **BasicHttpBinding_Resource1**. O elemento **client** inclui dois pontos de extremidade padrão. Um ponto de extremidade é para o acesso seguro ao endereço HTTP na porta 32843 e o outro é para acesso normal na porta 32843, da seguinte maneira: 
  
```XML
<client>
    <endpoint address="https://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="https://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

A configuração do serviço da PSI não usa as associações e os pontos de extremidade padrão. O Project Server exige que os aplicativos acessem serviços da PSI pelo ProjectServer.svc de front-end, que funciona como um roteador para chamadas para os serviços de back-end. Para criar o arquivo app.config, faça o seguinte:
  
1. Se você define uma referência para o assembly de proxy ProjectServerServices.dll ou adiciona o arquivo de origem de proxy para um serviço, o aplicativo não contém um arquivo app.config. Adicione um novo item ao projeto do Visual Studio. Na caixa de diálogo **Adicionar novo item**, escolha o modelo **Arquivo de Configuração do Aplicativo**, nomeie como app.config e escolha **Adicionar**.
    
2. Exclua todo o texto do arquivo app.config e, em seguida, copie o seguinte código no arquivo. Você pode usar a mesma associação, por exemplo `basicHttpConf`, para cada ponto de extremidade do serviço. Se quiser usar mais de uma associação, por exemplo, para vincular os protocolos HTTP e HTTPS, crie uma associação para cada protocolo.
    
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
                                <transport clientCredentialType="Ntlm" realm="https://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="https://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. Substitua `ServerName/ProjectServerName` no endereço do ponto de extremidade do cliente pelo nome do seu servidor e instância do Project Web App. 
    
4. Substitua `ServiceName` pelo nome do serviço da PSI; por exemplo, Resource. Substitua todas as três instâncias do nome do serviço, por exemplo:
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. Para usar mais de um serviço da PSI, crie um elemento **endpoint** para cada serviço e para cada elemento **binding** que o serviço usa. Por exemplo, os pontos de extremidade a seguir configuram o cliente para usar a associação básica de HTTP para o serviço Project e o serviço QueueSystem. 
    
    > [!NOTE]
    > Se você executar um aplicativo e receber um erro dizendo que o servidor está ocupado demais ou que a solicitação HTTP não tem autorização, verifique se os endereços de ponto de extremidade estão corretos no arquivo app.config. 
  
    ```XML
        <client>
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

É possível editar um arquivo app.config usando o **WCF Service Configuration Editor** no Visual Studio (no menu **Ferramentas**). A Figura 4 mostra como configurar o elemento **contract** na caixa de diálogo **Microsoft Service Configuration Editor**. Se a solução estiver usando o assembly de proxy da PSI, abra ProjectServerServices.dll no diretório `bin\debug` da solução do Visual Studio. A caixa de diálogo **Navegador de Tipo de Contrato** mostra todos os contratos de serviço do WCF (consulte a Figura 5). 
  
**Figura 4. Usar o Editor de Configuração de Serviço do WCF**

![Usar o Editor de Configuração de Serviço do WCF](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Usar o Editor de Configuração de Serviço do WCF")
  
Se a solução estiver usando um arquivo de proxy de serviço, como wcfResource.cs, compile o aplicativo e abra o arquivo executável no diretório `bin\debug`. Para saber mais sobre como editar o arquivo app.config, consulte [Passo a passo: desenvolver aplicativos da PSI usando o WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).
  
**Figura 5. Usar o navegador de tipo de contrato no WCF Service Configuration Editor**

![Usar o navegador de tipo de contrato](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Usar o navegador de tipo de contrato")
  
## <a name="using-multiple-authentication"></a>Usar autenticação múltipla
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

A autenticação de usuários do Project Server no local, por autenticação do Windows ou de formulários, é feita pelo processamento de declarações no SharePoint. Autenticação múltipla significa que o aplicativo Web no qual o Project Web App está provisionado oferece suporte à autenticação do Windows e à autenticação baseada em formulários. Se esse for o caso, qualquer chamada para um serviço WCF que usa autenticação do Windows falha com a seguinte mensagem de erro, porque o processo de declarações não pode determinar o tipo de usuário a autenticar:
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

Para corrigir o problema para WCF, todas as chamadas para métodos da PSI devem estar dentro de uma seção **OperationContextScope** definida para cada serviço da PSI. Não aninhe escopos para vários serviços; por exemplo, ao usar chamadas para os serviços Resource e Project, cada conjunto de chamadas deve estar em seu próprio escopo. 
  
No exemplo a seguir o método **DisableFormsAuth** pode ser chamado de cada seção **OperationContextScope** em um aplicativo. O método remove o valor de qualquer cabeçalho que anteriormente desativou a autenticação de formulários, de modo que a autenticação de formulários possa prosseguir se o parâmetro _isWindowsAuth_ for **false**. Se _isWindowsAuth_ for **true**, o método **DisableFormsAuth** desabilitará a autenticação de formulários. 
  
No método **WcfSample**, o objeto **projectClient** é uma instância da classe **SvcProject.ProjectClient** da PSI. 
  
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
> Fazer chamadas PSI em uma seção **OperationContextScope** é necessário apenas para aplicativos que são executados em um ambiente de várias autenticações. Se o Project Server usa apenas a autenticação do Windows, não é necessário definir um escopo e adicionar um cabeçalho de solicitação Web que desabilita a autenticação de formulários. 
> 
> A correção para um aplicativo baseado em ASMX é diferente. Para saber mais, consulte a seção *Usar autenticação múltipla* em [Pré-requisitos para exemplos de código baseados em ASMX no Project](prerequisites-for-asmx-based-code-samples-in-project.md). 
  
## <a name="changing-values-of-generic-constants"></a>Alterar os valores de constantes genéricas
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

A maioria dos exemplos tem uma ou mais variáveis que você deve atualizar para o exemplo funcionar corretamente em seu ambiente. No exemplo a seguir, se você tiver o SSL instalado, use o protocolo HTTPS ao invés do protocolo HTTP. Substitua _ServerName_ pelo nome do servidor que você está usando. Substitua _ProjectServerName_ pelo nome do diretório virtual do seu site do servidor do projeto, como o PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Todas as outras variáveis que você deve alterar são listadas na parte superior do exemplo de código.
  
## <a name="verifying-the-results"></a>Verificar os resultados
<a name="pj15_PrerequisitesWCF_Verify"> </a>

Obter e interpretar resultados de um exemplo de código nem sempre é simples. Por exemplo, se você criar um projeto, deve publicá-lo antes que ele possa aparecer na página Centro do Projeto no Project Web App.
  
Você pode verificar os resultados de exemplo de código de várias maneiras, por exemplo:
  
- Usar o cliente do Project Professional 2013 para abrir o projeto no computador do Project Server e exibir os itens desejados.
    
- Exibir os projetos publicados na página Centro de Projeto do Project Web App (`https://ServerName/ProjectServerName/projects.aspx`).
    
- Exibir o log de fila no Project Web App. Abra a página Configurações do servidor (escolha o ícone **Configurações** no canto superior direito) e escolha **Meus Trabalhos Enfileirados** na seção **Configurações Pessoais** (`https://ServerName/ProjectServerName/MyJobs.aspx`). Na lista suspensa **Exibir**, é possível classificar por status de trabalho. O status padrão será **Trabalhos em andamento e não concluídos na semana passada**. 
    
- Use a página Configurações do servidor no Project Web App (`https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) para gerenciar todos os trabalhos enfileirados e excluir ou forçar o check-in de objetos empresariais. Você deve ter permissões administrativas para acessar esses links na página Configurações do servidor.
    
- Use o **Microsoft SQL Server Management Studio** para executar uma consulta em uma tabela de um banco de dados do Project Server. Por exemplo, use a consulta a seguir para selecionar as primeiras 200 linhas da tabela MSP_WORKFLOW_STAGE_PDPS para mostrar as informações sobre as páginas de detalhes do projeto (PDPs) em estágios do fluxo de trabalho. 
    
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

## <a name="cleaning-up"></a>Limpar
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

Após testar alguns exemplos de código, há configurações e objetos empresariais que devem ser excluídos ou redefinidos. Você pode usar a página Configurações do servidor no Project Web App para gerenciar os dados empresariais (`https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Os links na página Configurações do servidor permitem excluir itens antigos, forçar o check-in em projetos, gerenciar a fila de tarefas para todos os usuários e realizar outras tarefas administrativas.
  
A seguir apresentamos alguns dos links da página Configurações do servidor para usar para atividades comuns de limpeza após executar exemplos de código:
  
- **Campos personalizados empresariais e tabelas de pesquisa**
    
- **Gerenciar trabalhos em fila**
    
- **Excluir objetos empresariais**
    
- **Forçar o check-in de objetos empresariais**
    
- **Tipos de projetos empresariais**
    
- **Fases do fluxo de trabalho**
    
- **Estágios do fluxo de trabalho**
    
- **Páginas de detalhes do projeto**
    
- **Períodos de relatório de tempo**
    
- **Configurações e padrões do quadro de horários**
    
- **Classificações de linha**
    
As configurações adicionais são gerenciadas pelo SharePoint Server 2013 para cada instância do Project Web App, ao invés de por uma página específica de Configurações do servidor do Project Web App. No aplicativo Administração Central do SharePoint, escolha **Configurações Gerais de Aplicativos**, escolha **Gerenciar** em **Configurações do Project Server** e escolha a instância do Project Web App na lista suspensa da página Configurações do servidor. Por exemplo, escolha **Manipuladores de Eventos no Servidor** para adicionar ou excluir os manipuladores de eventos para a instância selecionada do Project Web App. 
  
## <a name="see-also"></a>Confira também

- [Pré-requisitos para exemplos de código baseados em ASMX no Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Passo a passo: desenvolver aplicativos da PSI usando o WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [Usar representação com WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Visão geral da referência da PSI do Project](project-psi-reference-overview.md) 
- [Central de desenvolvedores do SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

