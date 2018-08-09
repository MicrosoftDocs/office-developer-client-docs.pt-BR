---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Retorna uma string que contém uma coleção de detalhes de imagem e a pessoa para os usuários especificados pelo parâmetro personsAddresses.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770869"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="95dc5-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="95dc5-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="95dc5-104">Retorna uma string que contém uma coleção de detalhes de imagem e a pessoa para os usuários especificados pelo parâmetro _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="95dc5-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="95dc5-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95dc5-105">Parameters</span></span>

<span data-ttu-id="95dc5-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="95dc5-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="95dc5-107">[in] Uma sequência de caracteres XML que especifica os endereços SMTP com hash de um conjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="95dc5-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="95dc5-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="95dc5-108">_personsCollection_</span></span>
  
> <span data-ttu-id="95dc5-109">[out] Uma sequência de caracteres XML que contém uma coleção de detalhes de imagem e de pessoa.</span><span class="sxs-lookup"><span data-stu-id="95dc5-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95dc5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="95dc5-110">Remarks</span></span>

<span data-ttu-id="95dc5-111">Outlook Social Connector (OSC) chama **GetPeopleDetails** se o provedor do OSC oferece suporte a sincronização sob demanda ou híbrida de amigos e não-amigos.</span><span class="sxs-lookup"><span data-stu-id="95dc5-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="95dc5-112">O parâmetro _personsAddresses_ deve estar de acordo com a definição de esquema **hashedAddresses**, conforme definido no esquema para extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="95dc5-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="95dc5-113">A cadeia de caracteres _personsAddresses_ representa um conjunto de hash endereços SMTP para cada usuário exibida no painel de pessoas.</span><span class="sxs-lookup"><span data-stu-id="95dc5-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="95dc5-114">O usuário não precisa ser um amigo do logon de usuário representado pela propriedade [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="95dc5-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="95dc5-115">Os endereços SMTP com hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** nos do provedor **capacidades** de XML.</span><span class="sxs-lookup"><span data-stu-id="95dc5-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="95dc5-116">O OSC identifica cada **hashedAddress** na coleção _personAddresses_ com um elemento de **índice** .</span><span class="sxs-lookup"><span data-stu-id="95dc5-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="95dc5-117">O provedor deve usar o elemento de **índice** para identificar os do destinatário **pessoa** XML quando ele retorna **amigos** XML para **GetPeopleDetails**.</span><span class="sxs-lookup"><span data-stu-id="95dc5-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="95dc5-118">Se o destinatário não for um usuário registrado na rede social, o provedor não deve retornar qualquer **pessoa** XML para que o destinatário.</span><span class="sxs-lookup"><span data-stu-id="95dc5-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="95dc5-119">O elemento de **índice** para cada usuário de rede representado por **pessoa** XML corresponde ao elemento de **índice** para o destinatário em _personsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="95dc5-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="95dc5-120">O OSC armazena as informações retornadas pelo parâmetro _personsCollection_ na memória.</span><span class="sxs-lookup"><span data-stu-id="95dc5-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="95dc5-121">A cadeia de caracteres XML _personsCollection_ deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="95dc5-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="95dc5-122">Para obter mais informações sobre como o OSC usa e atualiza a essas informações na memória, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="95dc5-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95dc5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="95dc5-123">See also</span></span>

- [<span data-ttu-id="95dc5-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95dc5-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="95dc5-125">Sincronização de amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="95dc5-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

