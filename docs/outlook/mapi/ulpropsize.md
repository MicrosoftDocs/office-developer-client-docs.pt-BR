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
ms.openlocfilehash: 2bfe2841592987c530f6323db94834c1dcb64b2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576635"
---
# <a name="ulpropsize"></a><span data-ttu-id="fa49b-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="fa49b-103">UlPropSize</span></span>

  
  
<span data-ttu-id="fa49b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa49b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa49b-105">Retorna o tamanho de um valor de propriedade exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fa49b-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa49b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fa49b-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa49b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa49b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fa49b-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="fa49b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa49b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa49b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa49b-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="fa49b-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa49b-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="fa49b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="fa49b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa49b-112">Parameters</span></span>

 <span data-ttu-id="fa49b-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="fa49b-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="fa49b-114">[in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo a propriedade a ser medido.</span><span class="sxs-lookup"><span data-stu-id="fa49b-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa49b-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fa49b-115">Return value</span></span>

<span data-ttu-id="fa49b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa49b-116">S_OK</span></span> 
  
> <span data-ttu-id="fa49b-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="fa49b-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="fa49b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="fa49b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="fa49b-119">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="fa49b-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa49b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa49b-120">Remarks</span></span>

<span data-ttu-id="fa49b-121">A função **UlPropSize** retorna o tamanho, em bytes, do valor da propriedade para a propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="fa49b-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="fa49b-122">Ele ignora o tamanho do restante da estrutura **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="fa49b-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

