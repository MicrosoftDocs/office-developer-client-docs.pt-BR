---
title: Exemplo de XML de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: O exemplo XML neste tópico é uma cadeia XML de amigos retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialPerson::GetFriendsAndColleagues. O exemplo mostra o XML de dois amigos, cada um delimitado pelo elemento person. Cada amigo especifica um valor exclusivo para o elemento userID na rede social.
ms.openlocfilehash: 5dbda1e4439f807ccc6e7abddd0ef654ae801fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280956"
---
# <a name="friends-xml-example"></a><span data-ttu-id="0ff6b-105">Exemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="0ff6b-105">Friends XML example</span></span>

<span data-ttu-id="0ff6b-106">O exemplo XML neste tópico é uma cadeia XML de amigos retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md).</span><span class="sxs-lookup"><span data-stu-id="0ff6b-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="0ff6b-107">O exemplo mostra o XML de dois **amigos**, cada um delimitado pelo elemento **person**.</span><span class="sxs-lookup"><span data-stu-id="0ff6b-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="0ff6b-108">Cada amigo especifica um valor exclusivo para o elemento **userID** na rede social.</span><span class="sxs-lookup"><span data-stu-id="0ff6b-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="0ff6b-109">Os demais elementos do **amigos** XML têm nomes autoexplicativos.</span><span class="sxs-lookup"><span data-stu-id="0ff6b-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="0ff6b-110">Para obter uma descrição detalhada desses elementos, confira [XML para amigos](xml-for-friends.md).</span><span class="sxs-lookup"><span data-stu-id="0ff6b-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="0ff6b-111">Exemplos de XML</span><span class="sxs-lookup"><span data-stu-id="0ff6b-111">XML example</span></span>

<span data-ttu-id="0ff6b-112">O exemplo a seguir mostra o XML de **amigos** para duas pessoas na rede social.</span><span class="sxs-lookup"><span data-stu-id="0ff6b-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
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
    <webProfilePage>https://contoso.com/michael</webProfilePage>
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

## <a name="see-also"></a><span data-ttu-id="0ff6b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ff6b-113">See also</span></span>

- [<span data-ttu-id="0ff6b-114">Exemplos de XML de provedor OSC</span><span class="sxs-lookup"><span data-stu-id="0ff6b-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="0ff6b-115">Exemplo de XML de recursos</span><span class="sxs-lookup"><span data-stu-id="0ff6b-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="0ff6b-116">Exemplo de XML de feed de atividades</span><span class="sxs-lookup"><span data-stu-id="0ff6b-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="0ff6b-117">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="0ff6b-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

