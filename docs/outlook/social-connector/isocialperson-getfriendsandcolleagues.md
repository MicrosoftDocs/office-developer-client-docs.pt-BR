---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtém um string que representa uma coleção de pessoas.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770840"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="0c605-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="0c605-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="0c605-104">Obtém um string que representa uma coleção de pessoas.</span><span class="sxs-lookup"><span data-stu-id="0c605-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="0c605-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c605-105">Parameters</span></span>

<span data-ttu-id="0c605-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="0c605-106">_personsCollection_</span></span>
  
> <span data-ttu-id="0c605-107">[out] Uma cadeia de caracteres XML que representa um conjunto de amigos da pessoa e que está em conformidade com a definição de **amigos** conforme definido no esquema XML para fornecer extensibilidade de provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="0c605-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c605-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c605-108">Remarks</span></span>

<span data-ttu-id="0c605-109">O OSC chamadas **GetFriendsAndColleagues** se o provedor OSC oferece suporte armazenado em cache ou sincronização híbrido de amigos na rede social.</span><span class="sxs-lookup"><span data-stu-id="0c605-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="0c605-110">Quando o OSC inicialmente chama o método **GetFriendsAndColleagues** para o usuário do Outlook que está conectado à rede social, **GetFriendsAndColleagues** retorna uma cadeia de caracteres XML que representa amigos do usuário conectado na rede social.</span><span class="sxs-lookup"><span data-stu-id="0c605-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="0c605-111">A cadeia de caracteres XML em conformidade com a definição de esquema XML **amigos** e especifica um elemento de **pessoa** (que também é compatível com a definição de esquema do provedor OSC) para cada amigo.</span><span class="sxs-lookup"><span data-stu-id="0c605-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="0c605-112">Quando **GetFriendsAndColleagues** retorna informações sobre o usuário conectado de amigos, o OSC armazena essas informações em uma pasta Contatos.</span><span class="sxs-lookup"><span data-stu-id="0c605-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="0c605-113">Essa pasta é específica para a rede social e reside no armazenamento do Outlook do usuário conectado no padrão.</span><span class="sxs-lookup"><span data-stu-id="0c605-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="0c605-114">Para obter mais informações sobre como o OSC armazena informações de amigos em uma pasta de contatos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="0c605-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="0c605-115">Informações de cada amigo retornado no parâmetro _personsCollection_ é compatível com a definição de esquema XML para a **pessoa**.</span><span class="sxs-lookup"><span data-stu-id="0c605-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="0c605-116">O elemento da **pessoa** que oferece suporte a muitas partes de informações para cada amigo, incluindo os endereços de email SMTP (que mapeiam para os elementos **emailAddress**, **emailAddress2**e **emailAddress3** ) que o amigo tenha especificado na rede social e a ID de usuário (que é mapeado para o elemento **userID** ) que identifica esse amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="0c605-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="0c605-117">Para mostrar as atividades para um usuário do Outlook selecionado no painel de pessoas, o OSC tenta corresponder ao usuário com cada amigo retornado da **GetFriendsAndColleagues**.</span><span class="sxs-lookup"><span data-stu-id="0c605-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="0c605-118">O OSC realiza isso mediante o endereço SMTP do usuário selecionado no Outlook com os endereços de email que cada amigo especificado na rede social de correspondência.</span><span class="sxs-lookup"><span data-stu-id="0c605-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="0c605-119">Se o OSC encontrar um endereço de email SMTP correspondente, o OSC usa o correspondente **userID** do amigo para chamar o método [ISocialSession::GetPerson](isocialsession-getperson.md) .</span><span class="sxs-lookup"><span data-stu-id="0c605-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="0c605-120">Ele faz isso para obter um objeto [ISocialPerson](isocialpersoniunknown.md) desse amigo, que habilita o OSC fazer atividades e imagens desse amigo a partir da rede social.</span><span class="sxs-lookup"><span data-stu-id="0c605-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="0c605-121">No entanto, se o usuário selecionado do Outlook não especificar esse mesmo endereço SMTP em uma conta na rede social, ou se o usuário do Outlook não têm uma conta na rede social, o OSC não conseguirão localizar uma correspondência para esse usuário e não exibirão qualquer activiti es para esse usuário na rede social.</span><span class="sxs-lookup"><span data-stu-id="0c605-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c605-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c605-122">See also</span></span>

- [<span data-ttu-id="0c605-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c605-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="0c605-124">Obtendo informações de amigos</span><span class="sxs-lookup"><span data-stu-id="0c605-124">Getting Friends Information</span></span>](getting-friends-information.md)

