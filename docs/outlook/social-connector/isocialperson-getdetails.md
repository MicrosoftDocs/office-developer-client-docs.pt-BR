---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtém uma cadeia de caracteres que representa detalhes da pessoa, como o nome, sobrenome e uma URL para uma imagem de perfil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427329"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="e6d89-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="e6d89-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="e6d89-104">Obtém uma cadeia de caracteres que representa detalhes da pessoa, como o nome, sobrenome e uma URL para uma imagem de perfil.</span><span class="sxs-lookup"><span data-stu-id="e6d89-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="e6d89-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6d89-105">Parameters</span></span>

<span data-ttu-id="e6d89-106">_detalhes_</span><span class="sxs-lookup"><span data-stu-id="e6d89-106">_details_</span></span>
  
> <span data-ttu-id="e6d89-107">[out] Um valor de cadeia de caracteres XML que representa os detalhes de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="e6d89-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6d89-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6d89-108">Remarks</span></span>

<span data-ttu-id="e6d89-109">A  _cadeia_ de caracteres XML de detalhes retornados deve estar em conformidade com a definição de esquema para **pessoa,** conforme definido na extensibilidade do provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="e6d89-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="e6d89-110">O OSC **chamará GetDetails** se o provedor OSC suportar a sincronização híbrida ou em cache de amigos na rede social.</span><span class="sxs-lookup"><span data-stu-id="e6d89-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="e6d89-111">Quando o OSC inicialmente obtém atividades de amigos para o usuário conectado, ele chama [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)e armazena informações de amigos em uma pasta de contatos específica da rede social, no armazenamento padrão do outlook do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="e6d89-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="e6d89-112">Subsequentemente, o OSC não chama **GetFriendsAndColleagues** ou **GetDetails,** a menos que o intervalo de atualização para o cache tenha expirado.</span><span class="sxs-lookup"><span data-stu-id="e6d89-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="e6d89-113">Para obter mais informações sobre como o OSC armazena em cache as informações dos amigos em uma pasta de contatos, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="e6d89-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6d89-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6d89-114">See also</span></span>

- [<span data-ttu-id="e6d89-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6d89-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

