---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica um usuário que pode ou não ter livre/ocupado dados disponíveis.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387899"
---
# <a name="fbuser"></a><span data-ttu-id="fefce-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="fefce-103">FBUser</span></span>

<span data-ttu-id="fefce-104">Identifica um usuário que pode ou não ter livre/ocupado dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fefce-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fefce-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="fefce-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="fefce-106">Members</span><span class="sxs-lookup"><span data-stu-id="fefce-106">Members</span></span>

<span data-ttu-id="fefce-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="fefce-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="fefce-108">O comprimento da identificação de entrada do usuário de email como representado pela interface [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) .</span><span class="sxs-lookup"><span data-stu-id="fefce-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="fefce-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="fefce-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="fefce-110">A identificação de entrada do usuário de email como representado pela interface **IMailUser** .</span><span class="sxs-lookup"><span data-stu-id="fefce-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="fefce-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="fefce-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="fefce-112">Este parâmetro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="fefce-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="fefce-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="fefce-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="fefce-114">Este parâmetro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="fefce-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fefce-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="fefce-115">See also</span></span>

- [<span data-ttu-id="fefce-116">Sobre a API do serviço de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="fefce-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="fefce-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="fefce-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

