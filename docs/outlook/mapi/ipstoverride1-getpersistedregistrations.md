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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767655"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="f09b9-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="f09b9-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="f09b9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f09b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f09b9-105">Recupera a lista dos registros para o arquivo de pastas particulares (. pst).</span><span class="sxs-lookup"><span data-stu-id="f09b9-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="f09b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f09b9-106">Parameters</span></span>

 <span data-ttu-id="f09b9-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="f09b9-107">_ppmval_</span></span>
  
> <span data-ttu-id="f09b9-108">[in] Um ponteiro para um ponteiro para uma estrutura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f09b9-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="f09b9-109">O membro ulPropTag esta estrutura é do tipo PT_MV_UNICODE e o membro de valor de MVszW será uma matriz de cadeias de caracteres de Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f09b9-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="f09b9-110">Essas cadeias de caracteres são caminhos para DLLs para o qual o registro tem foi persistente.</span><span class="sxs-lookup"><span data-stu-id="f09b9-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f09b9-111">suporte. pst para ANSI não está implementado.</span><span class="sxs-lookup"><span data-stu-id="f09b9-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="f09b9-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f09b9-112">Return value</span></span>

<span data-ttu-id="f09b9-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f09b9-113">S_OK</span></span> 
  
> <span data-ttu-id="f09b9-114">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f09b9-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f09b9-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f09b9-115">See also</span></span>



[<span data-ttu-id="f09b9-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f09b9-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="f09b9-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f09b9-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

