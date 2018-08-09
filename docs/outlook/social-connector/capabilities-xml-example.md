---
title: Exemplo de XML de recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: O exemplo de XML deste tópico é uma sequência de caracteres XML retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialProvider::GetCapabilities para uma rede social. O XML mostra como um provedor OSC Especifica seus recursos e requisitos para que o OSC.
ms.openlocfilehash: 5cafd6d29de8b4357e9e0ce6dab30b125f53b8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770827"
---
# <a name="capabilities-xml-example"></a>Exemplo de XML de recursos

O exemplo de XML deste tópico é uma sequência de caracteres XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para uma rede social. O XML mostra como um provedor OSC Especifica seus recursos e requisitos para que o OSC. 
  
## <a name="capabilities-for-friends"></a>Recursos para amigos

Neste exemplo, o provedor do OSC Especifica os seguintes elementos para mostrar seus recursos com suporte para o recurso de amigos:
  
- **getFriends** como **true** para indicar o provedor do OSC oferece suporte ao método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obter informações de amigos dos programaticamente. 
    
- **cacheFriends** como **true** para informações do cache dos amigos de suporte em uma pasta de contatos do Outlook. 
    
- **contactSyncRestartInterval** como 60 para indicar esse erro diante, o OSC deve repetir a atualização do cache a cada 60 minutos. 
    
- **followPerson** como **true** para indicar a capacidade de adicionar amigos na rede social. 
    
- **doNotFollowPerson** como **false** para indicar que o provedor do OSC não oferece suporte a remoção de uma pessoa como um amigo na rede social. 
    
- **dynamicContactsLookup** como **false** para indicar que o OSC não deve armazenar informações de amigos na memória. 
    
## <a name="capabilities-for-activities"></a>Recursos para atividades

O provedor do OSC Especifica os seguintes elementos para mostrar sua capacidade de oferecer suporte às atividades:
  
- **getActivities** como **true** para indicar que o provedor do OSC suporta o método [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para fazer atividades dos amigos programaticamente. 
    
- **cacheActivities** como **false** para oferecer suporte a atividades de cache de amigos na pasta oculta o Feed de notícias do Outlook. 
    
- **dynamicActivitiesLookupEx** como **true** para indicar que o OSC deve armazenar atividades dos amigos na memória. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Recursos para configuração de conta e autenticação

O provedor do OSC Especifica os seguintes elementos para mostrar seu suporte para autenticação e a configuração de conta:
  
- **useLogonWebAuth** como **false** para indicar que o provedor do OSC suporta a autenticação básica. 
    
- **supportsAutoConfigure** como **false** para indicar que o OSC não deve tentar configurar automaticamente e fazer logon rede social para o usuário. 
    
- **useLogonCached** e **hideRememberMyPassword** como **false** para indicar que o OSC deve solicitar senha cada vez e não deve usar o cache credenciais de logon para fazer logon. 
    
- **displayUrl** como **false** para indicar que o OSC não deve exibir a URL para a rede social na caixa de diálogo de configuração de conta. 
    
- **hideHyperlinks** como **false** para indicar que o provedor do OSC suporta somente contas existentes com senhas conhecidas e o OSC não deve exibir o **clique aqui para criar uma conta** e **Esqueceu sua senha?** hiperlinks na caixa de diálogo de configuração de conta. 
    
## <a name="xml-example"></a>Exemplo XML

O exemplo a seguir mostra os **recursos de** XML de um provedor OSC. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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
  <createAccountUrl>http://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>http://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Confira também

- [Exemplos XML de provedor do OSC](osc-provider-xml-examples.md)  
- [XML para recursos](xml-for-capabilities.md)  
- [Exemplo de XML de amigos](friends-xml-example.md)  
- [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md)  
- [Esquema XML do Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md)

