---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404971"
---
# <a name="sccountprops"></a><span data-ttu-id="a40a7-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="a40a7-103">ScCountProps</span></span>

  
  
<span data-ttu-id="a40a7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a40a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a40a7-105">Determina o tamanho, em bytes, de uma matriz de valor de propriedade e valida a memória associada à matriz.</span><span class="sxs-lookup"><span data-stu-id="a40a7-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a40a7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a40a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="a40a7-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="a40a7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a40a7-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a40a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a40a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a40a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a40a7-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a40a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="a40a7-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a40a7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="a40a7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a40a7-112">Parameters</span></span>

 <span data-ttu-id="a40a7-113">_cProp_</span><span class="sxs-lookup"><span data-stu-id="a40a7-113">_cprop_</span></span>
  
> <span data-ttu-id="a40a7-114">no Contagem de propriedades na matriz indicada pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="a40a7-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="a40a7-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="a40a7-115">_rgprop_</span></span>
  
> <span data-ttu-id="a40a7-116">no Ponteiro para um intervalo em uma matriz de estruturas [SPropValue](spropvalue.md) que define as propriedades cujo tamanho deve ser determinado.</span><span class="sxs-lookup"><span data-stu-id="a40a7-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="a40a7-117">Esse intervalo não começa necessariamente no início da matriz.</span><span class="sxs-lookup"><span data-stu-id="a40a7-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="a40a7-118">_PCB_</span><span class="sxs-lookup"><span data-stu-id="a40a7-118">_pcb_</span></span>
  
> <span data-ttu-id="a40a7-119">bota Ponteiro opcional para o tamanho, em bytes, da matriz de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a40a7-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a40a7-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a40a7-120">Return value</span></span>

<span data-ttu-id="a40a7-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a40a7-121">S_OK</span></span> 
  
> <span data-ttu-id="a40a7-122">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a40a7-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a40a7-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a40a7-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="a40a7-124">Pelo menos uma propriedade na matriz de valor de propriedade tem um identificador de PROP_ID_NULL ou PROP_ID_INVALID, ou a matriz de propriedade contém uma propriedade com vários valores sem valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a40a7-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a40a7-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a40a7-125">Remarks</span></span>

<span data-ttu-id="a40a7-126">Se NULL for passado no parâmetro _PCB_ , a função **ScCountProps** validará a matriz de notificações, mas nenhuma contagem será feita.</span><span class="sxs-lookup"><span data-stu-id="a40a7-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="a40a7-127">Se um valor não nulo for passado em _PCB_, a função **ScCountNotifications** determinará o tamanho da matriz e armazenará a _PCB_de causa.</span><span class="sxs-lookup"><span data-stu-id="a40a7-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="a40a7-128">O parâmetro _PCB_ deve ser grande o suficiente para conter toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="a40a7-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="a40a7-129">Conforme a contagem, **ScCountProps** valida a memória associada à matriz.</span><span class="sxs-lookup"><span data-stu-id="a40a7-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="a40a7-130">**ScCountProps** funciona apenas com as propriedades sobre as quais o MAPI tem informações.</span><span class="sxs-lookup"><span data-stu-id="a40a7-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a40a7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a40a7-131">See also</span></span>



[<span data-ttu-id="a40a7-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="a40a7-132">PropCopyMore</span></span>](propcopymore.md)

