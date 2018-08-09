---
title: Elementos de XML de recursos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: As tabelas deste tópico descrevem os elementos filho dos recursos XML e são agrupadas pelas áreas que eles suportam.
ms.openlocfilehash: 53bce69bbe22f6e950302a92b0ada21ed0f5a1f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770820"
---
# <a name="capabilities-xml-elements"></a>Elementos de XML de recursos

As tabelas deste tópico descrevem os elementos filho dos **recursos de** XML e são agrupadas pelas áreas que eles suportam. O valor padrão de cada elemento de **recursos** é **false**. Se o elemento não for especificado nas **capacidades** XML retornada pelo método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , o valor do elemento é igual a **false**.
  
Para uma descrição de visão geral dos **recursos** de XML, consulte [XML para recursos](xml-for-capabilities.md). Para obter um exemplo dos **recursos** de XML, consulte [Exemplo de XML de recursos](capabilities-xml-example.md). Para uma definição completa do esquema de XML de provedor Microsoft Outlook Social Connector (OSC), incluindo quais elementos são obrigatórias ou opcionais, consulte [Esquema de XML para Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Recursos de suporte aos amigos

A tabela a seguir mostra os elementos que se aplicam a qualquer forma de sincronização de amigos ou não-amigos.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Indica se o provedor oferece suporte a chamada do método [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md) .  <br/> **followPerson** e **doNotFollowPerson** são recursos independentes de um provedor OSC. Um provedor OSC pode indicar a capacidade de ser capaz de adicionar uma pessoa como um amigo (configuração **followPerson** como **true**) ou poderá remover uma pessoa como um amigo em uma conta de rede social (configuração **doNotFollowPerson** como **true**). Em geral, sendo capaz de acompanhar não implicam ser capaz de parar de seguir. **followPerson** é um recurso e ele não deve ser interpretado como uma ação a seguir uma pessoa específica ou cada pessoa na conta de redes sociais. **followPerson** sendo **true** não implica **doNotFollowPerson** for **false**.  <br/> |
|**followPerson** <br/> |Indica se o provedor oferece suporte a chamada do método [ISocialSession::FollowPerson](isocialsession-followperson.md) . O OSC verifica **followPerson** se **cacheFriends** for **true** (cache de sincronização de amigos), **dynamicContactsLookup** for **true** (sincronização sob demanda de amigos e não-amigos), ou ambos os cacheFriends ** **e **dynamicContactsLookup** são verdadeiras (sincronização de híbrido de amigos e não-amigos). Se o provedor define **followPerson** como **true**, o OSC exibe um emblema de rede no painel de pessoas para as pessoas que o usuário está seguindo e permite que o **em \<NetworkName\> ** command no menu **Adicionar (+)** na pessoas Painel. Se o provedor define **followPerson** como **false**, o emblema de rede não for exibido e o **em \<NetworkName\> ** comando está oculto.  <br/> |
|**getFriends** <br/> |Indica se o provedor oferece suporte a chamada do método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) ou [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . Se o provedor define **getFriends** como **true**, o OSC usa o valor de **cacheFriends** ou **dynamicContactsLookup** para determinar se a rede social permite armazenar amigos, como itens de contato do Outlook ou na memória. Se o provedor define **getFriends** como **false**, a rede social não suporta amigos e **ISocialPerson::GetFriendsAndColleagues** e **ISocialSession2::GetPeopleDetails** métodos e o OSC ignora os valores dos **cacheFriends** e **dynamicContactsLookup**.  <br/> |
   
Os elementos a seguir se aplicam apenas a sincronização de cache de amigos ou sincronização híbrido de amigos e não-amigos. Para obter mais informações sobre a sincronização de amigos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**cacheFriends** <br/> |Indica se o provedor do OSC permite o armazenamento de amigos como itens de contato do Outlook. O OSC verifica **cacheFriends** somente se **getFriends** for **true**. Se o provedor define **cacheFriends** como **true**, o OSC sincroniza amigos armazenando em cache e cria uma pasta de contatos de rede específica no repositório de padrão do usuário para contatos amigo. O nome da pasta Contatos específicos de rede é o valor da propriedade [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . Se o provedor define **cacheFriends** como **false**, o OSC não cria uma pasta de contatos específicos de rede para contatos de amigo armazenar amigos.  <br/> |
|**contactSyncRestartInterval** <br/> |Determina o intervalo de repetição, em minutos, entre as tentativas para sincronizar as informações de amigos da rede social, se ocorrer um erro de sincronização. O OSC usa esse elemento somente se o provedor do OSC oferece suporte à sincronização de cache ou pasta de contatos de sincronização de híbrido de amigos para uma rede social-específica (**cacheFriends** for **true**).  <br/> O intervalo de repetição padrão é 30 minutos, a menos que o padrão é substituído pelo `ContactSyncRestartInterval` chave sob `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`. Se o provedor define **contactSyncRestartInterval**, o valor de provedor substituirá o intervalo de repetição do padrão de 30 minutos ou o valor da chave do registro.  <br/> Para obter mais informações sobre a sincronização de amigos e informações de não-amigos sob demanda, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).  <br/> |
   
Os elementos a seguir se aplicam a apenas a sincronização sob demanda ou a sincronização de híbrido de amigos e não-amigos.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Indica se o provedor do OSC suporta a chamada [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) para a sincronização sob demanda de amigos e não-amigos.  <br/> O OSC verifica **dynamicContactsLookup** somente se **getFriends** for **true**. A configuração padrão para **dynamicContactsLookup** é **false**.  <br/> Se o provedor do OSC especifica **dynamicContactsLookup** como **true** e **getFriends** como **true**, o OSC chama **ISocialSession2::GetPeopleDetails** toda vez que o painel de pessoas for atualizado. O painel de pessoas é atualizado quando o usuário seleciona a outro usuário no painel de pessoas ou outro item na janela do explorer do Outlook ou abre uma janela de Inspetor do Outlook. Pesquisa de contatos dinâmica garante que o usuário sempre vê as imagens mais recentes do usuário e as informações de perfil no painel de pessoas, mas aumenta o número de chamadas do provedor para a rede social.  <br/> Se o provedor define **dynamicContactsLookup** como **false**, o OSC não chama **ISocialSession2::GetPeopleDetails** para atualizar o painel de pessoas.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Indica se o OSC deve realizar a sincronização sob demanda de amigos e não-amigos quando o painel de pessoas é minimizado.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Recursos para suporte de atividades

O seguinte elemento se aplica a qualquer forma de sincronização de atividades suportada pelo provedor do OSC.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**getActivities** <br/> |Indica se o provedor oferece suporte a chamadas de método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) ou [ISocialPerson::GetActivities](isocialperson-getactivities.md) . Se o provedor define **getActivities** como **true**, o OSC usa o valor de **cacheActivities** ou **dynamicActivitiesLookupEx** para determinar se o site de rede social permite armazenar atividades como itens RSS do Outlook ou como atividades de na memória. Se o provedor define **getActivities** como **false**, a rede social não suporta as atividades e **ISocialSession2::GetActivitiesEx** e **ISocialPerson::GetActivities** métodos e o OSC ignora os valores dos ** cacheActivities** e **dynamicActivitiesLookupEx**.  <br/> |
   
O seguinte elemento se aplica somente a sincronização em cache ou sincronização híbrida das atividades.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**cacheActivities** <br/> |Iniciando no Outlook Social Connector 2013, o OSC ignora esse elemento, pois provedores não poderá sincronizar atividades armazenando em cache-los em uma pasta oculta no repositório do usuário.  <br/> Se as atividades de suporte a provedor, o provedor devem suportar sincronize atividades sob demanda. O provedor define **cacheActivities** como **false** e define **dynamicActivitesLookupEx** como **true**. O OSC sincroniza atividades sob demanda e caches atividades na memória. O cache de memória de atividades é atualizado em um intervalo de 30 minutos.  <br/> |
   
Os elementos a seguir se aplicam a apenas a sincronização sob demanda ou a sincronização de híbrido das atividades.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Obsoleto no OSC 1.1.  <br/> Iniciando no OSC 1.1, não é mais o OSC chama [ISocialSession::GetActivities](isocialsession-getactivities.md) e ignora o valor de **dynamicActivitiesLookup**. Para dar suporte à pesquisa de atividades sob demanda, defina **cacheActivities** como **false** e **getActivities** e **dynamicActivitiesLookupEx** como **true**e o OSC chamará **ISocialSession2::GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Indica se o provedor do OSC suporta a chamada **ISocialSession2::GetActivitiesEx** para a sincronização sob demanda de atividades.  <br/> Se o provedor do OSC oferece suporte à sincronização de atividades sob demanda, ele define **getActivities** e **dynamicActivitiesLookupEx** como **true**e **cacheActivities** como **false**. O OSC chama **ISocialSession2::GetActivitiesEx** toda vez que o painel de pessoas for atualizado. O painel de pessoas é atualizado quando o usuário altera o item selecionado na janela do explorer do Outlook ou abre uma janela de Inspetor do Outlook. Pesquisa de atividades dinâmica garante que o usuário sempre verá as atividades mais recentes no painel de pessoas, mas vai aumentar o número de chamadas do provedor para a rede social.  <br/> Se o provedor define **dynamicActivitiesLookupEx** como **false**, o OSC não chama **ISocialSession2::GetActivitiesEx** para pessoas exibidas no painel de pessoas.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Indica se o OSC deve realizar a sincronização sob demanda para atividades quando o painel de pessoas é minimizado.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Recursos comuns para dar suporte a sincronização sob demanda ou híbrida de amigos, não-amigos e atividades

|**Elemento**|**Descrição**|
|:-----|:-----|
|**hashFunction** <br/> | Especifica a função de hash que o provedor do OSC suporte. Para proteger as informações de identificação pessoal de usuários que não estão na rede social ou do aplicativo de linha de negócios do provedor, o OSC passa os endereços de email com hash **ISocialSession2::GetPeopleDetails** e **ISocialSession2:: GetActivitiesEx**.  <br/>  Se **dynamicContactsLookup** estiver definida como **true** ou **dynamicActivitiesLookupEx** estiver definida como **true**, o provedor deve definir **hashFunction** como um dos valores permitidos: **SHA1**, **MD5**ou **CRC32MD5**. Se **hashFunction** estiver faltando ou especifica um valor incorreto, o OSC retornará um erro.  <br/> **SHA1** é o algoritmo de Hash seguro Internet Engineering Task Force (IETF) US 1 definido pela [[RFC3174]](http://www.rfc-editor.org/rfc/rfc3174.txt). Por exemplo, o valor de **SHA1** em hash de email endereço melissa@contoso.com é `bb81577b567262a21a4df5f6e335c1250acd7b50`.  <br/> **MD5** é Internet Engineering Task Force (IETF) MD5 Message-Digest Algorithm definido pela [[RFC1321]](http://www.rfc-editor.org/rfc/rfc1321.txt). Por exemplo, o valor de **MD5** em hash de email endereço melissa@contoso.com é `c8c39e61ca1662477b39b83d7b0a0615`.  <br/> **CRC32MD5** é uma combinação de **CRC32** e **MD5** definida da seguinte forma:  <br/>  Normalize o endereço de email, removendo à esquerda e à direita de espaço em branco e convertendo todos os caracteres para minúsculos.  <br/>  O valor de **CRC32** para o endereço de email normalizado de computação e use a representação de inteiro decimal desse valor. Se sua implementação retornar inteiros assinados, você deve converter o inteiro assinado como um inteiro não assinado.  <br/>  O valor de **MD5** para o endereço de email normalizado de computação e use a representação hexadecimal desse valor (usando minúsculas de À F).  <br/>  Combine esses dois valores com um caractere de sublinhado.  <br/>  Por exemplo, o valor de **CRC32MD5** em hash de email endereço melissa@contoso.com é `2149665315_c8c39e61ca1662477b39b83d7b0a0615`.  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Recursos para dar suporte a autenticação e a configuração da conta

|**Elemento**|**Descrição**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Indica se a rede social permite ao usuário alterar definições de configuração automática, como fornecer uma URL diferente para fazer logon.  <br/> |
|**createAccountUrl** <br/> |Se o provedor define **hideHyperlinks** como **false**, quando o usuário clica em **clique aqui para criar uma conta** na caixa de diálogo **configuração da conta** , o URL especificado pela **createAccountUrl** é aberto no navegador padrão.  <br/> |
|**displayUrl** <br/> |Indica se o OSC deve exibir a caixa de texto **Endereço URL** para a rede social na caixa de diálogo de configuração de conta.  <br/> |
|**forgotPasswordUrl** <br/> |Se o provedor define **hideHyperlinks** como **false**, quando o usuário clica **Esqueceu sua senha?** na caixa de diálogo **configuração da conta** , o URL especificado pela **forgotPasswordUrl** é aberto no navegador padrão.  <br/> |
|**hideHyperlinks** <br/> |Indica se o OSC deve ocultar o **clique aqui para criar uma conta** e **Esqueceu sua senha?** hiperlinks na caixa de diálogo de configuração de conta.  <br/> OSC 1.0 ignora essa configuração e os hiperlinks sempre estão ocultas. OSC 1.1 observa o valor dessa configuração.  <br/> |
|**hideRememberMyPassword** <br/> |Indica se o OSC deve ocultar a caixa de seleção **Lembrar minha senha** na caixa de diálogo de configuração de conta.  <br/> Se o provedor define **hideRememberMyPassword** como **true**, o OSC atuará como se a caixa de **Lembrar minha senha** está desmarcada e não salvará a senha.  <br/> Se o provedor define **hideRememberMyPassword** como **false**, o OSC exibirá a caixa de seleção **Lembrar minha senha** na caixa de diálogo de configuração de conta.  <br/> |
|**supportsAutoConfigure** <br/> |Indica se o OSC deve chamar a função de **GetAutoConfiguredSession** na interface **ISocialProvider** para tentar a configuração automática e faça logon na rede social para o usuário.  <br/> |
|**useLogonCached** <br/> |Indica se o provedor do OSC suporta a chamada [ISocialSession2::LogonCached](isocialsession2-logoncached.md) poderão fazer logon com credenciais armazenadas em cache.  <br/> Se o provedor define **useLogonCached** como **true**, o OSC ignora a configuração para **useLogonWebAuth** e o OSC chama **ISocialSession2::LogonCached** para autenticação.  <br/> Se o provedor define **dynamicActivitiesLookupEx** como **false**, o OSC não chama **ISocialSession2::LogonCached** para autenticação.  <br/> |
|**useLogonWebAuth** <br/> |Indica se o OSC deve usar autenticação baseada em formulários e o método [ISocialSession::LogonWeb](isocialsession-logonweb.md) . Se o provedor define **useLogonWebAuth** como **false**, o OSC usará a autenticação básica e chama o método [ISocialSession::Logon](isocialsession-logon.md) . Se o provedor define **useLogonWebAuth** como **true**, o OSC usa autenticação baseada em formulários e chama **ISocialSession::LogonWeb**.  <br/> |
   
Dependendo dos **recursos** XML retornado pelo provedor no método **ISocialProvider::GetCapabilities** , a configuração da conta alterações da caixa de diálogo. Por exemplo, a Figura 1 mostra a caixa de diálogo de configuração de conta para obter um exemplo de TestProvider. 
  
**Figura 1. Exemplo de TestProvider na caixa de diálogo de configuração de conta**

![TestProvider example configuration information](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)

