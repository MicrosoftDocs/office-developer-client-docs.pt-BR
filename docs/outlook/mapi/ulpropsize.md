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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416899"
---
# <a name="ulpropsize"></a><span data-ttu-id="de62d-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="de62d-103">UlPropSize</span></span>

  
  
<span data-ttu-id="de62d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de62d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de62d-105">Retorna o tamanho de um único valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="de62d-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de62d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="de62d-106">Header file:</span></span>  <br/> |<span data-ttu-id="de62d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="de62d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="de62d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="de62d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="de62d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="de62d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="de62d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="de62d-110">Called by:</span></span>  <br/> |<span data-ttu-id="de62d-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="de62d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="de62d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de62d-112">Parameters</span></span>

 <span data-ttu-id="de62d-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="de62d-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="de62d-114">no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define a propriedade a ser medida.</span><span class="sxs-lookup"><span data-stu-id="de62d-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="de62d-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="de62d-115">Return value</span></span>

<span data-ttu-id="de62d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="de62d-116">S_OK</span></span> 
  
> <span data-ttu-id="de62d-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="de62d-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="de62d-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="de62d-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="de62d-119">Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="de62d-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de62d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="de62d-120">Remarks</span></span>

<span data-ttu-id="de62d-121">A função **UlPropSize** retorna o tamanho, em bytes, do valor da propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="de62d-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="de62d-122">Ele ignora o tamanho do restante da estrutura **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="de62d-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

