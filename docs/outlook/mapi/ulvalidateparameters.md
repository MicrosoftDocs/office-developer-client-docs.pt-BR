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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315285"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="24d90-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="24d90-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="24d90-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24d90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24d90-105">Chama uma função interna para verificar os parâmetros que os aplicativos clientes passaram para os provedores de serviço e MAPI.</span><span class="sxs-lookup"><span data-stu-id="24d90-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24d90-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="24d90-106">Header file:</span></span>  <br/> |<span data-ttu-id="24d90-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="24d90-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="24d90-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="24d90-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="24d90-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="24d90-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="24d90-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="24d90-110">Called by:</span></span>  <br/> |<span data-ttu-id="24d90-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="24d90-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="24d90-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24d90-112">Parameters</span></span>

 <span data-ttu-id="24d90-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="24d90-113">_eMethod_</span></span>
  
> <span data-ttu-id="24d90-114">no Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="24d90-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="24d90-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="24d90-115">_First_</span></span>
  
> <span data-ttu-id="24d90-116">no Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="24d90-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24d90-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="24d90-117">Return value</span></span>

<span data-ttu-id="24d90-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="24d90-118">S_OK</span></span> 
  
> <span data-ttu-id="24d90-119">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="24d90-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="24d90-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="24d90-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="24d90-121">Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="24d90-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24d90-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="24d90-122">Remarks</span></span>

<span data-ttu-id="24d90-123">A macro **UlValidateParameters** foi substituída pela macro [UlValidateParms](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="24d90-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="24d90-124">O **UlValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilá-las.</span><span class="sxs-lookup"><span data-stu-id="24d90-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="24d90-125">Ele ainda é compilado e funciona corretamente nas plataformas Intel, mas o **UlValidateParms** é recomendado em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="24d90-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

