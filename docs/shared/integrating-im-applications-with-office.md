---
title: Integração de aplicativos de mensagens instantâneas ao Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Este artigo descreve como configurar um aplicativo cliente de mensagens instantâneas para que ele se integre aos recursos de redes sociais no Office 2013, incluindo exibir presença e enviar mensagens instantâneas do cartão de visita.
localization_priority: Priority
ms.openlocfilehash: b3add86f011e016b1b6ea1a74f425f3f1deab002
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270110"
---
# <a name="integrating-im-applications-with-office"></a>Integração de aplicativos de mensagens instantâneas ao Office

Este artigo descreve como configurar um aplicativo cliente de mensagens instantâneas para que ele se integre aos recursos de redes sociais no Office 2013, incluindo exibir presença e enviar mensagens instantâneas do cartão de visita.
  
Se você tiver dúvidas ou comentários sobre este artigo técnico, ou sobre os processos que o descrevem, entre em contato diretamente com a Microsoft enviando um email para [docthis@microsoft.com](mailto:docthis@microsoft.com).
  
## <a name="introduction"></a>Introdução
<a name="off15_IMIntegration_Intro"> </a>

O Office 2013 fornece integração avançada aos aplicativos cliente de mensagens instantâneas, incluindo o Lync 2013. Essa integração fornece aos usuários recursos de mensagens instantâneas no Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 e OneNote 2013, bem como fornece integração de presença em páginas do SharePoint 2013. Os usuários podem ver a foto, o nome, o status de presença e os dados de contato das pessoas em sua lista de contatos. Elas podem começar uma sessão de mensagens instantâneas, chamadas de vídeo ou telefonemas diretamente do cartão de visita (o elemento da interface do usuário no Office 2013 que apresenta informações de contato e opções de comunicação). Com o Office 2013, é fácil manter-se conectado aos seus contatos sem que você tenha que sair do email ou dos documentos em que está trabalhando. 
  
> [!NOTE]
> Este artigo usa o termo aplicativo cliente de mensagens instantâneas para se referir especificamente ao aplicativo instalado no computador de um usuário que se comunica com o serviço de mensagens instantâneas. Por exemplo, o Lync 2013 é considerado um aplicativo cliente de mensagens instantâneas. Este artigo não fornece detalhes sobre como o aplicativo cliente de mensagens instantâneas se comunica com o serviço de mensagens instantâneas nem sobre o serviço em si. 
  
Você pode personalizar um aplicativo cliente de mensagens instantâneas para que ele se comunique com o Office. Especificamente, é possível modificar o seu aplicativo de mensagens instantâneas para que ele exiba as seguintes informações na interface de usuário do Office:
  
- Foto do contato.
    
- Nome do contato.
    
- Nota de status pessoal do contato.
    
- Status de presença do contato.
    
- Cadeia de disponibilidade do contato (por exemplo, "Disponível" ou "Ausência Temporária").
    
- Cadeia de recursos do contato (por exemplo, "Pronto para Vídeo").
    
- Início de mensagens instantâneas com um clique.
    
- Início de chamada de vídeo com um clique.
    
- Início de telefonema com um clique (incluindo SIP, número de telefone, caixa postal e ligar para novo número).
    
- Gerenciamento de contatos (adicionar ao grupo de mensagens instantâneas).
    
- Local e fuso horário do contato.
    
- Dados, número de telefone, endereço de email, cargo e nome da empresa do contato.
    
**Figura 1. Cartão de visita no Office 2013**

![O Cartão de Pessoas no Office 2013](media/ocom15_peoplecard.png "O Cartão de Pessoas no Office 2013")
  
Para habilitar essa integração ao Office, um aplicativo cliente de mensagens instantâneas deve implementar um conjunto de interfaces que o Office fornece para se conectar a ele. As APIs para essa integração estão incluídas no namespace [UCCollborationLib](https://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) que está contido no arquivo Microsoft.Office.UC.dll, que é instalado com versões do Office 2013 que incluem o Lync/Skype for Business. O namespace **UCCollaborationLib** inclui as interfaces que você deve implementar para integração ao Office. 
  
> [!IMPORTANT] 
> A biblioteca de tipos para as interfaces necessárias está inserida no Lync 2013/Skype for Business. Para integradores terceirizados, isso funcionará apenas quando o Lync 2013 e o Skype for Business estiverem instalados no computador de destino. Se estiver fazendo a integração usando o Office Standard, você precisará extrair a biblioteca de tipos e instalá-la no computador de destino. O [SDK do Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) inclui o arquivo Microsoft.Office.UC.dll. 
  
> [!NOTE]
>  Alguns aplicativos do Office 2010 podem se integrar de maneira semelhante a um aplicativo provedor de mensagens instantâneas de terceiros: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 e SharePoint Server 2010 (usando o controle ActiveX). Muitas das etapas necessárias na integração do Office 2013 também se aplicam ao Office 2010. Há várias diferenças importantes em como o Office 2010 se integra a um aplicativo do provedor de mensagens instantâneas: 
>  - O Office 2010 não exibe a foto do contato. 
>  - Você deve baixar o arquivo Microsoft.Office.Uc.dll separadamente do Office 2010. O [SDK do Lync 2010](https://www.microsoft.com/en-us/download/details.aspx?id=18898) inclui o arquivo Microsoft.Office.UC.dll para Office 2010. 
>  - Quando o aplicativo do Office chama o método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) no aplicativo cliente de mensagens instantâneas, ele é passado na cadeia de caracteres "14.0.0.0". 
>  - O Office 2010 enumera todos os grupos e contatos assim que ele se conecta a um aplicativo cliente de mensagens instantâneas. 
  
## <a name="how-office-integrates-with-an-im-client-application"></a>Como o Office integra-se a um aplicativo cliente de mensagens instantâneas
<a name="off15_IMIntegration_How"> </a>

Quando um aplicativo do Office 2013 é iniciado, ele passa pelo seguinte processo para se integrar ao aplicativo cliente de mensagens instantâneas padrão:
  
1. Ele verifica o registro para descobrir o aplicativo cliente de mensagens instantâneas padrão e se conectar a ele.
    
2. Ele autentica-se no aplicativo cliente de mensagens instantâneas.
    
3. Ele conecta-se a interfaces específicas que são expostas pelo aplicativo cliente de mensagens instantâneas.
    
4. Ele determina os recursos do usuário atualmente conectado (usuário local), incluindo obter os contatos do usuário, determinar a presença do usuário e determinar os recursos de mensagens instantâneas do usuário (sistema de mensagens instantâneas, chat com vídeo, VOIP, etc.).
    
5. Ele obtém as informações de presença dos contatos do usuário local.
    
6. Quando o aplicativo cliente de mensagens instantâneas é desligado, o aplicativo do Office 2013 é silenciosamente desconectado.
    
### <a name="discovering-the-im-application"></a>Como descobrir o aplicativo de mensagens instantâneas

O aplicativo do Office procura várias chaves e entradas específicas no registro para descobrir o aplicativo cliente de mensagens instantâneas padrão. Se um aplicativo cliente de mensagens instantâneas padrão for descoberto, o aplicativo do Office tentará se conectar a ele.
  
O processo pelo qual o aplicativo do Office passa para descobrir o aplicativo cliente de mensagens instantâneas é o seguinte:
  
1. O aplicativo do Office busca a subchave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp no registro para verificar se ela está definida e lê o nome do aplicativo listado.
    
2. O aplicativo do Office lê a chave HKEY_CURRENT_USER\Software\IM Providers\ _Nome do aplicativo_\UpAndRunning e monitora o valor das alterações.
    
3. O aplicativo do Office em seguida lê a chave do Registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _Nome do aplicativo_ e obtém os valores de ProcessName e CLSID (ID de classe) armazenados nela. 
    
4. Depois que o aplicativo cliente de mensagens instantâneas tiver concluído a sua sequência de inicialização com êxito e registrado todas as classes corretamente para a integração de presença, ele definirá a chave HKEY_CURRENT_USER\Software\IM Providers\ _Nome do aplicativo_\UpAndRunning para "2", indicando que o aplicativo cliente está em execução.
    
5. Quando o aplicativo do Office descobrir que a chave HKEY_CURRENT_USER\Software\IM Providers\ _Nome do aplicativo_\UpAndRunning foi definida para "2", ele verificará a lista de processos em execução no computador em busca do nome do processo do aplicativo cliente de mensagens instantâneas.
    
6. Assim que o aplicativo do Office encontrar o processo que o aplicativo cliente de mensagens instantâneas usa, o aplicativo do Office chamará **CoCreateInstance** usando a CLSID para estabelecer uma conexão com o aplicativo cliente de mensagens instantâneas como um servidor COM fora do processo. 
    
### <a name="authenticating-the-connection-to-the-im-application"></a>Autenticação da conexão com o aplicativo de mensagens instantâneas

Depois que o aplicativo do Office estabelecer uma conexão com o aplicativo cliente de mensagens instantâneas, o próximo passo será este:
  
1. O aplicativo do Office chama o método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para verificar a interface [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). 
    
2. O aplicativo do Office chama o método **IUCOfficeIntegration.GetAuthenticationInfo**, passando a versão mais alta de integração com suporte (por exemplo, "15.0.0.0"). 
    
3. Se o aplicativo cliente de mensagens instantâneas der suporte à versão do Office passada como um parâmetro, o aplicativo retornará a seguinte cadeia de caracteres XML embutida em código para o código de chamada:
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > Por motivos de herança, o aplicativo cliente de mensagens instantâneas deverá retornar o valor exato `<authenticationinfo>` para a chamada a **GetAuthenticationInfo** se a versão do Office passada tiver suporte como um parâmetro. 
  
4. Se o aplicativo cliente de mensagens instantâneas falhar ao retornar um valor, o aplicativo do Office chamará o método **GetAuthenticationInfo** novamente com a próxima versão mais alta com suporte do Office (por exemplo, "14.0.0.0"). 
    
5. Uma vez que o Office determina que o aplicativo cliente de mensagens instantâneas dá suporte às mensagens instantâneas e à integração de presença, ele se conecta a um conjunto necessário de interfaces para concluir a inicialização. (Para saber mais, confira [Estabelecendo conexão com interfaces necessárias](#off15_IMIntegration_HowConnect)).
    
Se o aplicativo do Office encontrar um erro em qualquer uma das etapas acima, ele recuará e a integração de presença não será estabelecida novamente durante a sessão do aplicativo do Office. 
  
### <a name="connecting-to-required-interfaces"></a>Como estabelecer conexão com as interfaces necessárias
<a name="off15_IMIntegration_HowConnect"> </a>

Depois de autenticar a conexão com o aplicativo cliente de mensagens instantâneas, o aplicativo do Office tentará se conectar a um conjunto necessário de interfaces que o aplicativo cliente de mensagens instantâneas deve expor. O aplicativo do Office faz isso seguindo este procedimento:
  
- O aplicativo do Office obtém um objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) chamando o método **IUCOfficeIntegration.GetInterface** e passando a constante **oiInterfaceLyncClient** da enumeração [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface). 
    
- O aplicativo do Office obtém um objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) chamando o método **IUCOfficeIntegration.GetInterface** e passando a constante **oiInterfaceAutomation** da enumeração **OIInterface**. 
    
- O aplicativo do Office configura o ouvinte de eventos [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). 
    
- O aplicativo do Office configura o ouvinte de eventos [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). 
    
- O aplicativo do Office obtém o estado conectado do aplicativo cliente de mensagens instantâneas acessando a propriedade **ILyncClient.State**. 
    
- O aplicativo do Office obtém os recursos do aplicativo cliente de mensagens instantâneas chamando o método **IUCOfficeIntegration.GetSupportedFeatures**, que retorna um sinalizador da enumeração [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature). 
    
- O aplicativo do Office acessa a propriedade **ILyncClient.Self** para obter uma referência a um objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf). 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a>Recuperação dos recursos do usuário local
<a name="off15_IMIntegration_HowConnect"> </a>

O aplicativo do Office obtém os recursos do usuário local seguindo este procedimento:
  
1. Se o aplicativo cliente de mensagens instantâneas der suporte à interface **IClient2**, o Office tentará obter um objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) acessando a propriedade **IClient2.PrivateContactManager**. 
    
2. Se o aplicativo de mensagens instantâneas não der suporte à interface **IClient2**, o aplicativo do Office obterá um objeto **IContactManager** acessando a propriedade **ILyncClient.ContactManager**. O aplicativo cliente de mensagens instantâneas deve retornar com êxito um objeto **IContactManager** para que qualquer outro recurso de mensagens instantâneas possa ser estabelecido. 
    
3. O aplicativo do Office acessa a propriedade **ILyncClient.Uri** e, em seguida, chama **IContactManager.GetContactByUri** para obter o objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) associado ao usuário local. 
    
4. O aplicativo do Office faz várias chamadas a **IContact.CanStart** para estabelecer os recursos do usuário local, passando os valores para **ModalityTypes.ucModalityInstantMessage** e **ModalityTypes.ucModalityAudioVideo** sucessivamente. 
    
### <a name="retrieving-contact-presence"></a>Recuperação da presença do contato
<a name="off15_IMIntegration_HowConnect"> </a>

O aplicativo do Office obtém a presença do contato, incluindo o usuário local, seguindo este procedimento: 
  
1. O aplicativo do Office chama **IContact.GetContactInformation** para obter um item de presença do contato. 
    
2. O aplicativo do Office, em seguida, faz a inscrição para receber alterações de status de presença do contato. Ele chama **IContactManager.CreateSubscription** para obter um objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription). Em seguida, ele chama **IContactSubscription.AddContact** para adicionar o contato à inscrição e chama **IContactSubscription.Subscribe** para obter as alterações no status do contato. 
    
3. Se o aplicativo de mensagens instantâneas der suporte a **IContact2**, o Office tentará obter informações de presença chamando **IContact2.BatchGetContactInformation2**.
    
4. O aplicativo do Office recupera as propriedades de presença para o contato chamando **IContact.BatchGetContactInformation**. O aplicativo do Office pode obter um segundo conjunto de propriedades de presença acessando a propriedade **IContact.Settings**. 
    
5. Por fim, o aplicativo do Office obtém a associação a um grupo do contato acessando a propriedade **IContact.CustomGroups**. Isso retorna uma coleção [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que inclui todos os objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) aos quais o contato pertence. 
    
### <a name="disconnecting-from-the-im-application"></a>Desconexão do aplicativo de mensagens instantâneas
<a name="off15_IMIntegration_HowConnect"> </a>

Quando o aplicativo do Office 2013 detecta o evento **OnShuttingDown** do aplicativo de mensagens instantâneas, ele se desconecta silenciosamente. No entanto, se o aplicativo do Office for desligado antes do aplicativo de mensagens instantâneas, o aplicativo do Office não garantirá que a conexão seja limpa. O aplicativo de mensagens instantâneas deve tratar dos vazamentos de conexão do cliente. 
  
## <a name="setting-registry-keys-and-entries"></a>Configuração de entradas e chaves do Registro
<a name="off15_IMIntegration_SetRegistry"> </a>

Conforme mencionado anteriormente, os aplicativos do Office 2013 compatíveis com mensagens instantâneas procuram chaves, entradas e valores específicos no registro para descobrir o aplicativo cliente de mensagens instantâneas ao qual se conectar. Esses valores de registro fornecem ao aplicativo do Office o nome do processo e a CLSID da classe que atua como o ponto de entrada para o modelo do aplicativo cliente de mensagens instantâneas (isto é, a classe que implementa a interface **IUCOfficeIntegration**). O aplicativo do Office cria essa classe em conjunto e se conecta como um cliente ao servidor COM fora do processo no aplicativo cliente de mensagens instantâneas. 
  
Use a Tabela 1 para identificar as chaves, as entradas e os valores que devem ser gravados no registro para integração de um aplicativo cliente de mensagens instantâneas ao Office.
  
**Table 1. Chaves do Registro para configuração do aplicativo cliente de mensagens instantâneas padrão**

|**Chave**|**Entrada**|**Tipo**|**Valor**|**Exemplo**|
|:-----|:-----|:-----|:-----|:-----|
|HKEY_LOCAL_MACHINE\Software\IM Providers\\<Nome do aplicativo\>  <br/> |FriendlyName  <br/> |REG_SZ  <br/> |O nome do aplicativo cliente de mensagens instantâneas de terceiros.  <br/> |Litware IM 2012  <br/> |
||ProcessName  <br/> |REG_SZ  <br/> |O nome do processo do aplicativo cliente de mensagens instantâneas de terceiros.  <br/> |litware.exe  <br/> |
||GUID  <br/> |REG_SZ  <br/> |Uma ID de classe (CLSID) para a classe raiz que pode ser criada em conjunto no aplicativo cliente de mensagens instantâneas (a classe que implementa a interface **IUCOfficeIntegration**).  <br/> |(UM GUID)  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers  <br/> |DefaultIMApp  <br/> |REG_SZ  <br/> |O nome do aplicativo cliente de mensagens instantâneas. Deve ser igual ao nome da chave do Registro de nível superior (hive) em HKEY_LOCAL_MACHINE.  <br/> |Litware  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers\\<Nome do aplicativo\>  <br/> |UpAndRunning  <br/> |REG_DWORD  <br/> | Um valor inteiro entre 0 e 2:  <br/>  0 – Não está em execução  <br/>  1 – Iniciando  <br/>  2 – Executando  <br/> <br/>**OBSERVAÇÃO**: a chave do Registro do nome do aplicativo deve ser igual ao valor da entrada DefaultIMApp.           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a>Como implementar as interfaces necessárias para integração ao Office
<a name="off15_IMIntegration_ImplementRequired"> </a>

Há três interfaces no namespace **UCCollaborationLib** que o executável (ou servidor COM) de um aplicativo cliente de mensagens instantâneas deve implementar para que possa se integrar ao Office. Se essas interfaces não estiverem implementadas, o aplicativo do Office recuará durante o processo de inicialização e a conexão com o aplicativo cliente de mensagens instantâneas não será estabelecida. 
  
As interfaces necessárias são as seguintes:
  
- [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration): embora não seja necessária, a interface **_IUCOfficeIntegrationEvents** também deve ser implementada na mesma classe derivada. 
    
- [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient): embora não seja necessária, a interface **_ILyncClientEvents** também deve ser implementada na mesma classe derivada. 
    
- [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a>Interface IUCOfficeIntegration
<a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a>

A interface **IUCOfficeIntegration** fornece o ponto de entrada para que um aplicativo do Office se conecte ao aplicativo cliente de mensagens instantâneas. A interface define três métodos que um aplicativo do Office chama como parte do processo de iniciar uma conexão com o aplicativo cliente de mensagens instantâneas. A classe que implementa a interface **IUCOfficeIntegration** deve ser criada em conjunto para que o Office possa criar uma instância dela em conjunto. Além disso, ela deve expor a CLSID que é inserida como o valor para a entrada GUID na chave do Registro HKEY_LOCAL_MACHINE\Software\IM Providers\  _Nome do aplicativo_. 
  
A classe que é herdada de **IUCOfficeIntegration** também deve implementar a interface **_IUCOfficeIntegrationEvents**. A interface **_IUCOfficeIntegrationEvents** contém os membros que expõem os manipuladores de eventos da interface **IUCOfficeIntegration**. 
  
A Tabela 2 mostra os membros que devem ser implementados na classe que é herdada de **IUCOfficeIntegration** e **_IUCOfficeIntegration**.
  
> [!NOTE]
> Para saber mais sobre as interfaces **IUCOfficeIntegration** e **_IUCOfficeIntegrationEvents** e seus membros, confira [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) e [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents). 
  
**Tabela 2. Implementação das interfaces IUCOfficeIntegration e _IUCOfficeIntegrationEvents**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**IUCOfficeIntegration** <br/> |Método **GetAuthenticationInfo**  <br/> |Obtém a cadeia de caracteres de informações sobre a autenticação.  <br/> |
||Método **GetInterface**  <br/> |Obtém a interface de uma versão específica.  <br/> |
||Método **GetSupportedFeatures**  <br/> |Obtém os recursos de integração do Office com suporte.  <br/> |
|**_IUCOfficeIntegrationEvents** <br/> |Evento **OnShuttingDown**  <br/> |O evento gerado quando o aplicativo cliente de mensagens instantâneas está tentando desligar.  <br/> |
   
Use o código a seguir para definir uma classe que é herdada das interfaces **IUCOfficeIntegration** e **_IUCOfficeIntegration** em um aplicativo cliente de mensagens instantâneas. 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

O método **GetAuthenticationInfo** usa uma cadeia de caracteres como um argumento para o parâmetro _version_. Quando o aplicativo do Office chama esse método, ele passa uma das duas cadeias de caracteres para o argumento, dependendo da versão do Office. Quando o aplicativo do Office fornece o método com a versão do Office que tem suporte do aplicativo cliente de mensagens instantâneas (isto é, dá suporte à funcionalidade), o método **GetAuthenticationInfo** retorna uma cadeia de XML embutida em código `<authenticationinfo>`. 
  
Use o código a seguir para implementar o método **GetAuthentication** no código do aplicativo cliente de mensagens instantâneas. 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

O método **GetInterface** leva e traz referências a classes para o código de chamada, dependendo do que é passado como um argumento para o parâmetro _interface_. Quando um aplicativo do Office chama o método **GetInterface**, ele passa um dos dois valores para o parâmetro interface: ou a constante **oiInterfaceILyncClient** (1) ou a constante **oiInterfaceIAutomation** (2) da enumeração [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface). Se o aplicativo do Office passar a constante **oiInterfaceILyncClient**, o método **GetInterface** retornará uma referência a uma classe que implementa a interface **ILyncClient**. Se o aplicativo do Office passar a constante **oiInterfaceIAutomation**, o método **GetInterface** retornará uma classe que implementa a interface **IAutomation**. 
  
Use o exemplo de código a seguir para implementar o método **GetInterface** no código do aplicativo cliente de mensagens instantâneas. 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

O método **GetSupportedFeatures** retorna informações sobre os recursos de mensagens instantâneas aos quais o aplicativo cliente de mensagens instantâneas dá suporte. Ele usa uma cadeia de caracteres para seu único parâmetro, _version_. Quando o aplicativo do Office chama o método **GetSupportFeatures**, o método retorna um valor da enumeração [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature). O valor retornado especifica os recursos do cliente de mensagens instantâneas, onde cada recurso do aplicativo cliente de mensagens instantâneas é indicado para o aplicativo do Office adicionando um sinalizador ao valor. 
  
> [!NOTE]
>  Os aplicativos do Office 2013 ignoram as seguintes constantes na enumeração **OIFeature**: 
> - **oiFeaturePictures** (2) 
> - **oiFeatureFreeBusyIntegration**
> - **oiFeaturePhoneNormalization**
  
Use o exemplo de código a seguir para implementar o método **GetSupportFeatures** no código do aplicativo cliente de mensagens instantâneas. 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a>Interface ILyncClient
<a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a>

A interface **ILyncClient** é mapeada para os recursos do aplicativo cliente de mensagens instantâneas em si. Ela expõe propriedades que se referem à pessoa que está conectada ao aplicativo (o usuário local, representado pela interface [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf)), o estado do aplicativo, a lista de contatos do usuário local e várias outras configurações. Quando está tentando se conectar ao aplicativo cliente de mensagens instantâneas, o aplicativo do Office obtém uma referência a um objeto que implementa a interface **ILyncClient**. Dessa referência, o Office pode acessar muitas funcionalidades do aplicativo cliente de mensagens instantâneas. 
  
Além disso, a classe que implementa a interface **ILyncClient** também deve implementar a interface **_ILyncClientEvents**. A interface **_ILyncClientEvents** expõe vários eventos que são obrigatórios para monitoramento do estado do aplicativo cliente de mensagens instantâneas. 
  
A Tabela 3 mostra os membros que devem ser implementados na classe que é herdade de **ILyncClient** e **_ILyncClientEvents**.
  
> [!NOTE]
> Qualquer membro da interface **ILyncClient** ou **\_ILyncClientEvents** não listado na tabela deve estar presente, mas não precisa ser implementada. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E\_NOTIMPL**. 
> 
> Para saber mais sobre as interfaces **ILyncClient** e **_ILyncClientEvents** e seus membros, confira [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) e [UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents). 
  
**Tabela 3. Implementação das interfaces ILyncClient e ILyncClientEvents**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**ILyncClient** <br/> |Propriedade **ContactManager**  <br/> |Obtém o gerenciador do grupo de contatos.  <br/> |
||Propriedade **ConversationManager**  <br/> |Obtém o gerenciador de conversas.  <br/> |
||Propriedade **Self**  <br/> |Obtém o objeto **Self**.  <br/> |
||Método **SignIn**  <br/> |Inicia o processo de entrada do aplicativo cliente de mensagens instantâneas com uma disponibilidade específica.  <br/> |
||Propriedade **State**  <br/> |Obtém o estado atual da plataforma.  <br/> |
||Propriedade **Uri**  <br/> |Obtém o URI do aplicativo cliente de mensagens instantâneas.  <br/> |
|**_ILyncClientEvents** <br/> |Evento **OnStateChanged**  <br/> |Gerado quando o estado do aplicativo cliente de mensagens instantâneas muda. Você deve tratar esse evento e obter a propriedade **eventData.NewState**. O evento é gerado para todos os processos vinculados a uma instância de um aplicativo cliente de mensagens instantâneas quando qualquer subsistema no aplicativo faz com que o estado mude.  <br/> |
   
Durante o processo de inicialização, o Office acessa a propriedade **ILyncClient.State**. Essa propriedade precisa retornar um valor da enumeração [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState). 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

A propriedade **State** armazena o status atual do aplicativo cliente de mensagens instantâneas. Ela deve ser definida e atualizada durante toda a sessão de aplicativo cliente de mensagens instantâneas. Quando o aplicativo cliente de mensagens instantâneas é conectado, desconectado ou desligado, ele deve definir a propriedade **State**. É melhor definir essa propriedade nos métodos **ILyncClient.SignIn** e **ILyncClient.SignOut**, como demonstra o exemplo a seguir. 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

O exemplo de código a seguir demonstra como configurar o ouvinte de eventos usando as interfaces _ **ILyncClientEvents** e _ **IUCOfficeIntegrationEvents**. 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a>Interface IAutomation
<a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a>

A interface **IAutomation** automatiza recursos do aplicativo cliente de mensagens instantâneas. Ela pode ser usada para iniciar conversas, ingressar em conferências e fornecem contexto da janela de extensibilidade. 
  
A Tabela 4 mostra os membros que devem ser implementados na classe que é herdada de **IAutomation**.
  
> [!NOTE]
> Qualquer membro da interface **IAutomation** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**. 
> 
> Para saber mais sobre a interface **IAutomation** e seus membros, confira [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation). 
  
**Tabela 4. Implementação da interface IAutomation**

|**Membro**|**Descrição**|
|:-----|:-----|
|Método **StartConversation**  <br/> |Inicia uma conversa usando a modalidade de conversa especificada. Uma instância de **IConversationWindow** é retornada.  <br/> |
   
## <a name="implementing-contact-presence-integration"></a>Como implementar a integração da presença do contato
<a name="off15_IMIntegration_ImplementIMFeatures"> </a>

Além das três interfaces obrigatórias abordadas anteriormente, há várias outras interfaces que são importantes para habilitar a funcionalidade de presença do contato no Office. Elas incluem o seguinte:
  
- A interface [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) ou **IContact2**. 
    
- A interface [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf). 
    
- As interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) e [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager). 
    
- As interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) e [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup). 
    
- A interface [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription). 
    
- A interface [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint). 
    
- A interface [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) 
    
### <a name="icontact-interface"></a>Interface IContact
<a name="off15_IMIntegration_ImplementRequired_IContact"> </a>

A interface **IContact** representa um usuário do aplicativo cliente de mensagens instantâneas. A interface expõe presença, modalidades disponíveis, associação a um grupo e propriedades do tipo de contato de um usuário. Para iniciar uma conversa com outro usuário, você deve fornecer a instância de usuário de **IContact**.
  
A Tabela 5 mostra os membros que devem ser implementados na classe que é herdada de **IContact**.
  
> [!NOTE]
> Qualquer membro da interface **IContact** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**. 
>
> Para saber mais sobre a interface **IContact** e seus membros, confira [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact). 
  
**Tabela 5. Implementação da interface IContact**

|**Membro**|**Descrição**|
|:-----|:-----|
|Método **CanStart**  <br/> |Retornará **true** se um determinado tipo de modalidade puder ser iniciado no contato.  <br/> |
|Método **GetContactInformation**  <br/> |Obtém um item de presença de um contato de publicação.  <br/> |
|Método **BatchGetContactInformation**  <br/> |Obtém vários itens de presença de um contato de publicação.  <br/> |
|Propriedade **Settings**  <br/> |Obtém uma coleção de propriedades do contato.  <br/> |
|Propriedade **CustomGroups**  <br/> |Obtém uma coleção de grupos dos quais o contato é um membro.  <br/> |
   
Durante o processo de inicialização, o aplicativo do Office chama o método **IContact.CanStart** para determinar os recursos de mensagens instantâneas para o usuário local. O método **CanStart** usa um sinalizador da enumeração [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como um argumento para o parâmetro __modalityTypes_. Se o usuário atual puder se envolver na modalidade solicitada (isto é, o usuário pode enviar e receber mensagens instantâneas, mensagens de áudio e vídeo ou compartilhar aplicativos), o método **CanStart** retornará **true**.
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

O método **GetContactInformation** recupera informações sobre o contato do objeto **IContact**. O código de chamada precisa passar um valor da enumeração [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para o parâmetro __contactInformationType_, que indica os dados a serem recuperados. 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

Semelhante a **GetContactInformation**, o método **BatchGetContactInformation** recupera vários itens de presença sobre o contato no objeto **IContact**. O código de chamada precisa passar uma matriz de valores da enumeração **ContactInformationType** para o parâmetro __contactInformationTypes_. O método retorna um objeto [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contém os dados solicitados. 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

A propriedade **IContact.Settings** retorna um objeto **IContactSettingDictionary** que contém propriedades personalizadas sobre o contato. 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

A propriedade **IContact.CustomGroups** retorna um objeto **IGroupCollection** que inclui todos os grupos dos quais o contato é um membro. 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a>Interface ISelf
<a name="off15_IMIntegration_ImplementRequired_ISelf"> </a>

Durante o processo de inicialização, o aplicativo do Office obtém os dados para o usuário atual acessando a propriedade **ILyncClient.Self**, que deve retornar um objeto **ISelf**. A interface **ISelf** representa o local, o usuário do aplicativo cliente de mensagens instantâneas. 
  
A Tabela 6 mostra os membros que devem ser implementados na classe que é herdada de **ISelf**.
  
> [!NOTE]
> Qualquer membro da interface **ISelf** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**. 
  
**Tabela 6. Implementação da interface ISelf**

|**Membro**|**Descrição**|
|:-----|:-----|
|Propriedade **Contact**  <br/> |Obtém o objeto **IContact** associado ao usuário local.  <br/> |
   
Presença, modalidades disponíveis, associação a um grupo e propriedades do tipo de contato para o usuário local são expostos pela propriedade **ISelf.Contact** (que retorna um objeto **IContact**). Durante o processo de inicialização, o aplicativo do Office acessa a propriedade **ISelf.Contact** para obter uma referência às informações de contato para o usuário local. 
  
Use o código a seguir para definir uma classe que seja herdada da interface **ISelf** que implementa a propriedade **Contact**. 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a>Interfaces IContactManager e _IContactManagerEvents
<a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a>

O objeto **IContactManager** gerencia os contatos para o usuário local, incluindo as informações de contato do próprio usuário local. O aplicativo do Office usa um objeto **IContactManager** para acessar objetos **IContact** que correspondem aos contatos do usuário local. 
  
A Tabela 7 mostra os membros que devem ser implementados na classe que é herdada de **IContactManager** e **_IContactManagerEvents**.
  
> [!NOTE]
> Qualquer membro da interface **IContactManager** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E\_NOTIMPL**. 
>
> Para saber mais sobre as interfaces **IContactManager** e **_IContactManagerEvents** e seus membros, confira [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) e [UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents). 
  
**Tabela 7. Implementação das interfaces IContactManager e _IContactManagerEvents**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**IContactManager** <br/> |Método **GetContactByUri**  <br/> |Encontra ou cria uma nova instância de contato usando o URI de contato.  <br/> |
||Método **CreateSubscription**  <br/> |Cria um objeto **ISubscription** que pode ser usado para envio em lotes de inscrições ou consultas.  <br/> |
||Método **Lookup**  <br/> |Procura um contato ou grupo de distribuição.  <br/> |
|**_IContactManagerEvents** <br/> |Evento **OnGroupAdded**  <br/> |Gerado quando um grupo é adicionado a uma coleção de grupos. A coleção de grupos atualizados pode ser obtida na propriedade **IContactManager.Groups**.  <br/> |
||Evento **OnGroupRemoved**  <br/> |Gerado quando um grupo é removido de uma coleção de grupos. A coleção de grupos atualizados pode ser obtida na propriedade **IContactManager.Groups**.  <br/> |
||Evento **OnSearchProviderStateChanged**  <br/> |Gerado quando o status de um provedor de pesquisa muda.  <br/> |
   
O Office chama **IContactManager.GetContactByUri** para obter informações de presença de um contato usando o endereço SIP do contato. Quando um contato é configurado para um endereço SIP no Active Directory, o Office determina esse endereço para um contato e chama **GetContactByUri**, passando o endereço SIP do contato para o parâmetro __contactUri_. 
  
Quando o Office não puder determinar o endereço SIP para o contato, ele chamará o método **IContactManager.Lookup** para encontrar o SIP usando o serviço de mensagens instantâneas. Aqui, o Office passa os melhores dados que pode encontrar para o contato (por exemplo, o endereço de email do contato). O método **Lookup** retorna um objeto **AsynchronousOperation** de modo assíncrono. Quando invocar o retorno de chamada, o método **Lookup** deverá retornar o êxito ou a falha da operação além do URI do contato. 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

O aplicativo do Office precisa ser inscrito para receber as alterações de presença de um contato individual. Dessa forma, quando o status de presença de um contato é alterado, o servidor de mensagens instantâneas alerta o aplicativo cliente de mensagens instantâneas, alertando, assim, o aplicativo do Office. Para isso, o aplicativo do Office chama o método **IContactManager.CreateSubscription** para criar um novo objeto **IContactSubscription** para essa solicitação. 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a>Interfaces IGroup e IGroupCollection
<a name="off15_IMIntegration_ImplementRequired_IGroup"> </a>

O objeto **IGroup** representa uma coleção de contatos com propriedades adicionais para identificar a coleção de contatos por um nome de grupo coletivo. Um objeto **IGroupCollection** representa uma coleção de objetos **IGroup** definidos por um usuário local e o aplicativo cliente de mensagens instantâneas. O aplicativo do Office usa os objetos **IGroupCollection** e **IGroup** para acessar os contatos do usuário local. 
  
A Tabela 9 mostra os membros que devem ser implementados nas classes que são herdadas de **IGroup** e **IGroupCollection** na tabela a seguir. 
  
> [!NOTE]
> Qualquer membro da interface **IGroup** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**. 
>
> Para saber mais sobre as interfaces **IGroup** e **IGroupCollection** e seus membros, confira [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) e [UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection). 
  
**Tabela 9. Implementação das interfaces IGroup e IGroupCollection**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**IGroupCollection** <br/> |Propriedade **Count**  <br/> |Retorna a contagem dos objetos **IGroup** na coleção  <br/> |
||Propriedade **Item**  <br/> |Retorna o objeto **IGroup** no índice especificado na coleção.  <br/> |
|**IGroup** <br/> |Propriedade **Id**  <br/> |Retorna a ID do grupo.  <br/> |
   
Quando o aplicativo do Office obtém informações do usuário local, ele acessa as associações ao grupo do contato (usuário local) chamando a propriedade **IContact.CustomGroups**, que retorna um objeto **IGroupCollection**. O **IGroupCollection** deve conter uma matriz (ou **Lista**) de objetos **IGroup**. A classe que deriva de **IGroupCollection** deve expor uma propriedade **Count**, que retorna o número de itens na coleção, e um método indexador, **this(int)**, que retorna um objeto **IGroup** da coleção. 
  
### <a name="icontactsubscription-interface"></a>Interface IContactSubscription
<a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a>

A interface **IContactSubscription** permite especificar os contatos que receberão atualizações das informações de presença e os tipos de informações de presença que disparam uma notificação. Os aplicativos do Office usam um objeto **IContactSubscription** para registrar alterações no status de presença do contato. 
  
A Tabela 10 mostra os membros que devem ser implementados nas classes que são herdadas de **IContactSubscription**.
  
> [!NOTE]
> Qualquer membro da interface **IContactSubscription** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.
>
> Para saber mais sobre a interface **IContactSubscription** e seus membros, confira [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription). 
  
**Tabela 10. Implementação da interface IContactSubscription**

|**Membro**|**Descrição**|
|:-----|:-----|
|Método **AddContact**  <br/> |Adiciona um contato ao objeto de inscrição.  <br/> |
|Método **Subscribe**  <br/> |Ajuda o aplicativo cliente de mensagens instantâneas a monitorar a presença de um contato.  <br/> |
   
A interface **IContactSubscription** deve conter uma referência a todos os objetos **IContact** que ela monitora, usando uma matriz ou uma **Lista**. O método **IContactSubscription.AddContact** é adicionado para um objeto **IContact** à estrutura de dados subjacente do objeto **IContactSubscription**, adicionando, assim, um novo contato a ser monitorado em busca de alterações de presença. 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

O método **IContactSubscription.Subscribe** permite que um aplicativo cliente de mensagens instantâneas acesse observadores de presença do contato. Ele pode usar a estratégia de sondagem para obter a presença do servidor dos contatos nos quais o aplicativo cliente de mensagens instantâneas se inscreveu. O método **Subscribe** é útil em situações em que a presença é solicitada para alguém fora da lista de contatos de um usuário (por exemplo, de uma rede pública maior). 
  
### <a name="icontactendpoint-interface"></a>Interface IContactEndPoint
<a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a>

A **IContactEndPoint** representa um número de telefone de uma coleção de números de telefone de um contato. 
  
A Tabela 11 mostra os membros que devem ser implementados nas classes que são herdadas de **IContactEndPoint**.
  
> [!NOTE]
> Qualquer membro da interface **IContactEndPoint** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.
>
> Para saber mais sobre a interface **IContactEndPoint** e seus membros, confira [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint). 
  
**Tabela 11. Implementação da interface IContactEndPoint**

|**Membro**|**Descrição**|
|:-----|:-----|
|Propriedade **DisplayName**  <br/> |Obtém a cadeia de caracteres de exibição.  <br/> |
|Propriedade **Type**  <br/> |Obtém o tipo de ponto de extremidade do contato  <br/> |
|Propriedade **Uri**  <br/> |Obtém URI do contato.  <br/> |
   
### <a name="ilocalestring-interface"></a>Interface ILocaleString
<a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a>

A **ILocaleString** é uma estrutura de cadeia de caracteres localizada que contém uma cadeia de caracteres localizada e a identificação de localidade da localização. A interface **ILocaleString** é usada para formatar a cadeia de caracteres de status personalizada no cartão de visita. 
  
A Tabela 12 mostra os membros que devem ser implementados nas classes que são herdadas de **ILocaleString**.
  
> [!NOTE]
> Qualquer membro da interface **ILocaleString** não listado na tabela deve estar presente, mas não precisa ser implementado. Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.
>
> Para saber mais sobre a interface **ILocalString** e seus membros, confira [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString). 
  
**Tabela 12. Implementação da interface ILocaleString**

|**Membro**|**Descrição**|
|:-----|:-----|
|Propriedade **LocaleId**  <br/> |Obtém a identificação de localidade.  <br/> |
|Propriedade **Value**  <br/> |Obtém a cadeia de caracteres.  <br/> |
   
## <a name="see-also"></a>Confira também

- Namespace [UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) 
    

