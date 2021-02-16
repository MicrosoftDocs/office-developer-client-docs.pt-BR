---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418369"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="e5a7d-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="e5a7d-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="e5a7d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5a7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5a7d-105">Recupera uma linha com base em sua posição na tabela.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="e5a7d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5a7d-106">Parameters</span></span>

 <span data-ttu-id="e5a7d-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="e5a7d-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="e5a7d-108">[in] O número da linha para a qual as propriedades de retorno são retornadas.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="e5a7d-109">O valor no parâmetro  _ulRowNumber_ pode ser qualquer valor de 0, que indica a primeira linha na tabela, até n - 1, que indica a última linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="e5a7d-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="e5a7d-110">_lppSRow_</span></span>
  
> <span data-ttu-id="e5a7d-111">[out] Um ponteiro para um ponteiro para uma [estrutura SRow](srow.md) que descreve a linha de destino.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e5a7d-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e5a7d-112">Return value</span></span>

<span data-ttu-id="e5a7d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5a7d-113">S_OK</span></span> 
  
> <span data-ttu-id="e5a7d-114">A linha foi recuperada com êxito ou não existe uma linha para o número de linha especificado pelo _parâmetro ulRowNumber._</span><span class="sxs-lookup"><span data-stu-id="e5a7d-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e5a7d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5a7d-115">Remarks</span></span>

<span data-ttu-id="e5a7d-116">O **método ITableData::HrEnumRow** recupera uma linha com base em um número sequencial.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="e5a7d-117">Esse número representa a ordem de inserção (0 indica a primeira linha e o número de linhas menos 1 indica a última linha).</span><span class="sxs-lookup"><span data-stu-id="e5a7d-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="e5a7d-118">O MAPI mantém essa ordem cronológica de inserção de linha durante o tempo de vida do objeto de dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="e5a7d-119">Se o número especificado em  _ulRowNumber_ não corresponder a uma linha na tabela, **HrEnumRow** retornará S_OK e define o parâmetro  _lppSRow_ como NULL.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="e5a7d-120">MAPI aloca memória para a estrutura **SRow** retornada usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) quando o objeto de dados de tabela é criado.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="e5a7d-121">O chamador deve liberar essa memória chamando a [função MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="e5a7d-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="e5a7d-122">Para recuperar linhas de uma tabela na ordem em que foram inseridas, os usuários do objeto de dados de tabela chamam o **método HrEnumRow.**</span><span class="sxs-lookup"><span data-stu-id="e5a7d-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5a7d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5a7d-123">See also</span></span>



[<span data-ttu-id="e5a7d-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e5a7d-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e5a7d-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e5a7d-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e5a7d-126">SRow</span><span class="sxs-lookup"><span data-stu-id="e5a7d-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="e5a7d-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5a7d-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

