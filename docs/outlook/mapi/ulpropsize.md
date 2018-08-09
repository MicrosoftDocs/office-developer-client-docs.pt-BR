---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770643"
---
# <a name="ulpropsize"></a><span data-ttu-id="ce8b8-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="ce8b8-103">UlPropSize</span></span>

  
  
<span data-ttu-id="ce8b8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce8b8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce8b8-105">Retorna o tamanho de um valor de propriedade exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce8b8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ce8b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce8b8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce8b8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ce8b8-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ce8b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce8b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ce8b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ce8b8-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ce8b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="ce8b8-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ce8b8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="ce8b8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce8b8-112">Parameters</span></span>

 <span data-ttu-id="ce8b8-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="ce8b8-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="ce8b8-114">[in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo a propriedade a ser medido.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce8b8-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ce8b8-115">Return value</span></span>

<span data-ttu-id="ce8b8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce8b8-116">S_OK</span></span> 
  
> <span data-ttu-id="ce8b8-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="ce8b8-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="ce8b8-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="ce8b8-119">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce8b8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce8b8-120">Remarks</span></span>

<span data-ttu-id="ce8b8-121">A função **UlPropSize** retorna o tamanho, em bytes, do valor da propriedade para a propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="ce8b8-122">Ele ignora o tamanho do restante da estrutura **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="ce8b8-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

