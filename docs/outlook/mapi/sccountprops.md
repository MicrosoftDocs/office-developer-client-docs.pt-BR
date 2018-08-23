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
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583348"
---
# <a name="sccountprops"></a><span data-ttu-id="ede72-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="ede72-103">ScCountProps</span></span>

  
  
<span data-ttu-id="ede72-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ede72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ede72-105">Determina o tamanho, em bytes, de uma matriz de valores de propriedade e valida a memória associada a matriz.</span><span class="sxs-lookup"><span data-stu-id="ede72-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ede72-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ede72-106">Header file:</span></span>  <br/> |<span data-ttu-id="ede72-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ede72-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ede72-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ede72-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ede72-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ede72-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ede72-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ede72-110">Called by:</span></span>  <br/> |<span data-ttu-id="ede72-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ede72-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="ede72-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ede72-112">Parameters</span></span>

 <span data-ttu-id="ede72-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="ede72-113">_cprop_</span></span>
  
> <span data-ttu-id="ede72-114">[in] Contagem de propriedades na matriz indicado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="ede72-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="ede72-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="ede72-115">_rgprop_</span></span>
  
> <span data-ttu-id="ede72-116">[in] Ponteiro para um intervalo em uma matriz de estruturas de [SPropValue](spropvalue.md) que define as propriedades cujo tamanho é seja determinado.</span><span class="sxs-lookup"><span data-stu-id="ede72-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="ede72-117">Esse intervalo não necessariamente inicia no início da matriz.</span><span class="sxs-lookup"><span data-stu-id="ede72-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="ede72-118">_PCB_</span><span class="sxs-lookup"><span data-stu-id="ede72-118">_pcb_</span></span>
  
> <span data-ttu-id="ede72-119">[out] Ponteiro opcional para o tamanho, em bytes, de matriz de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ede72-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ede72-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ede72-120">Return value</span></span>

<span data-ttu-id="ede72-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ede72-121">S_OK</span></span> 
  
> <span data-ttu-id="ede72-122">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ede72-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="ede72-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ede72-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="ede72-124">Pelo menos uma propriedade da matriz de valores de propriedade tem um identificador de PROP_ID_NULL ou PROP_ID_INVALID ou a matriz de propriedade contém uma propriedade de vários valores sem valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ede72-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ede72-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ede72-125">Remarks</span></span>

<span data-ttu-id="ede72-126">Se NULL é passada no parâmetro _pcb_ , a função **ScCountProps** valida a matriz de notificações, mas nenhum contando é feito.</span><span class="sxs-lookup"><span data-stu-id="ede72-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="ede72-127">Se um valor não-nulo é passado _pcb_, a função **ScCountNotifications** determina o tamanho da matriz e armazena a causa _pcb_.</span><span class="sxs-lookup"><span data-stu-id="ede72-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="ede72-128">O parâmetro _pcb_ deve ser grande o suficiente para conter toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="ede72-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="ede72-129">Conforme ele está contando, **ScCountProps** valida a memória associada a matriz.</span><span class="sxs-lookup"><span data-stu-id="ede72-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="ede72-130">**ScCountProps** funciona apenas com sobre quais MAPI tem informações de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ede72-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ede72-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ede72-131">See also</span></span>



[<span data-ttu-id="ede72-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="ede72-132">PropCopyMore</span></span>](propcopymore.md)

