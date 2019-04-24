---
title: Elementos de XML de recursos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: As tabelas neste tópico descrevem elementos filho do XML de recursos e estão agrupadas pelas áreas às quais oferecem suporte.
ms.openlocfilehash: 6816bbdcd24eceffc47d6b9d0835a90c7089c039
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281181"
---
# <a name="capabilities-xml-elements"></a>Elementos XML de recursos

As tabelas neste tópico descrevem elementos filho do XML de **recursos** e estão agrupadas pelas áreas às quais oferecem suporte. O valor padrão de cada elemento **capabilities** é **false**. Se o elemento não for especificado no XML de **recursos** retornados pelo método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), o valor do elemento será igual a **false**.
  
Para obter uma descrição geral do XML de **recursos**, consulte [XML para recursos](xml-for-capabilities.md). Para obter um exemplo do XML de **recursos**, consulte [Exemplo do XML de recursos](capabilities-xml-example.md). Para obter uma definição completa do esquema XML do provedor Microsoft OSC (Outlook Social Connector), incluindo quais elementos são obrigatórios ou opcionais, consulte [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Recursos para suporte a amigos

A tabela a seguir mostra elementos que se aplicam a qualquer forma de sincronização de amigos ou não amigos.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Indica se o provedor oferece suporte para a chamada do método [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md).  <br/> **followPerson** e **doNotFollowPerson** são recursos independentes de um provedor OSC. Um provedor OSC pode indicar a capacidade de adicionar uma pessoa como amigo (definindo **followPerson** como **true**) ou de remover uma pessoa como amigo em uma conta de rede social (definindo **doNotFollowPerson** como **true**). Em geral, ser capaz de seguir não significa ser capaz de parar de seguir. **followPerson** é um recurso e não deve ser mal interpretado como uma ação para seguir uma pessoa específica ou todas as pessoas na conta de rede social. A definição de **followPerson** como **true** não implica que **doNotFollowPerson** seja **false**.  <br/> |
|**followPerson** <br/> |Indica se o provedor oferece suporte para a chamada do método [ISocialSession::FollowPerson](isocialsession-followperson.md). O OSC verifica em **followPerson** se **cacheFriends** é **true** (sincronização de amigos em cache), se **dynamicContactsLookup** é **true** (sincronização de amigos e não amigos sob demanda) ou se ambos **cacheFriends** e **dynamicContactsLookup** são true (sincronização híbrida de amigos e não amigos). Se o provedor definir **followPerson** como **true**, o OSC exibirá um selo de rede no Painel de Pessoas para as pessoas que o usuário está seguindo e ativará o comando **on \<NetworkName\>** no menu **Adicionar (+)** do Painel de Pessoas. Se o provedor definir **followPerson** como **false**, o selo de rede não será exibido, e o comando **on \<NetworkName\>** será oculto.  <br/> |
|**getFriends** <br/> |Indica se o provedor oferece suporte para a chamada do método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) ou [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md). Se o provedor definir **getFriends** como **true**, o OSC usará o valor de **cacheFriends** ou **dynamicContactsLookup** para determinar se a rede social permite o armazenamento de amigos como itens de contato do Outlook ou na memória. Se o provedor definir **getFriends** como **false**, a rede social não oferecerá suporte a amigos e aos métodos **ISocialPerson::GetFriendsAndColleagues** e **ISocialSession2::GetPeopleDetails**, e o OSC ignorará os valores de **cacheFriends** e **dynamicContactsLookup**.  <br/> |
   
Os elementos a seguir aplicam-se apenas à sincronização em cache de amigos ou à sincronização híbrida de amigos e não amigos. Para obter mais informações sobre como sincronizar amigos, consulte [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md).
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**cacheFriends** <br/> |Indica se o provedor OSC permite armazenar amigos como itens de contato do Outlook. O OSC verifica **cacheFriends** somente quando **getFriends** é **true**. Se o provedor definir **cacheFriends** como **true**, o OSC sincronizará amigos via armazenamento em cache e criará uma pasta de contatos específicos da rede no repositório padrão do usuário para contatos de amigos. O nome da pasta de contatos específica da rede é o valor da propriedade [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). Se o provedor definir **cacheFriends** como **false**, o OSC não criará uma pasta de contatos específica da rede para contatos de amigos para armazenar amigos.  <br/> |
|**contactSyncRestartInterval** <br/> |Determina o intervalo de repetição, em minutos, entre tentativas de sincronizar as informações de amigos da rede social se um erro de sincronização ocorrer. O OSC usará esse elemento somente se o provedor OSC oferecer suporte à sincronização em cache ou à sincronização híbrida de amigos com uma pasta de contatos específica da rede social (**cacheFriends** é **true**).  <br/> O intervalo de repetição padrão é de 30 minutos, a menos que o padrão seja substituído pela chave `ContactSyncRestartInterval` em `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`. Se o provedor definir **contactSyncRestartInterval**, o valor do provedor substituirá o intervalo de repetição padrão de 30 minutos ou o valor da chave do Registro.  <br/> Para obter mais informações sobre como sincronizar informações de amigos e não amigos sob demanda, consulte [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md).  <br/> |
   
Os elementos a seguir aplicam-se apenas à sincronização sob demanda ou à sincronização híbrida de amigos e não amigos.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Indica se o provedor OSC oferece suporte à chamada [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) para sincronização sob demanda de amigos e não amigos.  <br/> O OSC verificará **dynamicContactsLookup** apenas se **getFriends** for **true**. A configuração padrão para **dynamicContactsLookup** é **false**.  <br/> Se o provedor OSC especificar **dynamicContactsLookup** como **true** e **getFriends** como **true**, o OSC chamará **ISocialSession2::GetPeopleDetails** sempre que o Painel de Pessoas for atualizado. O Painel de Pessoas é atualizado quando o usuário seleciona outro usuário nele ou outro item na janela do explorador do Outlook ou quando abre uma janela do inspetor do Outlook. A pesquisa de contatos dinâmicos garante que o usuário sempre veja as fotos do usuário e suas informações de perfil mais recentes no Painel de Pessoas, mas aumenta o número de chamadas do provedor para a rede social.  <br/> Se o provedor definir **dynamicContactsLookup** como **false**, o OSC não chamará **ISocialSession2::GetPeopleDetails** para atualizar o Painel de Pessoas.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Indica se o OSC deve realizar a sincronização sob demanda para amigos e não amigos quando o Painel de Pessoas é minimizado.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Recursos para suporte a atividades

O elemento a seguir aplica-se a qualquer forma de sincronização de atividades com suporte pelo provedor OSC.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**getActivities** <br/> |Indica se o provedor oferece suporte para as chamadas do método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) ou [ISocialPerson::GetActivities](isocialperson-getactivities.md). Se o provedor definir **getActivities** como **true**, o OSC usará o valor de **cacheActivities** ou **dynamicActivitiesLookupEx** para determinar se o site da rede social permite o armazenamento de atividades como itens RSS do Outlook ou como atividades na memória. Se o provedor definir **getActivities** como **false**, a rede social não oferecerá suporte a atividades e aos métodos **ISocialSession2::GetActivitiesEx** e **ISocialPerson::GetActivities**, e o OSC ignorará os valores de **cacheActivities** e **dynamicActivitiesLookupEx**.  <br/> |
   
O elemento a seguir aplica-se apenas à sincronização em cache ou à sincronização híbrida de atividades.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**cacheActivities** <br/> |Começando com o Outlook Social Connector 2013, o OSC ignora esse elemento, pois os provedores não podem mais sincronizar atividades armazenando-as em cache em uma pasta oculta no repositório do usuário.  <br/> Se o provedor oferecer suporte para atividades, ele deverá oferecer suporte à sincronização de atividades sob demanda. O provedor define **cacheActivities** como **false** e **dynamicActivitesLookupEx** como **true**. O OSC sincroniza atividades sob demanda e as armazena em cache na memória. O cache de memória de atividades é atualizado em um intervalo de 30 minutos.  <br/> |
   
Os elementos a seguir aplicam-se apenas à sincronização sob demanda ou à sincronização híbrida de atividades.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Preterido no OSC 1.1.  <br/> Começando no OSC 1.1, o OSC não chama mais [ISocialSession::GetActivities](isocialsession-getactivities.md) e ignora o valor de **dynamicActivitiesLookup**. Para suportar a pesquisa de atividades sob demanda, defina **cacheActivities** como **false** e **getActivities** e **dynamicActivitiesLookupEx** como **true**, e o OSC chamará **ISocialSession2::GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Indica se o provedor OSC oferece suporte para a chamada **ISocialSession2::GetActivitiesEx** para sincronização de atividades sob demanda.  <br/> Se o provedor OSC oferecer suporte à sincronização de atividades sob demanda, ele definirá **getActivities** e **dynamicActivitiesLookupEx** como **true** e **cacheActivities** como **false**. O OSC chama **ISocialSession2::GetActivitiesEx** sempre que o Painel de Pessoas é atualizado. O Painel de Pessoas é atualizado quando o usuário altera o item selecionado na janela do explorador do Outlook ou abre uma janela do inspetor do Outlook. A pesquisa de atividades dinâmicas garante que o usuário sempre verá as atividades mais recentes no Painel de Pessoas, mas aumentará o número de chamadas do provedor para a rede social.  <br/> Se o provedor definir **dynamicActivitiesLookupEx** como **false**, o OSC não chamará **ISocialSession2::GetActivitiesEx** para pessoas exibidas no Painel de Pessoas.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Indica se o OSC deve executar a sincronização sob demanda para atividades quando o Painel de Pessoas é minimizado.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Recursos comuns para oferecer suporte à sincronização sob demanda ou híbrida de amigos, não amigos e atividades

|**Elemento**|**Descrição**|
|:-----|:-----|
|**hashFunction** <br/> | Especifica a função de hash com suporte pelo provedor OSC. Para proteger informações de identificação pessoal de usuários que não estão na rede social do provedor ou em aplicativos de linha de negócios, o OSC transmite endereços de email com hash para **ISocialSession2::GetPeopleDetails** e **ISocialSession2::GetActivitiesEx**.  <br/>  Se **dynamicContactsLookup** estiver configurado como **true** ou **dynamicActivitiesLookupEx** estiver configurado como **true**, o provedor deverá definir **hashFunction** como um dos valores permitidos: **SHA1**, **MD5** ou **CRC32MD5**. Se **hashFunction** estiver ausente ou especificar um valor incorreto, o OSC retornará um erro.  <br/> **SHA1** é o US Secure Hash Algorithm 1 da Internet Engineering Task Force (IETF) definido por [[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt). Por exemplo, o valor com hash **SHA1** do endereço de email melissa@contoso.com é `bb81577b567262a21a4df5f6e335c1250acd7b50`.  <br/> **MD5** é o MD5 Message-Digest Algorithm da Internet Engineering Task Force (IETF) definido por [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt). Por exemplo, o valor com hash **MD5** do endereço de email melissa@contoso.com é `c8c39e61ca1662477b39b83d7b0a0615`.  <br/> **CRC32MD5** é uma combinação de **CRC32** e **MD5**, definida da seguinte forma:  <br/>  Normalize o endereço de email removendo espaços em branco iniciais e finais e convertendo todos os caracteres em minúsculas.  <br/>  Calcule o valor de **CRC32** para o endereço de email normalizado e use a representação decimal inteira desse valor. Se a sua implementação retornar números inteiros assinados, você deverá converter o número inteiro assinado em um inteiro não assinado.  <br/>  Calcule o valor **MD5** do endereço de email normalizado e use a representação hexadecimal desse valor (usando minúsculas de A até F).  <br/>  Combine esses dois valores com um sublinhado.  <br/>  Por exemplo, o valor com hash **CRC32MD5** do endereço de email melissa@contoso.com é `2149665315_c8c39e61ca1662477b39b83d7b0a0615`.  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Recursos para suporte à autenticação e à configuração de conta

|**Elemento**|**Descrição**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Indica se a rede social permite que o usuário altere as definições de configuração automática, como fornecer uma URL diferente para fazer logon.  <br/> |
|**createAccountUrl** <br/> |Se o provedor definir **hideHyperlinks** como **false**, quando o usuário clicar em **Clique aqui para criar uma conta** na caixa de diálogo **Configuração da conta**, a URL especificada por **createAccountUrl** será aberta no navegador padrão.  <br/> |
|**displayUrl** <br/> |Indica se o OSC deve exibir a caixa de texto **Endereço da URL** para a rede social na caixa de diálogo de configuração da conta.  <br/> |
|**forgotPasswordUrl** <br/> |Se o provedor definir **hideHyperlinks** como **false**, quando o usuário clicar em **Esqueceu sua senha?** na caixa de diálogo **Configuração da conta**, a URL especificada por **forgotPasswordUrl** será aberta no navegador padrão.  <br/> |
|**hideHyperlinks** <br/> |Indica se o OSC deve ocultar os hiperlinks **Clique aqui para criar uma conta** e **Esqueceu sua senha?** na caixa de diálogo de configuração da conta.  <br/> O OSC 1.0 ignora essa configuração, e os hiperlinks ficam sempre ocultos. O OSC 1.1 observa o valor dessa configuração.  <br/> |
|**hideRememberMyPassword** <br/> |Indica se o OSC deve ocultar a caixa de seleção **Lembrar minha senha** na caixa de diálogo de configuração da conta.  <br/> Se o provedor definir **hideRememberMyPassword** como **true**, o OSC agirá como se a caixa **Lembrar minha senha** estivesse desmarcada e não salvará a senha.  <br/> Se o provedor definir **hideRememberMyPassword** como **false**, o OSC exibirá a caixa de seleção **Lembrar minha senha** na caixa de diálogo de configuração da conta.  <br/> |
|**supportsAutoConfigure** <br/> |Indica se o OSC deve chamar a função **GetAutoConfiguredSession** na interface **ISocialProvider** para tentar a configuração automática e fazer logon na rede social para o usuário.  <br/> |
|**useLogonCached** <br/> |Indica se o provedor OSC oferece suporte para a chamada [ISocialSession2::LogonCached](isocialsession2-logoncached.md)para fazer logon com credenciais armazenadas em cache.  <br/> Se o provedor definir **useLogonCached** como **true**, o OSC ignorará a configuração para **useLogonWebAuth**, e o OSC chamará **ISocialSession2::LogonCached** para autenticação.  <br/> Se o provedor definir **dynamicActivitiesLookupEx** como **false**, o OSC não chamará **ISocialSession2::LogonCached** para autenticação.  <br/> |
|**useLogonWebAuth** <br/> |Indica se o OSC deve usar a autenticação baseada em formulários e o método [ISocialSession::LogonWeb](isocialsession-logonweb.md). Se o provedor definir **useLogonWebAuth** como **false**, o OSC usa autenticação básica e chama o método [ISocialSession::Logon](isocialsession-logon.md). Se o provedor definir **useLogonWebAuth** como **true**, o OSC usará a autenticação baseada em formulários e chamará **ISocialSession::LogonWeb**.  <br/> |
   
Dependendo do XML de **recursos** retornado pelo provedor no método **ISocialProvider::GetCapabilities**, a caixa de diálogo de configuração de conta é alterada. Por exemplo, a Figura 1 mostra a caixa de diálogo de configuração da conta para um exemplo de TestProvider. 
  
**Figura 1. Exemplo de TestProvider na caixa de diálogo de configuração da conta**

![Informações de configuração de exemplo de TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)

