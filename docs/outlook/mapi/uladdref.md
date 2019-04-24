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
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315369"
---
# <a name="uladdref"></a><span data-ttu-id="ed83c-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="ed83c-103">UlAddRef</span></span>

  
  
<span data-ttu-id="ed83c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed83c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed83c-105">Fornece uma maneira alternativa de chamar o método OLE **IUnknown: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="ed83c-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed83c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ed83c-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed83c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ed83c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ed83c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ed83c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ed83c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ed83c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ed83c-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="ed83c-110">Called by:</span></span>  <br/> |<span data-ttu-id="ed83c-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="ed83c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="ed83c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed83c-112">Parameters</span></span>

 <span data-ttu-id="ed83c-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="ed83c-113">_punk_</span></span>
  
> <span data-ttu-id="ed83c-114">no Ponteiro para uma interface derivada da interface **IUnknown** , em outras palavras, em qualquer interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed83c-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ed83c-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed83c-115">Return value</span></span>

<span data-ttu-id="ed83c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed83c-116">S_OK</span></span> 
  
> <span data-ttu-id="ed83c-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="ed83c-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="ed83c-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="ed83c-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="ed83c-119">Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="ed83c-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed83c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed83c-120">Remarks</span></span>

 <span data-ttu-id="ed83c-121">**UlAddRef** retorna o valor retornado pelo método **IUnknown:: AddRef** , que é o novo valor da contagem de referência da interface.</span><span class="sxs-lookup"><span data-stu-id="ed83c-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="ed83c-122">O valor é diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ed83c-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="ed83c-123">Para obter mais informações sobre o **IUnknown:: AddRef**, consulte [Implementing the IUnknown interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ed83c-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

