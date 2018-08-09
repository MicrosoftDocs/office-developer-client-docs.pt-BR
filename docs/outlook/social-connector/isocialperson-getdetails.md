---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtém um string que representa os detalhes para a pessoa, como o primeiro nome, sobrenome e uma URL para uma imagem de perfil.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770831"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="1416a-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="1416a-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="1416a-104">Obtém um string que representa os detalhes para a pessoa, como o primeiro nome, sobrenome e uma URL para uma imagem de perfil.</span><span class="sxs-lookup"><span data-stu-id="1416a-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="1416a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1416a-105">Parameters</span></span>

<span data-ttu-id="1416a-106">_detalhes_</span><span class="sxs-lookup"><span data-stu-id="1416a-106">_details_</span></span>
  
> <span data-ttu-id="1416a-107">[out] Um valor de cadeia de caracteres XML que representa os detalhes de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="1416a-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1416a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1416a-108">Remarks</span></span>

<span data-ttu-id="1416a-109">A cadeia de caracteres retornada _detalhes_ XML deve estar em conformidade com a definição de esquema para a **pessoa**, conforme definido no esquema para fornecer extensibilidade de provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="1416a-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="1416a-110">O OSC chamadas **GetDetails** se o provedor OSC oferece suporte armazenado em cache ou sincronização híbrido de amigos na rede social.</span><span class="sxs-lookup"><span data-stu-id="1416a-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="1416a-111">Quando o OSC inicialmente obtém atividades dos amigos para o usuário conectado, ele chama [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)e armazena informações de amigos em uma pasta de contatos específica à rede social, no repositório de Outlook padrão do usuário conectado .</span><span class="sxs-lookup"><span data-stu-id="1416a-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="1416a-112">Subsequentemente o OSC não chama **GetFriendsAndColleagues** ou **GetDetails** , a menos que o intervalo de atualização para o cache expirou.</span><span class="sxs-lookup"><span data-stu-id="1416a-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="1416a-113">Para obter mais informações sobre como o OSC armazena informações de amigos em uma pasta de contatos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="1416a-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1416a-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="1416a-114">See also</span></span>

- [<span data-ttu-id="1416a-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1416a-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

