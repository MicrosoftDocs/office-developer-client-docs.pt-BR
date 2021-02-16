---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431271"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="b591e-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="b591e-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="b591e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b591e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b591e-105">Chama uma função interna para verificar os parâmetros que os aplicativos cliente passaram para provedores de serviços e MAPI.</span><span class="sxs-lookup"><span data-stu-id="b591e-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b591e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b591e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b591e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b591e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b591e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b591e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b591e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b591e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b591e-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b591e-110">Called by:</span></span>  <br/> |<span data-ttu-id="b591e-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b591e-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="b591e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b591e-112">Parameters</span></span>

 <span data-ttu-id="b591e-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="b591e-113">_eMethod_</span></span>
  
> <span data-ttu-id="b591e-114">[in] Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="b591e-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="b591e-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="b591e-115">_First_</span></span>
  
> <span data-ttu-id="b591e-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="b591e-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b591e-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b591e-117">Return value</span></span>

<span data-ttu-id="b591e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b591e-118">S_OK</span></span> 
  
> <span data-ttu-id="b591e-119">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="b591e-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b591e-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b591e-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b591e-121">Um erro de origem inesperada ou desconhecida impedia a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="b591e-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b591e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b591e-122">Remarks</span></span>

<span data-ttu-id="b591e-123">A **macro UlValidateParameters** foi sobressalída pela macro [UlValidateParms.](ulvalidateparms.md)</span><span class="sxs-lookup"><span data-stu-id="b591e-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="b591e-124">**UlValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilar neles.</span><span class="sxs-lookup"><span data-stu-id="b591e-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="b591e-125">Ele ainda compila e funciona corretamente em plataformas Intel, mas **UlValidateParms** é recomendado em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="b591e-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

