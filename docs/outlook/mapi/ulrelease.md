---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770660"
---
# <a name="ulrelease"></a><span data-ttu-id="85b41-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="85b41-103">UlRelease</span></span>

  
  
<span data-ttu-id="85b41-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85b41-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85b41-105">Fornece uma maneira alternativa para invocar o método OLE **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="85b41-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85b41-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="85b41-106">Header file:</span></span>  <br/> |<span data-ttu-id="85b41-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85b41-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="85b41-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="85b41-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85b41-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85b41-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85b41-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="85b41-110">Called by:</span></span>  <br/> |<span data-ttu-id="85b41-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="85b41-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="85b41-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85b41-112">Parameters</span></span>

 <span data-ttu-id="85b41-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="85b41-113">_punk_</span></span>
  
> <span data-ttu-id="85b41-114">[in] Ponteiro para uma interface derivada da interface **IUnknown** , em outras palavras, qualquer interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="85b41-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85b41-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="85b41-115">Return value</span></span>

<span data-ttu-id="85b41-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="85b41-116">S_OK</span></span> 
  
> <span data-ttu-id="85b41-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="85b41-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="85b41-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="85b41-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="85b41-119">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="85b41-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85b41-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="85b41-120">Remarks</span></span>

<span data-ttu-id="85b41-121">A contagem de referência é o número de ponteiros existentes para o objeto ser liberada.</span><span class="sxs-lookup"><span data-stu-id="85b41-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="85b41-122">Se o parâmetro _punk_ for NULL, a função retornará imediatamente sem chamar **IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="85b41-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="85b41-123">**UlRelease** retornará o valor retornado pelo método **IUnknown:: Release** , que pode ser igual à contagem de referência para o objeto ser liberada.</span><span class="sxs-lookup"><span data-stu-id="85b41-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="85b41-124">Para obter mais informações sobre **IUnknown:: Release**, consulte [Implementando a IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="85b41-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

