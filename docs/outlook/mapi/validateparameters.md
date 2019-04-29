---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425196"
---
# <a name="validateparameters"></a><span data-ttu-id="6c2a2-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="6c2a2-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="6c2a2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c2a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c2a2-105">Chama uma função interna para verificar os parâmetros que os aplicativos clientes passaram para os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="6c2a2-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c2a2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6c2a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="6c2a2-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6c2a2-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6c2a2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6c2a2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6c2a2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6c2a2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6c2a2-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6c2a2-110">Called by:</span></span>  <br/> |<span data-ttu-id="6c2a2-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6c2a2-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="6c2a2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c2a2-112">Parameters</span></span>

 <span data-ttu-id="6c2a2-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="6c2a2-113">_eMethod_</span></span>
  
> <span data-ttu-id="6c2a2-114">no Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="6c2a2-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="6c2a2-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="6c2a2-115">_First_</span></span>
  
> <span data-ttu-id="6c2a2-116">no Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="6c2a2-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c2a2-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6c2a2-117">Return value</span></span>

<span data-ttu-id="6c2a2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c2a2-118">S_OK</span></span> 
  
> <span data-ttu-id="6c2a2-119">Todos os parâmetros são válidos.</span><span class="sxs-lookup"><span data-stu-id="6c2a2-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="6c2a2-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="6c2a2-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="6c2a2-121">Um ou mais parâmetros não são válidos.</span><span class="sxs-lookup"><span data-stu-id="6c2a2-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c2a2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c2a2-122">Remarks</span></span>

<span data-ttu-id="6c2a2-123">A \*\*\*\* macro ValidateParameters foi substituída pela macro [ValidateParms](validateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="6c2a2-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="6c2a2-124">**ValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilá-las.</span><span class="sxs-lookup"><span data-stu-id="6c2a2-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="6c2a2-125">Ele ainda é compilado e funciona corretamente nas plataformas Intel, mas o **ValidateParms** é recomendado em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="6c2a2-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

