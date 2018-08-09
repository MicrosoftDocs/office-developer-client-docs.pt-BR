---
title: Exemplo de XML de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: O exemplo de XML neste tópico é uma cadeia de caracteres XML amigo retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialPerson::GetFriendsAndColleagues. O exemplo mostra os XML de amigos para dois amigos, que cada delimitados pelo elemento de pessoa. Cada amigo Especifica um valor exclusivo para o elemento userID na rede social.
ms.openlocfilehash: 6944213e9483042862fa4cefd8420e39ade9139f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770818"
---
# <a name="friends-xml-example"></a>Exemplo de XML de amigos

O exemplo de XML neste tópico é uma cadeia de caracteres XML amigo retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) . O exemplo mostra os **amigos** XML para dois amigos, que cada delimitados pelo elemento de **pessoa** . Cada amigo Especifica um valor exclusivo para o elemento **userID** na rede social. 
  
Os elementos restantes de **amigos** XML têm nomes auto-explicativos. Para obter uma descrição detalhada desses elementos, consulte [XML para amigos](xml-for-friends.md). 
  
## <a name="xml-example"></a>Exemplo XML

O exemplo a seguir mostra os **amigos** XML para as duas pessoas na rede social. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>http://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>http://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a>Confira também

- [Exemplos XML de provedor do OSC](osc-provider-xml-examples.md)  
- [Exemplo de XML de recursos](capabilities-xml-example.md) 
- [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md) 
- [Esquema XML do Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md)

