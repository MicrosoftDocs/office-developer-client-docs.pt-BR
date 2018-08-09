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
ms.openlocfilehash: 921417d8fc73ca9c1f126b2cb0add23f6625e3f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770708"
---
# <a name="validateparameters"></a><span data-ttu-id="a781f-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="a781f-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="a781f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a781f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a781f-105">Chama uma função interna para verificar que os aplicativos de cliente parâmetros já se passaram a provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="a781f-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a781f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a781f-106">Header file:</span></span>  <br/> |<span data-ttu-id="a781f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a781f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a781f-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a781f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a781f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a781f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a781f-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a781f-110">Called by:</span></span>  <br/> |<span data-ttu-id="a781f-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a781f-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="a781f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a781f-112">Parameters</span></span>

 <span data-ttu-id="a781f-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="a781f-113">_eMethod_</span></span>
  
> <span data-ttu-id="a781f-114">[in] Especifica o enumeração, o método para validar.</span><span class="sxs-lookup"><span data-stu-id="a781f-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="a781f-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="a781f-115">_First_</span></span>
  
> <span data-ttu-id="a781f-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="a781f-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a781f-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a781f-117">Return value</span></span>

<span data-ttu-id="a781f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a781f-118">S_OK</span></span> 
  
> <span data-ttu-id="a781f-119">Todos os parâmetros são válidos.</span><span class="sxs-lookup"><span data-stu-id="a781f-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="a781f-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="a781f-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="a781f-121">Um ou mais dos parâmetros não são válidos.</span><span class="sxs-lookup"><span data-stu-id="a781f-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a781f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a781f-122">Remarks</span></span>

<span data-ttu-id="a781f-123">A macro **ValidateParameters** foi substituída pela macro [ValidateParms](validateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="a781f-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="a781f-124">**ValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilação neles.</span><span class="sxs-lookup"><span data-stu-id="a781f-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="a781f-125">Ele ainda é compilado e funciona corretamente em plataformas Intel, mas **ValidateParms** é recomendado em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="a781f-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

