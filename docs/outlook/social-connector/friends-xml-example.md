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
# <a name="friends-xml-example"></a><span data-ttu-id="9dad2-105">Exemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="9dad2-105">Friends XML example</span></span>

<span data-ttu-id="9dad2-106">O exemplo de XML neste tópico é uma cadeia de caracteres XML amigo retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) .</span><span class="sxs-lookup"><span data-stu-id="9dad2-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="9dad2-107">O exemplo mostra os **amigos** XML para dois amigos, que cada delimitados pelo elemento de **pessoa** .</span><span class="sxs-lookup"><span data-stu-id="9dad2-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="9dad2-108">Cada amigo Especifica um valor exclusivo para o elemento **userID** na rede social.</span><span class="sxs-lookup"><span data-stu-id="9dad2-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="9dad2-109">Os elementos restantes de **amigos** XML têm nomes auto-explicativos.</span><span class="sxs-lookup"><span data-stu-id="9dad2-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="9dad2-110">Para obter uma descrição detalhada desses elementos, consulte [XML para amigos](xml-for-friends.md).</span><span class="sxs-lookup"><span data-stu-id="9dad2-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="9dad2-111">Exemplo XML</span><span class="sxs-lookup"><span data-stu-id="9dad2-111">XML example</span></span>

<span data-ttu-id="9dad2-112">O exemplo a seguir mostra os **amigos** XML para as duas pessoas na rede social.</span><span class="sxs-lookup"><span data-stu-id="9dad2-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9dad2-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dad2-113">See also</span></span>

- [<span data-ttu-id="9dad2-114">Exemplos XML de provedor do OSC</span><span class="sxs-lookup"><span data-stu-id="9dad2-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="9dad2-115">Exemplo de XML de recursos</span><span class="sxs-lookup"><span data-stu-id="9dad2-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="9dad2-116">Exemplo de XML de Feed de atividade</span><span class="sxs-lookup"><span data-stu-id="9dad2-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="9dad2-117">Esquema XML do Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="9dad2-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

