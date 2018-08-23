---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592365"
---
# <a name="uladdref"></a><span data-ttu-id="f85bd-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="f85bd-103">UlAddRef</span></span>

  
  
<span data-ttu-id="f85bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f85bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f85bd-105">Fornece uma maneira alternativa para invocar o método OLE **AddRef**.</span><span class="sxs-lookup"><span data-stu-id="f85bd-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f85bd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f85bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="f85bd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f85bd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f85bd-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="f85bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f85bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f85bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f85bd-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="f85bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="f85bd-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f85bd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="f85bd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f85bd-112">Parameters</span></span>

 <span data-ttu-id="f85bd-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="f85bd-113">_punk_</span></span>
  
> <span data-ttu-id="f85bd-114">[in] Ponteiro para uma interface derivada da interface **IUnknown** , em outras palavras, qualquer interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="f85bd-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f85bd-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f85bd-115">Return value</span></span>

<span data-ttu-id="f85bd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f85bd-116">S_OK</span></span> 
  
> <span data-ttu-id="f85bd-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="f85bd-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f85bd-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f85bd-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f85bd-119">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="f85bd-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f85bd-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f85bd-120">Remarks</span></span>

 <span data-ttu-id="f85bd-121">**UlAddRef** retornará o valor retornado pelo método **AddRef** , que é o novo valor da contagem de referência para a interface.</span><span class="sxs-lookup"><span data-stu-id="f85bd-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="f85bd-122">O valor é diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="f85bd-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="f85bd-123">Para obter mais informações sobre **AddRef**, consulte [Implementando a IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f85bd-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

