---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo parâmetro personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404530"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="cd5cf-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="cd5cf-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="cd5cf-104">Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo parâmetro _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="cd5cf-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="cd5cf-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd5cf-105">Parameters</span></span>

<span data-ttu-id="cd5cf-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="cd5cf-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="cd5cf-107">no Uma sequência de caracteres XML que especifica os endereços SMTP de hash de um conjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="cd5cf-108">__</span><span class="sxs-lookup"><span data-stu-id="cd5cf-108">_personsCollection_</span></span>
  
> <span data-ttu-id="cd5cf-109">bota Uma sequência de caracteres XML que contém uma coleção de detalhes de pessoa e imagem.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd5cf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd5cf-110">Remarks</span></span>

<span data-ttu-id="cd5cf-111">O Outlook Social Connector (OSC) chama **GetPeopleDetails** se o provedor OSC oferecer suporte à sincronização por demanda ou híbrida de amigos e não amigos.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="cd5cf-112">O parâmetro _personsAddresses_ deve estar em conformidade com a definição de esquema para **hashedAddresses**, conforme definido no esquema para a extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="cd5cf-113">A cadeia de caracteres _personsAddresses_ representa um conjunto de endereços SMTP com hash para cada usuário exibido no painel de pessoas.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="cd5cf-114">O usuário não precisa ser um amigo do usuário conectado representado pela propriedade [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="cd5cf-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="cd5cf-115">Os endereços SMTP de hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** no XML de **recursos** do provedor.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="cd5cf-116">O OSC identifica cada **hashedAddress** na coleção _personAddresses_ com um elemento **index** .</span><span class="sxs-lookup"><span data-stu-id="cd5cf-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="cd5cf-117">O provedor deve usar o elemento **index** para identificar o XML **Person** do destinatário quando ele retorna o XML de **amigos** para **GetPeopleDetails**.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="cd5cf-118">Se o destinatário não for um usuário registrado na rede social, o provedor não deverá retornar nenhum XML de **pessoa** para esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="cd5cf-119">O elemento **index** para cada usuário de rede representado pelo **Person** XML corresponde ao elemento **index** do destinatário em _personsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="cd5cf-120">O OSC armazena as informações retornadas pelo __ parâmetro Persons na memória.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="cd5cf-121">A __ cadeia de caracteres XML deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para a extensibilidade do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="cd5cf-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="cd5cf-122">Para obter mais informações sobre como o OSC usa e atualiza essas informações na memória, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="cd5cf-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd5cf-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd5cf-123">See also</span></span>

- [<span data-ttu-id="cd5cf-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd5cf-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="cd5cf-125">Sincronizar amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="cd5cf-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

