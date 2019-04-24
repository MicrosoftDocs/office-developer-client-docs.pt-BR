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
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315299"
---
# <a name="ulpropsize"></a><span data-ttu-id="063ab-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="063ab-103">UlPropSize</span></span>

  
  
<span data-ttu-id="063ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="063ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="063ab-105">Retorna o tamanho de um único valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="063ab-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="063ab-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="063ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="063ab-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="063ab-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="063ab-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="063ab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="063ab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="063ab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="063ab-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="063ab-110">Called by:</span></span>  <br/> |<span data-ttu-id="063ab-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="063ab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="063ab-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="063ab-112">Parameters</span></span>

 <span data-ttu-id="063ab-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="063ab-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="063ab-114">no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define a propriedade a ser medida.</span><span class="sxs-lookup"><span data-stu-id="063ab-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="063ab-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="063ab-115">Return value</span></span>

<span data-ttu-id="063ab-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="063ab-116">S_OK</span></span> 
  
> <span data-ttu-id="063ab-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="063ab-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="063ab-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="063ab-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="063ab-119">Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="063ab-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="063ab-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="063ab-120">Remarks</span></span>

<span data-ttu-id="063ab-121">A função **UlPropSize** retorna o tamanho, em bytes, do valor da propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="063ab-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="063ab-122">Ele ignora o tamanho do restante da estrutura **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="063ab-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

