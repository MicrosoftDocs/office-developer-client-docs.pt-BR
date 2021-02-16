---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434764"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="efb39-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="efb39-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="efb39-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efb39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efb39-105">Recupera uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="efb39-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="efb39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efb39-106">Parameters</span></span>

 <span data-ttu-id="efb39-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="efb39-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="efb39-108">[in] Um ponteiro para uma estrutura de valores de propriedade que descreve a coluna de índice para a linha a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="efb39-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="efb39-109">O **membro ulPropTag** da estrutura de valores de propriedade deve conter a mesma marca de propriedade que o parâmetro _ulPropTagIndexColumn_ da chamada para a função [CreateTable,](createtable.md) que acessa a implementação [de ITableData.](itabledataiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="efb39-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="efb39-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="efb39-110">_lppSRow_</span></span>
  
> <span data-ttu-id="efb39-111">[out] Um ponteiro para um ponteiro para a linha recuperada.</span><span class="sxs-lookup"><span data-stu-id="efb39-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="efb39-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="efb39-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="efb39-113">[in, out] Na entrada, um ponteiro válido ou NULL, que indica que nenhuma informação precisa ser retornada.</span><span class="sxs-lookup"><span data-stu-id="efb39-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="efb39-114">Na saída, um ponteiro válido que aponta para o número da linha, um número sequencial que identifica a posição da linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="efb39-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efb39-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="efb39-115">Return value</span></span>

<span data-ttu-id="efb39-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="efb39-116">S_OK</span></span> 
  
> <span data-ttu-id="efb39-117">A linha foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="efb39-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="efb39-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="efb39-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="efb39-119">A [estrutura SPropValue](spropvalue.md) para a  _qual lpSPropValue_ aponta não contém a propriedade da coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="efb39-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="efb39-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="efb39-120">Remarks</span></span>

<span data-ttu-id="efb39-121">O método **ITableData::HrQueryRow** recupera todas as propriedades da linha que tem uma coluna de índice que corresponde ao valor da coluna de índice incluída na estrutura de propriedades apontada por  _lpSPropValue_.</span><span class="sxs-lookup"><span data-stu-id="efb39-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="efb39-122">**HrQueryRow** também retorna o número da linha, se o chamador solicitar, que identifica a posição da linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="efb39-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="efb39-123">Como **HrQueryRow** não modifica a estrutura **SPropValue** apontada por  _lpSPropValue_, os chamadores devem liberar a estrutura **quando HrQueryRow** retornar.</span><span class="sxs-lookup"><span data-stu-id="efb39-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="efb39-124">Os chamadores também devem liberar a **estrutura SRow** que contém a linha recuperada.</span><span class="sxs-lookup"><span data-stu-id="efb39-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efb39-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="efb39-125">See also</span></span>



[<span data-ttu-id="efb39-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="efb39-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="efb39-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="efb39-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="efb39-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="efb39-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="efb39-129">SRow</span><span class="sxs-lookup"><span data-stu-id="efb39-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="efb39-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="efb39-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

