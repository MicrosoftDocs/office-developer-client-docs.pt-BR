---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575865"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="af21c-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="af21c-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="af21c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af21c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af21c-105">Recupera a lista dos registros para o arquivo de pastas particulares (. pst).</span><span class="sxs-lookup"><span data-stu-id="af21c-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="af21c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af21c-106">Parameters</span></span>

 <span data-ttu-id="af21c-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="af21c-107">_ppmval_</span></span>
  
> <span data-ttu-id="af21c-108">[in] Um ponteiro para um ponteiro para uma estrutura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="af21c-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="af21c-109">O membro ulPropTag esta estrutura é do tipo PT_MV_UNICODE e o membro de valor de MVszW será uma matriz de cadeias de caracteres de Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="af21c-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="af21c-110">Essas cadeias de caracteres são caminhos para DLLs para o qual o registro tem foi persistente.</span><span class="sxs-lookup"><span data-stu-id="af21c-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="af21c-111">suporte. pst para ANSI não está implementado.</span><span class="sxs-lookup"><span data-stu-id="af21c-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="af21c-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="af21c-112">Return value</span></span>

<span data-ttu-id="af21c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="af21c-113">S_OK</span></span> 
  
> <span data-ttu-id="af21c-114">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="af21c-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af21c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="af21c-115">See also</span></span>



[<span data-ttu-id="af21c-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af21c-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="af21c-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af21c-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

