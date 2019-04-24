---
title: Exemplo de XML de recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: O exemplo XML neste tópico é uma cadeia XML retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialProvider::GetCapabilities para uma rede social. O XML mostra como um provedor de OSC especifica seus recursos e os requisitos para a OSC.
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281227"
---
# <a name="capabilities-xml-example"></a>Exemplo de XML de recursos

O exemplo XML neste tópico é uma cadeia XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para uma rede social. O XML mostra como um provedor de OSC especifica seus recursos e os requisitos para a OSC. 
  
## <a name="capabilities-for-friends"></a>Recursos para amigos

Neste exemplo, o provedor OSC Especifica os seguintes elementos para mostrar os recursos de suporte no recurso amigos:
  
- **getFriends** como **verdadeiro** para indicar que o provedor do OSC é compatível com o método[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obter informações dos amigos por programação. 
    
- **cacheFriends** como **verdadeiro** para dar suporte a informações sobre o cache de amigos em uma pasta de contatos do Outlook. 
    
- **contactSyncRestartInterval** como 60 para indicar que, em caso de erro, a OSC deve repetir a atualização do cache a cada 60 minutos. 
    
- **followPerson** como **verdadeiro** para indicar a capacidade de adicionar amigos em rede social. 
    
- **doNotFollowPerson** como **falso** para indicar que o provedor OSC não oferece suporte para desfazer uma amizade em rede social. 
    
- **dynamicContactsLookup** como **falso** para indicar que o OSC não deve armazenar informações dos amigos na memória. 
    
## <a name="capabilities-for-activities"></a>Recursos para atividades

O provedor OSC especifica os seguintes elementos para mostrar o recurso de atividades de suporte:
  
- **getActivities** como **verdadeiro** para indicar que o provedor do OSC é compatível com o método[ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para visualizar atividades dos amigos por programação. 
    
- **cacheActivities** como **falso** para dar suporte de atividades de cache de amigos na pasta oculta Feed de notícias do Outlook. 
    
- **dynamicActivitiesLookupEx** como **verdadeiro** para indicar que o OSC deverá ser armazenado nas atividades dos amigos na memória. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Testar recursos para autenticação e configuração de conta

O provedor OSC especifica os seguintes elementos para mostrar o suporte para autenticação e configuração de conta:
  
- **useLogonWebAuth** como **falso** para indicar que o provedor OSC dá suporte à autenticação básica. 
    
- **supportsAutoConfigure** como **falso** para indicar que a OSC não deve tentar configurar automaticamente e fazer logon na rede social para o usuário. 
    
- **useLogonCached** e **hideRememberMyPassword** como **falso** para indicar que a OSC deve solicitar senha sempre e não deve usar credenciais de logon armazenadas em cache para fazer logon. 
    
- **displayUrl** como **falso** para indicar que o OSC não deverá exibir a URL para a rede social na caixa de diálogo da Configuração de conta. 
    
- **hideHyperlinks** como **falso** para indicar que o provedor OSC oferece suporte apenas para contas existentes com senhas conhecidas e o OSC não deve exibir os hyperlinks **clique aqui para criar uma conta** e **Esqueceu sua senha? ** na caixa de diálogo da configuração de conta. 
    
## <a name="xml-example"></a>Exemplos de XML

O exemplo a seguir mostra os**recursos** XML de um provedor do OSC. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Confira também

- [Exemplos de XML de provedor OSC](osc-provider-xml-examples.md)  
- [XML para recursos](xml-for-capabilities.md)  
- [Exemplo de XML de amigos](friends-xml-example.md)  
- [Exemplo de XML de feed de atividades](activity-feed-xml-example.md)  
- [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

