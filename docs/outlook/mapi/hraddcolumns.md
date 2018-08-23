---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580730"
---
# <a name="hraddcolumns"></a><span data-ttu-id="78e14-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="78e14-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="78e14-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78e14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78e14-105">Adiciona ou move colunas para o início de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="78e14-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78e14-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="78e14-106">Header file:</span></span>  <br/> |<span data-ttu-id="78e14-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="78e14-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="78e14-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="78e14-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="78e14-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="78e14-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="78e14-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="78e14-110">Called by:</span></span>  <br/> |<span data-ttu-id="78e14-111">Provedores de serviços e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="78e14-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="78e14-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78e14-112">Parameters</span></span>

 <span data-ttu-id="78e14-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="78e14-113">_lptbl_</span></span>
  
> <span data-ttu-id="78e14-114">[in] Ponteiro para a tabela MAPI afetado.</span><span class="sxs-lookup"><span data-stu-id="78e14-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="78e14-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="78e14-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="78e14-116">[in] Ponteiro para uma estrutura **SPropTagArray** que contém uma matriz de marcas de propriedade para as propriedades sejam adicionados ou movidos para o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="78e14-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="78e14-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="78e14-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="78e14-118">[in] Ponteiro para a função **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="78e14-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="78e14-119">Usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="78e14-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="78e14-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="78e14-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="78e14-121">[in] Ponteiro para a função **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="78e14-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="78e14-122">Usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="78e14-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="78e14-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="78e14-123">Return value</span></span>

 <span data-ttu-id="78e14-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="78e14-124">**S_OK**</span></span>
  
> <span data-ttu-id="78e14-125">A chamada foi bem-sucedida e das colunas especificadas foram movidas ou adicionadas.</span><span class="sxs-lookup"><span data-stu-id="78e14-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78e14-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="78e14-126">Remarks</span></span>

<span data-ttu-id="78e14-127">A função **HrAddColumns** é equivalente ao uso **HrAddColumnsEx** com _lpfnFilterColumns_ definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="78e14-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78e14-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="78e14-128">See also</span></span>



[<span data-ttu-id="78e14-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="78e14-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="78e14-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="78e14-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="78e14-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="78e14-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="78e14-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="78e14-132">SPropTagArray</span></span>](sproptagarray.md)

