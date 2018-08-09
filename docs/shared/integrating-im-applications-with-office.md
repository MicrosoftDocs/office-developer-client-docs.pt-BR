---
title: Integração de aplicativos de mensagens instantâneas com o Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Este artigo descreve como configurar um aplicativo de cliente de mensagem instantânea (IM), para que ele se integra os recursos sociais no Office 2013, incluindo exibindo a presença e enviar mensagens instantâneas do cartão de visita.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771191"
---
# <a name="integrating-im-applications-with-office"></a>Integração de aplicativos de mensagens instantâneas com o Office

Este artigo descreve como configurar um aplicativo de cliente de mensagem instantânea (IM), para que ele se integra os recursos sociais no Office 2013, incluindo exibindo a presença e enviar mensagens instantâneas do cartão de visita.
  
Se você tiver quaisquer dúvidas ou comentários sobre este artigo técnico ou os processos que ele descreve, contate a Microsoft diretamente enviando um email para [docthis@microsoft.com](mailto:docthis@microsoft.com).
  
## <a name="introduction"></a>Introdução
<a name="off15_IMIntegration_Intro"> </a>

Office 2013 fornece integração rica com o cliente de mensagens Instantâneas de aplicativos, incluindo o Lync 2013. Essa integração oferece aos usuários recursos de mensagens Instantâneas de dentro do Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 e OneNote 2013, bem como oferecendo integração de presença em páginas do SharePoint 2013. Os usuários podem ver as fotos, o nome, o status de presença e entre em contato com dados de pessoas em sua lista de contatos. Elas podem começar uma sessão de mensagens Instantâneas, chamada de vídeo ou chamada telefônica diretamente do cartão de visita (o elemento de interface do usuário no Office 2013 que mostra as opções de comunicação e informações de contato). Office 2013 facilita ficar conectado aos seus contatos sem levá-lo fora do seu email ou documentos. 
  
> [!NOTE]
> Este artigo usa o termo aplicativo cliente de mensagens Instantâneas para referir-se especificamente para o aplicativo instalado no computador de um usuário que se comunica com o serviço de mensagens Instantâneas. Por exemplo, Lync 2013 é considerado um aplicativo de cliente de mensagens Instantâneas. Este artigo não fornece detalhes sobre como o aplicativo cliente de mensagens Instantâneas comunica-se ao serviço de mensagens Instantâneas ou sobre o próprio serviço de mensagens Instantâneas. 
  
Você pode personalizar um aplicativo de cliente de mensagens Instantâneas para que ele se comunica com o Office. Especificamente, você pode modificar o seu aplicativo de mensagens Instantâneas para que exiba as seguintes informações na interface do usuário do Office:
  
- Fotos do contato.
    
- Nome do contato.
    
- Entre em contato com a nota de status pessoal.
    
- Entre em contato com o status de presença.
    
- Entre em contato com a cadeia de caracteres de disponibilidade (por exemplo, "Disponível" ou "ausência temporária").
    
- Entre em contato com a cadeia de caracteres de recurso (por exemplo, "vídeo pronto").
    
- Lançamento de mensagens Instantâneas de um clique.
    
- Início da chamada de vídeo de um clique.
    
- Início da chamada telefônica com um clique (incluindo SIP, número de telefone, caixa postal e novo número de chamada).
    
- Gerenciamento de contatos (Adicionar ao grupo de mensagens Instantâneas).
    
- Entre em contato com o local e fuso horário.
    
- Dados de contato, número de telefone, endereço de email, título e nome da empresa.
    
**Figura 1. Cartão de visita no Office 2013**

![O cartão de pessoas no Office 2013] (media/ocom15_peoplecard.png "O cartão de pessoas no Office 2013")
  
Para habilitar essa integração com o Office, um aplicativo de cliente de mensagens Instantâneas deve implementar um conjunto de interfaces que o Office oferece para se conectar a ela. As APIs para essa integração estão incluídas no namespace [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) que está contido no arquivo dll, que é instalado com as versões do Office 2013 que incluem Lync / Skype para negócios. O namespace **UCCollaborationLib** inclui as interfaces que você deve implementar para integração com o Office. 
  
> [!IMPORTANT] 
> Biblioteca de tipos para as interfaces necessárias está incorporada no Lync 2013/Skype para negócios. Para integradores de terceiros, isso funciona apenas quando o Lync 2013 e Skype para negócios estão instalados no computador de destino. Se você estiver integrando usando Office Standard, você precisará extrair a biblioteca de tipos e instalá-lo no computador de destino. O [SDK do Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) inclui o arquivo dll. 
  
> [!NOTE]
>  Um número limitado de aplicativos do Office 2010 pode integrar da mesma forma, com um aplicativo de provedor IM de terceiros: Outlook 2010, o Word 2010, o Excel 2010, o PowerPoint 2010 e o SharePoint Server 2010 (usando um controle ActiveX). Muitas das etapas necessárias para integração com o Office 2013 se aplicam também para o Office 2010. Há várias das principais diferenças em como o Office 2010 é integrado com um aplicativo do provedor de mensagens Instantâneas: 
>  - Office 2010 não exibe fotos do contato. 
>  - Você deve baixar o arquivo DLL separadamente do Office 2010. O [SDK do Lync 2010](http://www.microsoft.com/en-us/download/details.aspx?id=18898) inclui o arquivo DLL para o Office 2010. 
>  - Quando o aplicativo Office chama o método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) no aplicativo do cliente de mensagens Instantâneas, ele passa na cadeia de caracteres "14.0.0.0". 
>  - Office 2010 enumera todos os grupos e contatos assim que ele se conecta a um aplicativo de cliente de mensagens Instantâneas. 
  
## <a name="how-office-integrates-with-an-im-client-application"></a>Como o Office é integrado com um aplicativo de cliente de mensagens Instantâneas
<a name="off15_IMIntegration_How"> </a>

Quando um aplicativo do Office 2013 for iniciado, ele vai através do seguinte processo para integrar com o aplicativo de cliente de mensagens Instantâneas padrão:
  
1. Ele verifica o registro para descobrir o aplicativo de cliente de mensagens Instantâneas padrão e, em seguida, conecta-se a ela.
    
2. Ele autentica com o aplicativo cliente de mensagens Instantâneas.
    
3. Ele se conecta ao interfaces específicas que são expostos pelo aplicativo de cliente de mensagens Instantâneas.
    
4. Ele determina os recursos do usuário conectado (usuário local), incluindo a obtenção de contatos do usuário, determinando a presença do usuário e determinar os recursos de IM do usuário (mensagens instantâneas, conversa com vídeo, VOIP e assim por diante).
    
5. Ela obtém informações de presença de contatos do usuário local.
    
6. Quando o aplicativo cliente de mensagens Instantâneas desligado, o aplicativo do Office 2013 se desconecta silenciosamente.
    
### <a name="discovering-the-im-application"></a>Descobrir o aplicativo de mensagens Instantâneas

O aplicativo Office procura por vários teclas específicas e entradas no registro para descobrir o aplicativo de cliente de mensagens Instantâneas padrão. Se descobrir a um aplicativo de cliente de mensagens Instantâneas padrão e, em seguida, ele tenta se conectar a ela.
  
O processo que o aplicativo Office passa para descobrir o aplicativo de cliente de mensagens Instantâneas padrão é da seguinte maneira:
  
1. O aplicativo Office procura para ver se a subchave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp no registro é definida e lê o nome do aplicativo na lista.
    
2. Em seguida, o aplicativo Office lê a chave de \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _nome do aplicativo_e monitora o valor para que as alterações.
    
3. Em seguida, o aplicativo Office lê a chave de registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _nome do aplicativo_ e obtém os valores de ID (CLSID) Nome_do_processo e a classe armazenados nela. 
    
4. Depois que o aplicativo cliente de mensagens Instantâneas tiver concluído sua sequência iniciar com êxito e registrados todas as classes corretamente para a integração de presença, ele define a chave de \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _nome do aplicativo_para "2" indicando que o aplicativo de cliente está sendo executado.
    
5. Quando o aplicativo Office descobre que a chave de \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _nome do aplicativo_tiver sido definida como "2", ele verificará a lista de processos em execução no computador para que o nome do processo do aplicativo de cliente de mensagens Instantâneas.
    
6. Depois que o aplicativo Office localiza o processo que usa o aplicativo de cliente de mensagens Instantâneas, o aplicativo Office chama **CoCreateInstance** usando o CLSID para estabelecer uma conexão para o aplicativo cliente de mensagens Instantâneas como um servidor de COM fora do processo. 
    
### <a name="authenticating-the-connection-to-the-im-application"></a>Autenticar a conexão para o aplicativo de mensagens Instantâneas

Depois que o aplicativo Office estabelece uma conexão para o aplicativo cliente de mensagens Instantâneas, em seguida, acontece o seguinte:
  
1. O aplicativo Office chama o método de [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) para verificar se há a interface [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) . 
    
2. O aplicativo do Office, em seguida, chama o método **IUCOfficeIntegration.GetAuthenticationInfo** , passando a versão mais recente a integração com suporte (por exemplo, "15.0.0.0"). 
    
3. Se o aplicativo cliente de mensagens Instantâneas suporta a versão do Office passado como um parâmetro, o aplicativo retorna a seguinte sequência XML codificadas ao código de chamada:
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > Por motivos de herança, o aplicativo cliente de mensagens Instantâneas deve retornar o valor exato `<authenticationinfo>` para a chamada para **GetAuthenticationInfo** se ele oferece suporte a versão do Office passado como um parâmetro. 
  
4. Se o aplicativo cliente de mensagens Instantâneas não retorna um valor, o aplicativo Office chama o método **GetAuthenticationInfo** novamente com a próxima versão com suporte mais alto do Office (por exemplo, "14.0.0.0"). 
    
5. Depois que o Office determina que o aplicativo cliente de mensagens Instantâneas oferece suporte a integração de mensagens Instantâneas e presença, ele se conecta a um conjunto necessário das interfaces termine a inicialização. (Para obter mais informações, consulte [Connecting to interfaces necessárias](#off15_IMIntegration_HowConnect).)
    
Se o aplicativo Office encontra um erro em qualquer uma das etapas acima, ele faz o check-out e integração de presença não é estabelecida novamente durante a sessão do aplicativo do Office. 
  
### <a name="connecting-to-required-interfaces"></a>Conectando-se a interfaces necessárias
<a name="off15_IMIntegration_HowConnect"> </a>

Depois de autenticar a conexão para o aplicativo cliente de mensagens Instantâneas, o aplicativo do Office tenta se conectar a um conjunto de interfaces necessárias que o aplicativo cliente de mensagens Instantâneas deve expor. O aplicativo Office realiza isso fazendo o seguinte:
  
- O aplicativo Office obtém um objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) chamando o método **IUCOfficeIntegration.GetInterface** , passando o **oiInterfaceLyncClient** constante da enumeração [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) . 
    
- O aplicativo Office obtém um objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) chamando o método **IUCOfficeIntegration.GetInterface** , passando o **oiInterfaceAutomation** constante da enumeração **OIInterface** . 
    
- O aplicativo Office configura o ouvinte de eventos [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) . 
    
- O aplicativo Office configura o ouvinte de eventos [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) . 
    
- O aplicativo Office obtém o estado de entrada do aplicativo de cliente de mensagens Instantâneas, acessando a propriedade **ILyncClient.State** . 
    
- O aplicativo Office obtém os recursos do aplicativo cliente IM chamando o método **IUCOfficeIntegration.GetSupportedFeatures** , que retorna um sinalizador provenientes da enumeração [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) . 
    
- O aplicativo Office acessa a propriedade **ILyncClient.Self** para obter uma referência a um objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) . 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a>Recuperando os recursos do usuário local
<a name="off15_IMIntegration_HowConnect"> </a>

O aplicativo Office obtém os recursos do usuário local, fazendo o seguinte:
  
1. Se o aplicativo cliente de mensagens Instantâneas dá suporte à interface **IClient2** , Office tentará obter um objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) acessando a propriedade **IClient2.PrivateContactManager** . 
    
2. Se o aplicativo de mensagens Instantâneas não oferece suporte para a interface **IClient2** , o aplicativo Office obtém um objeto de **IContactManager** acessando a propriedade **ILyncClient.ContactManager** . O aplicativo cliente de mensagens Instantâneas com êxito deve retornar um objeto **IContactManager** antes que quaisquer outros recursos de mensagem Instantânea podem ser estabelecidos. 
    
3. O aplicativo Office acessa a propriedade **ILyncClient.Uri** e, em seguida, chama **IContactManager.GetContactByUri** para obter o objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) associado ao usuário local. 
    
4. O aplicativo do Office, em seguida, faz várias chamadas para **IContact.CanStart** para estabelecer as capacidades do usuário local, passando os valores para **ModalityTypes.ucModalityInstantMessage** e **ModalityTypes.ucModalityAudioVideo** sucessivamente. 
    
### <a name="retrieving-contact-presence"></a>Recuperando a presença de contato
<a name="off15_IMIntegration_HowConnect"> </a>

O aplicativo Office obtém a presença de contato, incluindo o usuário local, fazendo o seguinte: 
  
1. O aplicativo Office chama **IContact.GetContactInformation** para obter um item de presença do contato. 
    
2. Em seguida, o aplicativo do Office se inscreve para alteração de status de presença do contato. Ela chama **IContactManager.CreateSubscription** para obter um objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) . Ela chama **IContactSubscription.AddContact** para adicionar o contato à assinatura de e, em seguida, chama **IContactSubscription.Subscribe** para fazer alterações no status do contato. 
    
3. Se o aplicativo de mensagens Instantâneas suporta **IContact2**, Office tenta obter informações de presença chamando **IContact2.BatchGetContactInformation2**.
    
4. O aplicativo do Office, em seguida, recupera as propriedades de presença do contato chamando **IContact.BatchGetContactInformation**. O aplicativo do Office pode obter um segundo conjunto de propriedades de presença, acessando a propriedade **IContact.Settings** . 
    
5. Finalmente, o aplicativo Office obtém a associação de grupo do contato acessando a propriedade **IContact.CustomGroups** . Isso retorna uma coleção de [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que inclui todos os objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que o contato pertencer a. 
    
### <a name="disconnecting-from-the-im-application"></a>Desconectar-se de que o aplicativo de mensagens Instantâneas
<a name="off15_IMIntegration_HowConnect"> </a>

Quando o aplicativo do Office 2013 detecta o evento **OnShuttingDown** do aplicativo de mensagens Instantâneas, ele desconecta silenciosamente. No entanto, se o aplicativo Office desligado antes que o aplicativo de mensagens Instantâneas, o aplicativo do Office não garante que a conexão é limpos. O aplicativo de mensagens Instantâneas deve tratar vazamento de conexão do cliente. 
  
## <a name="setting-registry-keys-and-entries"></a>Entradas e chaves de registro de configuração
<a name="off15_IMIntegration_SetRegistry"> </a>

Conforme mencionado anteriormente, os aplicativos do Office com capacidade para mensagens Instantâneas 2013 procuram teclas específicas, entradas e valores do registro para descobrir o aplicativo cliente de mensagens Instantâneas para se conectar ao. Esses valores do registro fornecem o aplicativo do Office com o nome de processo e o CLSID da classe que atua como o ponto de partida para o modelo de objeto do aplicativo de cliente de mensagens Instantâneas (ou seja, a classe que implementa a interface **IUCOfficeIntegration** ). O aplicativo Office co cria essa classe e conecta-se como um cliente no servidor fora do processo COM o aplicativo cliente de mensagens Instantâneas. 
  
Use a tabela 1 para identificar as chaves, entradas e valores que precisam ser gravados no registro para integrar um aplicativo de cliente de mensagens Instantâneas com o Office.
  
**Tabela 1. Chaves do registro para configurar o aplicativo de cliente de mensagens Instantâneas padrão**

|**Key**|**Entry**|**Tipo de**|**Valor**|**Exemplo**|
|:-----|:-----|:-----|:-----|:-----|
|Provedores de HKEY_LOCAL_MACHINE\Software\IM\\< nome do aplicativo\>  <br/> |FriendlyName  <br/> |REG_SZ  <br/> |O nome do aplicativo de cliente IM de terceiros.  <br/> |Litware IM 2012  <br/> |
||Nome_do_processo  <br/> |REG_SZ  <br/> |O nome do processo do aplicativo de cliente IM de terceiros.  <br/> |Litware.exe  <br/> |
||GUID  <br/> |REG_SZ  <br/> |Uma ID da classe (CLSID) para a raiz, a classe cocreatable no aplicativo de mensagens Instantâneas (a classe que implementa a interface **IUCOfficeIntegration** ).  <br/> |(UMA GUID)  <br/> |
|Provedores de HKEY_CURRENT_USER\Software\IM  <br/> |DefaultIMApp  <br/> |REG_SZ  <br/> |O nome do aplicativo de cliente de mensagens Instantâneas. Isso deve ser o mesmo que o nome da chave do registro de nível superior (hive) na HKEY_LOCAL_MACHINE.  <br/> |Litware  <br/> |
|Provedores de HKEY_CURRENT_USER\Software\IM\\< nome do aplicativo\>  <br/> |UpAndRunning  <br/> |REG_DWORD  <br/> | Um valor inteiro entre 0 e 2:  <br/>  0 — não funcionando  <br/>  1 — Iniciando  <br/>  2 — executando  <br/> <br/>**Observação**: A chave de registro de nome do aplicativo deve ser o mesmo que o valor da entrada DefaultIMApp.           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a>Implementando as interfaces necessárias para integração com o Office
<a name="off15_IMIntegration_ImplementRequired"> </a>

Existem três interfaces do namespace **UCCollaborationLib** executável (ou servidor COM) de um aplicativo de cliente de mensagens Instantâneas deve implementar para que ele pode se integrar com o Office. Se essas interfaces não são implementadas, o aplicativo Office faz o check-out durante o processo de inicialização e a conexão com o aplicativo cliente de mensagens Instantâneas não é estabelecida. 
  
As interfaces necessárias são:
  
- [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)— Embora não seja obrigatório, a interface **_IUCOfficeIntegrationEvents** também deve ser implementada na mesma classe derivada. 
    
- [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)— Embora não seja obrigatório, a interface **_ILyncClientEvents** também deve ser implementada na mesma classe derivada. 
    
- [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a>Interface de IUCOfficeIntegration
<a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a>

A interface de **IUCOfficeIntegration** fornece o ponto de entrada para um aplicativo do Office para se conectar ao aplicativo de cliente de mensagens Instantâneas. A interface define três métodos que chama um aplicativo do Office como parte do processo de iniciar uma conexão com o aplicativo cliente de mensagens Instantâneas. A classe que implementa a interface **IUCOfficeIntegration** deve ser co creatable para que o Office co pode criar uma instância dele. Além disso, ele deve expor o CLSID que é inserido como o valor para a entrada GUID na chave do registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _nome do aplicativo_ . 
  
A classe que herda de **IUCOfficeIntegration** também deve implementar a interface **_IUCOfficeIntegrationEvents** . A interface de **_IUCOfficeIntegrationEvents** contém os membros que exponham os manipuladores de eventos da interface **IUCOfficeIntegration** . 
  
Tabela 2 mostra os membros que devem ser implementados na classe que herda de **IUCOfficeIntegration** e **_IUCOfficeIntegration**.
  
> [!NOTE]
> Para obter mais informações sobre o **IUCOfficeIntegration** e interfaces **_IUCOfficeIntegrationEvents** e seus membros, consulte [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) e [UCCollaborationLib._IUCOfficeIntegrationEvents ](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents). 
  
**Tabela 2. Implementação das interfaces IUCOfficeIntegration e _IUCOfficeIntegrationEvents**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**IUCOfficeIntegration** <br/> |Método **GetAuthenticationInfo**  <br/> |Obtém a sequência de informações de autenticação.  <br/> |
||Método **GetInterface**  <br/> |Obtém a interface de uma versão específica.  <br/> |
||Método **GetSupportedFeatures**  <br/> |Obtém os recursos de integração do Office com suporte.  <br/> |
|**_IUCOfficeIntegrationEvents** <br/> |Evento **OnShuttingDown**  <br/> |O evento acionado quando o aplicativo cliente de mensagens Instantâneas está tentando desligar.  <br/> |
   
Use o código a seguir para definir uma classe que os herda as interfaces **IUCOfficeIntegration** e **_IUCOfficeIntegration** dentro de um aplicativo de cliente de mensagens Instantâneas. 
  
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

O método de **GetAuthenticationInfo** aceita uma cadeia de caracteres como um argumento para o parâmetro de _versão_ . Quando o aplicativo Office chama esse método, ele passa de uma das duas cadeias de caracteres para o argumento, dependendo da versão do Office. Quando o aplicativo Office fornece o método com a versão do Office que suporta o aplicativo cliente de mensagens Instantâneas (ou seja, suporta a funcionalidade), o método **GetAuthenticationInfo** retorna uma cadeia de caracteres XML codificadas `<authenticationinfo>`. 
  
Use o código a seguir para implementar o método **GetAuthentication** dentro do código de aplicativo do cliente de mensagens Instantâneas. 
  
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

O método **GetInterface** coloca referências às classes ao código de chamada, dependendo de qual é passado como um argumento para o parâmetro de _interface_ . Quando um aplicativo do Office chama o método **GetInterface** , passa em um dos dois valores para o parâmetro interface: a constante **oiInterfaceILyncClient** (1) ou a constante **oiInterfaceIAutomation** (2) do [ UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeração. Se o aplicativo Office passa na constante **oiInterfaceILyncClient** , o método **GetInterface** retorna uma referência a uma classe que implementa a interface **ILyncClient** . Se o aplicativo Office passa na constante **oiInterfaceIAutomation** , o método **GetInterface** retorna uma classe que implementa a interface **IAutomation** . 
  
Use o exemplo de código a seguir para implementar o método **GetInterface** dentro do código de aplicativo do cliente de mensagens Instantâneas. 
  
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

O método **GetSupportedFeatures** retorna informações sobre os recursos de mensagens Instantâneas que suporta o aplicativo cliente de mensagens Instantâneas. Leva uma cadeia de caracteres para seu único parâmetro, a _versão_. Quando o aplicativo Office chama o método **GetSupportFeatures** , o método retorna um valor da enumeração [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) . O valor retornado especifica os recursos do cliente de mensagens Instantâneas, onde cada recurso do aplicativo de cliente de mensagens Instantâneas é indicado para o aplicativo do Office, adicionando um sinalizador com o valor. 
  
> [!NOTE]
>  Aplicativos do Office 2013 ignoram as seguintes constantes na enumeração **OIFeature** : 
> - **oiFeaturePictures** (2) 
> - **oiFeatureFreeBusyIntegration**
> - **oiFeaturePhoneNormalization**
  
Use o exemplo de código a seguir para implementar o método **GetSupportFeatures** dentro do código de aplicativo do cliente de mensagens Instantâneas. 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a>Interface de ILyncClient
<a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a>

A interface **ILyncClient** mapeia para os recursos do aplicativo de cliente de mensagens Instantâneas em si. Ele expõe as propriedades que se referem a pessoa que está conectada ao aplicativo (o usuário local, representado pela interface [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) ), o estado do aplicativo, a lista de contatos, a para o usuário local e várias outras configurações. Quando ele tenta se conectar ao aplicativo de cliente de mensagens Instantâneas, o aplicativo Office obtém uma referência a um objeto que implementa a interface **ILyncClient** . Essa referência, Office pode acessar grande parte da funcionalidade do aplicativo de cliente de mensagens Instantâneas. 
  
Além disso, a classe que implementa a interface **ILyncClient** também deve implementar a interface **_ILyncClientEvents** . A interface **_ILyncClientEvents** expõe vários eventos que são necessários para o monitoramento do estado do aplicativo de cliente de mensagens Instantâneas. 
  
A tabela 3 mostra os membros que devem ser implementados na classe que herda de **ILyncClient** e **_ILyncClientEvents**.
  
> [!NOTE]
> Qualquer membro do **ILyncClient** ou ** \_ILyncClientEvents** interface não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar uma **NotImplementedException** ou **f\_NOTIMPL** erro. 
> 
> Para obter mais informações sobre o **ILyncClient** e interfaces **_ILyncClientEvents** e seus membros, consulte [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) e [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents). 
  
**Tabela 3. Implementação das interfaces ILyncClient e ILyncClientEvents**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**ILyncClient** <br/> |Propriedade **ContactManager**  <br/> |Obtém o gerente de grupo de contatos.  <br/> |
||Propriedade **ConversationManager**  <br/> |Obtém o Gerenciador de conversas.  <br/> |
||Propriedade **Self**  <br/> |Obtém o objeto **Self** .  <br/> |
||Método de **logon**  <br/> |Inicia o aplicativo de cliente de mensagens Instantâneas entrar processo com uma disponibilidade específica.  <br/> |
||Propriedade **State**  <br/> |Obtém o estado atual da plataforma.  <br/> |
||Propriedade **URI**  <br/> |Obtém o URI do aplicativo de cliente de mensagens Instantâneas.  <br/> |
|**_ILyncClientEvents** <br/> |Evento **OnStateChanged**  <br/> |Gerado quando o estado de aplicativo do cliente de mensagens Instantâneas é alterado. Você deve lidar com esse evento e obter a propriedade **eventData.NewState** . O evento é disparado para todos os processos vinculados a uma instância de um aplicativo de cliente de mensagens Instantâneas quando qualquer subsistema no aplicativo faz com que a alteração de estado.  <br/> |
   
Durante o processo de inicialização, Office acessa a propriedade **ILyncClient.State** . Esta propriedade deve retornar um valor da enumeração [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) . 
  
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

A propriedade **State** armazena o status atual do aplicativo de cliente de mensagens Instantâneas. Deve ser definido e atualizado em toda a sessão de aplicativo do cliente de mensagens Instantâneas. Quando a mensagem Instantânea aplicativo cliente entra no, desconecta-se ou desligado, ele deve definir a propriedade **State** . É melhor definir essa propriedade dentro os métodos **ILyncClient.SignIn** e **ILyncClient.SignOut** , como o exemplo a seguir demonstra. 
  
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

O exemplo de código a seguir demonstra como configurar o ouvinte de eventos usando o _ **ILyncClientEvents** e _ **IUCOfficeIntegrationEvents** interfaces. 
  
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

### <a name="iautomation-interface"></a>Interface de IAutomation
<a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a>

A interface **IAutomation** automatiza recursos do aplicativo de cliente de mensagens Instantâneas. Ele pode ser usado para iniciar conversas, ingressar em conferências e fornecer um contexto de janela de extensibilidade. 
  
A tabela 4 mostra os membros que devem ser implementados na classe que herda de **IAutomation**.
  
> [!NOTE]
> Qualquer membro da interface **IAutomation** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** . 
> 
> Para obter mais informações sobre a interface **IAutomation** e seus membros, consulte [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation). 
  
**Tabela 4. Implementação da interface IAutomation**

|**Membro**|**Descrição**|
|:-----|:-----|
|Método **StartConversation**  <br/> |Inicia uma conversa usando a modalidade de conversa especificado. Uma instância de **IConversationWindow** é retornada.  <br/> |
   
## <a name="implementing-contact-presence-integration"></a>Implementando a integração de presença do contato
<a name="off15_IMIntegration_ImplementIMFeatures"> </a>

Além das interfaces obrigatórias três discutidas anteriormente, existem várias outras interfaces que são importantes para habilitar a funcionalidade de presença de contato no Office. Isso inclui o seguinte:
  
- A interface [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) ou **IContact2** . 
    
- A interface [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) . 
    
- As interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) e [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) . 
    
- As interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) e [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) . 
    
- A interface [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) . 
    
- A interface [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) . 
    
- A interface [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) 
    
### <a name="icontact-interface"></a>Interface de IContact
<a name="off15_IMIntegration_ImplementRequired_IContact"> </a>

A interface **IContact** representa um usuário de aplicativo do cliente de mensagens Instantâneas. A interface expõe a presença, pelas modalidades disponíveis, a associação ao grupo e as propriedades de tipo de contato para um usuário. Para iniciar uma conversa com outro usuário, você deve fornecer essa instância do usuário do **IContact**.
  
Tabela 5 mostra os membros que devem ser implementados na classe que herda de **IContact**.
  
> [!NOTE]
> Qualquer membro da interface **IContact** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** . 
>
> Para obter mais informações sobre a interface **IContact** e seus membros, consulte [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact). 
  
**Tabela 5. Implementação da interface IContact**

|**Membro**|**Descrição**|
|:-----|:-----|
|Método **CanStart**  <br/> |Retorna **true** se um determinado tipo de modalidade pode ser iniciado no contato.  <br/> |
|Método **GetContactInformation**  <br/> |Obtém um item de presença de um contato de publicação.  <br/> |
|Método **BatchGetContactInformation**  <br/> |Obtém a vários itens de presença de um contato de publicação.  <br/> |
|Propriedade **Settings**  <br/> |Obtém uma coleção de propriedades do contato.  <br/> |
|Propriedade **CustomGroups**  <br/> |Obtém uma coleção dos grupos que o contato é um membro de.  <br/> |
   
Durante o processo de inicialização, o aplicativo Office chama o método **IContact.CanStart** para determinar os recursos de mensagens Instantâneas para o usuário local. O método **CanStart** leva um sinalizador provenientes da enumeração [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como um argumento para o parâmetro de_modalityTypes_ _. Se o usuário atual pode participar a modalidade solicitada (ou seja, o usuário é capaz de mensagens instantâneas, áudio e vídeo de mensagens ou compartilhamento de aplicativos), o método **CanStart** retorna **true**.
  
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

O método **GetContactInformation** recupera informações sobre o contato do objeto **IContact** . O código de chamada precisa passar um valor da enumeração [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para o parâmetro_contactInformationType_ _, que indica os dados a ser recuperado. 
  
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

Assim como o **GetContactInformation**, o método **BatchGetContactInformation** recupera vários itens de presença sobre o contato do objeto **IContact** . O código de chamada precisa passar uma matriz de valores da enumeração **ContactInformationType** para o parâmetro de_contactInformationTypes_ _. O método retorna um objeto de [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contém os dados solicitados. 
  
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

A propriedade **IContact.Settings** retorna um objeto de **IContactSettingDictionary** que contém as propriedades personalizadas sobre o contato. 
  
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

A propriedade **IContact.CustomGroups** retorna um objeto **IGroupCollection** que inclui todos os grupos dos quais o contato é membro. 
  
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

### <a name="iself-interface"></a>Interface de ISelf
<a name="off15_IMIntegration_ImplementRequired_ISelf"> </a>

Durante o processo de inicialização, o aplicativo Office obtém os dados para o usuário atual, acessando a propriedade **ILyncClient.Self** , que deve retornar um objeto **ISelf** . A interface **ISelf** representa o usuário de aplicativo de cliente de mensagens Instantâneas de local, conectado. 
  
Tabela 6 mostra os membros que devem ser implementados na classe que herda de **ISelf**.
  
> [!NOTE]
> Qualquer membro da interface **ISelf** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** . 
  
**Tabela 6. Implementação da interface ISelf**

|**Membro**|**Descrição**|
|:-----|:-----|
|Propriedade **Contact**  <br/> |Obtém o objeto **IContact** associado ao usuário local.  <br/> |
   
Presença, pelas modalidades disponíveis, a associação ao grupo e as propriedades de tipo de contato para o usuário local são expostas por meio da propriedade **ISelf.Contact** (que retorna um objeto **IContact** ). Durante o processo de inicialização, o aplicativo Office acessa a propriedade **ISelf.Contact** para obter uma referência para as informações de contato para o usuário local. 
  
Use o código a seguir para definir uma classe que herda da interface **ISelf** que implementa a propriedade do **contato** . 
  
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

O objeto **IContactManager** gerencia os contatos do usuário local, incluindo as informações de contato do local do próprio usuário. O aplicativo Office usa um objeto **IContactManager** para acessar objetos de **IContact** que correspondem aos contatos do usuário local. 
  
A tabela 7 mostra os membros que devem ser implementados na classe que herda de **IContactManager** e **_IContactManagerEvents**.
  
> [!NOTE]
> Qualquer membro da interface **IContactManager** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar uma **NotImplementedException** ou **f\_NOTIMPL** erro. 
>
> Para obter mais informações sobre o **IContactManager** e interfaces **_IContactManagerEvents** e seus membros, consulte [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) e [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents). 
  
**A tabela 7. Implementação das interfaces IContactManager e _IContactManagerEvents**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**IContactManager** <br/> |Método **GetContactByUri**  <br/> |Localiza ou cria uma nova instância de contato usando o URI do contato.  <br/> |
||Método **CreateSubscription**  <br/> |Cria um objeto **ISubscription** que pode ser usado para processamento em lotes assinaturas ou consultas.  <br/> |
||Método **proc**  <br/> |Pesquise um contato ou grupo de distribuição.  <br/> |
|**_IContactManagerEvents** <br/> |Evento **OnGroupAdded**  <br/> |Acionado quando um grupo é adicionado a uma coleção de grupo. A coleção de grupo atualizados pode ser obtida da propriedade **IContactManager.Groups** .  <br/> |
||Evento **OnGroupRemoved**  <br/> |Acionado quando um grupo é removido de uma coleção de grupo. A coleção de grupo atualizados pode ser obtida da propriedade **IContactManager.Groups** .  <br/> |
||Evento **OnSearchProviderStateChanged**  <br/> |Acionado quando o status do provedor de pesquisa for alterado.  <br/> |
   
O Office chama **IContactManager.GetContactByUri** para obter informações de presença de um contato, usando o endereço SIP do contato. Quando um contato estiver configurado para um endereço SIP no Active Directory, o Office determina esse endereço para um contato e chamadas **GetContactByUri**, passando o endereço SIP do contato no parâmetro __contactUri_ . 
  
Quando o Office não puder determinar o endereço SIP do contato, ele chama o método **IContactManager.Lookup** para localizar o SIP usando o serviço de mensagens Instantâneas. Aqui Office passa nos dados recomendados que ele possa encontrar para o contato (por exemplo, apenas o endereço de email do contato). O método **Lookup** assincronamente retorna um objeto **AsynchronousOperation** . Quando invoca o retorno de chamada, o método de **pesquisa** deve retornar o êxito ou falha da operação além o URI do contato. 
  
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

O aplicativo do Office precisa se inscrever para alterações de presença para um contato individual. Assim, quando o status de presença do contato for alterado, o servidor de mensagens Instantâneas avisa o aplicativo cliente de mensagens Instantâneas — alertas, portanto, o aplicativo do Office. Para fazer isso, o aplicativo Office chama o método **IContactManager.CreateSubscription** para criar um novo objeto de **IContactSubscription** para essa solicitação. 
  
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

O objeto **IGroup** representa uma coleção de contatos com propriedades adicionais para identificar o conjunto de contatos por nome de um grupo coletivo. Um objeto **IGroupCollection** representa uma coleção de objetos **IGroup** definido por um usuário local e o aplicativo de cliente de mensagens Instantâneas. O aplicativo do Office usa os objetos **IGroupCollection** e **IGroup** para acessar os contatos do usuário local. 
  
A tabela 9 mostra os membros que devem ser implementados nas classes que herdam **IGroup** e **IGroupCollection** na tabela a seguir. 
  
> [!NOTE]
> Qualquer membro da interface **IGroup** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** . 
>
> Para obter mais informações sobre as interfaces **IGroup** e **IGroupCollection** e seus membros, consulte [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) e [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection). 
  
**A tabela 9. Implementação das interfaces IGroup e IGroupCollection**

|**Interface**|**Membro**|**Descrição**|
|:-----|:-----|:-----|
|**IGroupCollection** <br/> |Propriedade **Count**  <br/> |Retorna a contagem de objetos **IGroup** na coleção  <br/> |
||Propriedade **item**  <br/> |Retorna o objeto **IGroup** no índice especificado na coleção.  <br/> |
|**IGroup** <br/> |Propriedade **ID**  <br/> |Retorna a identificação do grupo.  <br/> |
   
Quando o aplicativo Office obtém as informações do usuário local, ele acessa as associações de grupo do contato (usuário local) chamando-se a propriedade **IContact.CustomGroups** , que retorna um objeto **IGroupCollection** . O **IGroupCollection** deve conter uma matriz (ou **lista**) de objetos **IGroup** . A classe derivada de **IGroupCollection** deve expor uma propriedade **Count** , que retorna o número de itens na coleção e um método de indexador, **this(int)**, que retorna um objeto **IGroup** da coleção. 
  
### <a name="icontactsubscription-interface"></a>Interface de IContactSubscription
<a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a>

A interface **IContactSubscription** permite que você especifique os contatos para receber notificações e atualizações de informações de presença para os tipos de informações de presença que acionam uma notificação. Aplicativos do Office usam um objeto **IContactSubscription** para registrar as alterações para o status de presença do contato. 
  
A tabela 10 mostra os membros que devem ser implementados nas classes que herdam **IContactSubscription**.
  
> [!NOTE]
> Qualquer membro da interface **IContactSubscription** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .
>
> Para obter mais informações sobre a interface **IContactSubscription** e seus membros, consulte [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription). 
  
**Tabela 10. Implementação da interface IContactSubscription**

|**Membro**|**Descrição**|
|:-----|:-----|
|Método **AddContact**  <br/> |Adiciona um contato para o objeto de inscrição.  <br/> |
|Método **Subscribe**  <br/> |Ajuda o aplicativo cliente de mensagens Instantâneas para monitorar a presença de um contato.  <br/> |
   
A interface **IContactSubscription** deve conter uma referência a todos os objetos **IContact** monitora, usando uma matriz ou uma **lista**. O método **IContactSubscription.AddContact** adiciona um objeto **IContact** para na estrutura de dados subjacente do objeto **IContactSubscription** , assim, adicionando um novo contato para o monitoramento de alterações de presença. 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

O método **IContactSubscription.Subscribe** permite que um aplicativo cliente de mensagens Instantâneas acessar observadores de presença do contato. Ele pode usar uma estratégia de sondagem para obter que as informações de presença do servidor para os contatos para que o aplicativo cliente de mensagens Instantâneas assinou. O método **Subscribe** é útil em situações onde a presença é solicitada para alguém de fora da lista de contatos do usuário (por exemplo, a partir de uma rede pública maior). 
  
### <a name="icontactendpoint-interface"></a>Interface de IContactEndPoint
<a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a>

O **IContactEndPoint** representa um número de telefone da coleção de um contato de números de telefone. 
  
A tabela 11 mostra os membros que devem ser implementados nas classes que herdam **IContactEndPoint**.
  
> [!NOTE]
> Qualquer membro da interface **IContactEndPoint** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .
>
> Para obter mais informações sobre a interface **IContactEndPoint** e seus membros, consulte [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint). 
  
**A tabela 11. Implementação da interface IContactEndPoint**

|**Membro**|**Descrição**|
|:-----|:-----|
|Propriedade **DisplayName**  <br/> |Obtém a cadeia de caracteres de exibição.  <br/> |
|Propriedade **Type**  <br/> |Obtém o tipo de contato do ponto de extremidade  <br/> |
|Propriedade **URI**  <br/> |Obtém o URI do contato.  <br/> |
   
### <a name="ilocalestring-interface"></a>Interface de ILocaleString
<a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a>

O **ILocaleString** é uma estrutura de cadeia de caracteres localizada que contém uma cadeia de caracteres localizada e a identificação de localidade da localização. A interface de **ILocaleString** é utilizada para formatar a cadeia de caracteres de status personalizados no cartão de visita. 
  
12 de tabela mostra os membros que devem ser implementados nas classes que herdam **ILocaleString**.
  
> [!NOTE]
> Qualquer membro da interface **ILocaleString** não listado na tabela deve estar presente, mas não precisará ser implementado. Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .
>
> Para obter mais informações sobre a interface **ILocalString** e seus membros, consulte [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString). 
  
**A tabela 12. Implementação da interface ILocaleString**

|**Membro**|**Descrição**|
|:-----|:-----|
|Propriedade **LocaleId**  <br/> |Obtém a ID de localidade.  <br/> |
|Propriedade **Value**  <br/> |Obtém a cadeia de caracteres.  <br/> |
   
## <a name="see-also"></a>Confira também

- Namespace [UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib) 
    

