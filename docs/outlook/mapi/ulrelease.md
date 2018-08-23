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
ms.openlocfilehash: 46c37dbcf1aa3b0469281b8db99f210bda0918be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582298"
---
# <a name="ulrelease"></a><span data-ttu-id="0db9b-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="0db9b-103">UlRelease</span></span>

  
  
<span data-ttu-id="0db9b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0db9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0db9b-105">Fornece uma maneira alternativa para invocar o método OLE **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="0db9b-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0db9b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0db9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0db9b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0db9b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0db9b-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0db9b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0db9b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0db9b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0db9b-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0db9b-110">Called by:</span></span>  <br/> |<span data-ttu-id="0db9b-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0db9b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="0db9b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0db9b-112">Parameters</span></span>

 <span data-ttu-id="0db9b-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="0db9b-113">_punk_</span></span>
  
> <span data-ttu-id="0db9b-114">[in] Ponteiro para uma interface derivada da interface **IUnknown** , em outras palavras, qualquer interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="0db9b-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0db9b-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0db9b-115">Return value</span></span>

<span data-ttu-id="0db9b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0db9b-116">S_OK</span></span> 
  
> <span data-ttu-id="0db9b-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="0db9b-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0db9b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="0db9b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="0db9b-119">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="0db9b-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0db9b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0db9b-120">Remarks</span></span>

<span data-ttu-id="0db9b-121">A contagem de referência é o número de ponteiros existentes para o objeto ser liberada.</span><span class="sxs-lookup"><span data-stu-id="0db9b-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="0db9b-122">Se o parâmetro _punk_ for NULL, a função retornará imediatamente sem chamar **IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="0db9b-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="0db9b-123">**UlRelease** retornará o valor retornado pelo método **IUnknown:: Release** , que pode ser igual à contagem de referência para o objeto ser liberada.</span><span class="sxs-lookup"><span data-stu-id="0db9b-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="0db9b-124">Para obter mais informações sobre **IUnknown:: Release**, consulte [Implementando a IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0db9b-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

