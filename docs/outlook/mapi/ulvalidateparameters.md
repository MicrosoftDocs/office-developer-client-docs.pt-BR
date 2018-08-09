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
ms.openlocfilehash: 42b2f8e9695b1dbdc5ea02db5a4e8a0eaba6099c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770669"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="0dfc2-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="0dfc2-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="0dfc2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0dfc2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0dfc2-105">Chama uma função interna para verificar que os aplicativos de cliente parâmetros tem passado para provedores de serviços e MAPI.</span><span class="sxs-lookup"><span data-stu-id="0dfc2-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dfc2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0dfc2-106">Header file:</span></span>  <br/> |<span data-ttu-id="0dfc2-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0dfc2-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0dfc2-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0dfc2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0dfc2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0dfc2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0dfc2-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0dfc2-110">Called by:</span></span>  <br/> |<span data-ttu-id="0dfc2-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="0dfc2-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="0dfc2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0dfc2-112">Parameters</span></span>

 <span data-ttu-id="0dfc2-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="0dfc2-113">_eMethod_</span></span>
  
> <span data-ttu-id="0dfc2-114">[in] Especifica o enumeração, o método para validar.</span><span class="sxs-lookup"><span data-stu-id="0dfc2-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="0dfc2-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="0dfc2-115">_First_</span></span>
  
> <span data-ttu-id="0dfc2-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="0dfc2-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0dfc2-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0dfc2-117">Return value</span></span>

<span data-ttu-id="0dfc2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0dfc2-118">S_OK</span></span> 
  
> <span data-ttu-id="0dfc2-119">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="0dfc2-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0dfc2-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="0dfc2-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="0dfc2-121">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="0dfc2-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0dfc2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dfc2-122">Remarks</span></span>

<span data-ttu-id="0dfc2-123">A macro **UlValidateParameters** foi substituída pela macro [UlValidateParms](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="0dfc2-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="0dfc2-124">**UlValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilação neles.</span><span class="sxs-lookup"><span data-stu-id="0dfc2-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="0dfc2-125">Ele ainda é compilado e funciona corretamente em plataformas Intel, mas **UlValidateParms** é recomendado em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="0dfc2-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

