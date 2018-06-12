---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica um usuário que pode ou não ter livre/ocupado dados disponíveis.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765799"
---
# <a name="fbuser"></a><span data-ttu-id="52f46-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="52f46-103">FBUser</span></span>

<span data-ttu-id="52f46-104">Identifica um usuário que pode ou não ter livre/ocupado dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="52f46-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="52f46-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="52f46-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="52f46-106">Membros</span><span class="sxs-lookup"><span data-stu-id="52f46-106">Members</span></span>

<span data-ttu-id="52f46-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="52f46-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="52f46-108">O comprimento da identificação de entrada do usuário de email como representado pela interface [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="52f46-108">The length of the entry ID of the mail user as represented by the [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) interface.</span></span> 
    
<span data-ttu-id="52f46-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="52f46-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="52f46-110">A identificação de entrada do usuário de email como representado pela interface **IMailUser** .</span><span class="sxs-lookup"><span data-stu-id="52f46-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="52f46-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="52f46-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="52f46-112">Este parâmetro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="52f46-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="52f46-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="52f46-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="52f46-114">Este parâmetro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="52f46-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52f46-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="52f46-115">See also</span></span>

- [<span data-ttu-id="52f46-116">Sobre a API do serviço de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="52f46-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="52f46-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="52f46-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

