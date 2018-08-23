---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b71d1f477435b4a9327b4156560d1aa2e6079536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578700"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="d786e-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="d786e-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="d786e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d786e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d786e-105">Chama uma função interna para verificar que os aplicativos de cliente parâmetros tem passado para provedores de serviços e MAPI.</span><span class="sxs-lookup"><span data-stu-id="d786e-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d786e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d786e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d786e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d786e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d786e-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="d786e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d786e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d786e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d786e-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="d786e-110">Called by:</span></span>  <br/> |<span data-ttu-id="d786e-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="d786e-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="d786e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d786e-112">Parameters</span></span>

 <span data-ttu-id="d786e-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="d786e-113">_eMethod_</span></span>
  
> <span data-ttu-id="d786e-114">[in] Especifica o enumeração, o método para validar.</span><span class="sxs-lookup"><span data-stu-id="d786e-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="d786e-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="d786e-115">_First_</span></span>
  
> <span data-ttu-id="d786e-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="d786e-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d786e-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d786e-117">Return value</span></span>

<span data-ttu-id="d786e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d786e-118">S_OK</span></span> 
  
> <span data-ttu-id="d786e-119">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="d786e-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d786e-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="d786e-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="d786e-121">Um erro impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="d786e-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d786e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d786e-122">Remarks</span></span>

<span data-ttu-id="d786e-123">Parâmetros passados entre MAPI e serviço são considerados provedores estejam corretas e são submetidos a validação de depuração somente à macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="d786e-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="d786e-124">Provedores devem verificar todos os parâmetros passados por aplicativos do cliente, mas os clientes devem presumir que parâmetros MAPI e o provedor estão corretos.</span><span class="sxs-lookup"><span data-stu-id="d786e-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="d786e-125">Use a macro **HR_FAILED** para testar valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="d786e-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="d786e-126">A macro **UlValidateParms** é chamada de forma diferente, dependendo se o código de chamada é C ou C++.</span><span class="sxs-lookup"><span data-stu-id="d786e-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="d786e-127">Esta macro é usada para validar os parâmetros para os métodos **IUnknown** e MAPI alguns que retornam ULONG, em vez de valores HRESULT; a macro [ValidateParms](validateparms.md) funciona para todos os outros.</span><span class="sxs-lookup"><span data-stu-id="d786e-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

