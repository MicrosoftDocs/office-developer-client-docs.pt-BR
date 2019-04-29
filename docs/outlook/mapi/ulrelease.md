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
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415842"
---
# <a name="ulrelease"></a><span data-ttu-id="b7aa6-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="b7aa6-103">UlRelease</span></span>

  
  
<span data-ttu-id="b7aa6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7aa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7aa6-105">Fornece uma maneira alternativa para invocar o método OLE **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="b7aa6-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7aa6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b7aa6-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7aa6-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b7aa6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b7aa6-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b7aa6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7aa6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b7aa6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b7aa6-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b7aa6-110">Called by:</span></span>  <br/> |<span data-ttu-id="b7aa6-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b7aa6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="b7aa6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7aa6-112">Parameters</span></span>

 <span data-ttu-id="b7aa6-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="b7aa6-113">_punk_</span></span>
  
> <span data-ttu-id="b7aa6-114">no Ponteiro para uma interface derivada da interface **IUnknown** , em outras palavras, em qualquer interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7aa6-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b7aa6-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b7aa6-115">Return value</span></span>

<span data-ttu-id="b7aa6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7aa6-116">S_OK</span></span> 
  
> <span data-ttu-id="b7aa6-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="b7aa6-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b7aa6-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b7aa6-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b7aa6-119">Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="b7aa6-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7aa6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7aa6-120">Remarks</span></span>

<span data-ttu-id="b7aa6-121">A contagem de referência é o número de ponteiros existentes para o objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="b7aa6-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="b7aa6-122">Se o parâmetro _punk_ for NULL, a função retornará imediatamente sem chamar **IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="b7aa6-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="b7aa6-123">**UlRelease** retorna o valor retornado pelo método **IUnknown:: Release** , que pode ser igual à contagem de referência do objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="b7aa6-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="b7aa6-124">Para obter mais informações sobre o **IUnknown:: Release**, consulte [Implementing the IUnknown interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b7aa6-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

