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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6c149a215a048b96408025e08df55972fa989f46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767707"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="00283-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="00283-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="00283-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00283-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00283-105">Recupera uma linha com base em sua posição na tabela.</span><span class="sxs-lookup"><span data-stu-id="00283-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="00283-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00283-106">Parameters</span></span>

 <span data-ttu-id="00283-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="00283-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="00283-108">[in] O número da linha para o qual retornar propriedades.</span><span class="sxs-lookup"><span data-stu-id="00283-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="00283-109">O valor no parâmetro _ulRowNumber_ pode ser qualquer valor de 0, que indica a primeira linha na tabela, por meio de n - 1, que indica a última linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="00283-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="00283-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="00283-110">_lppSRow_</span></span>
  
> <span data-ttu-id="00283-111">[out] Um ponteiro para um ponteiro para uma estrutura de [SRow](srow.md) que descreve a linha de destino.</span><span class="sxs-lookup"><span data-stu-id="00283-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00283-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="00283-112">Return value</span></span>

<span data-ttu-id="00283-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="00283-113">S_OK</span></span> 
  
> <span data-ttu-id="00283-114">A linha foi recuperada com êxito, ou uma linha para o número da linha especificada pelo parâmetro _ulRowNumber_ não existe.</span><span class="sxs-lookup"><span data-stu-id="00283-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00283-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="00283-115">Remarks</span></span>

<span data-ttu-id="00283-116">O método **ITableData::HrEnumRow** recupera uma linha com base em um número sequencial.</span><span class="sxs-lookup"><span data-stu-id="00283-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="00283-117">Este número representa a ordem de inserção (0 indica que a primeira linha e o número de linhas menos 1 indica a última linha).</span><span class="sxs-lookup"><span data-stu-id="00283-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="00283-118">MAPI mantém nesta ordem cronológica de inserção de linha para o tempo de vida do objeto de dados de tabela.</span><span class="sxs-lookup"><span data-stu-id="00283-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="00283-119">Se o número especificado na _ulRowNumber_ não corresponde a uma linha na tabela, **HrEnumRow** Retorna S_OK e define o parâmetro _lppSRow_ como NULL.</span><span class="sxs-lookup"><span data-stu-id="00283-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="00283-120">MAPI aloca memória para a estrutura de **SRow** retornada usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) quando o objeto de dados de tabela é criado.</span><span class="sxs-lookup"><span data-stu-id="00283-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="00283-121">O chamador deve liberar essa memória chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="00283-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="00283-122">Para recuperar linhas de uma tabela na ordem em que foram inseridos, os usuários de objeto de dados de tabela chame o método de **HrEnumRow** .</span><span class="sxs-lookup"><span data-stu-id="00283-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00283-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="00283-123">See also</span></span>



[<span data-ttu-id="00283-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="00283-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="00283-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00283-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00283-126">SRow</span><span class="sxs-lookup"><span data-stu-id="00283-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="00283-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00283-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

