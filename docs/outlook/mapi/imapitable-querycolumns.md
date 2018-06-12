---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767336"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="c43fd-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="c43fd-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="c43fd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c43fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c43fd-105">Retorna uma lista das colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="c43fd-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="c43fd-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c43fd-106">Parameters</span></span>

 <span data-ttu-id="c43fd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c43fd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c43fd-108">[in] Bitmask dos sinalizadores que indica qual coluna conjunto deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="c43fd-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="c43fd-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="c43fd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c43fd-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="c43fd-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="c43fd-111">A tabela deve retornar todas as colunas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c43fd-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="c43fd-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c43fd-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c43fd-113">[out] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade para a coluna definido.</span><span class="sxs-lookup"><span data-stu-id="c43fd-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c43fd-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c43fd-114">Return value</span></span>

<span data-ttu-id="c43fd-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c43fd-115">S_OK</span></span> 
  
> <span data-ttu-id="c43fd-116">O conjunto de coluna foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="c43fd-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="c43fd-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c43fd-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c43fd-118">Outra operação é em andamento que impeça a coluna definida a operação de recuperação seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="c43fd-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="c43fd-119">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="c43fd-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c43fd-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c43fd-120">Remarks</span></span>

<span data-ttu-id="c43fd-121">O método **IMAPITable::QueryColumns** pode ser chamado para recuperar:</span><span class="sxs-lookup"><span data-stu-id="c43fd-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="c43fd-122">Coluna padrão definido para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="c43fd-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="c43fd-123">A coluna atual definido para uma tabela, conforme estabelecido por uma chamada ao método [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="c43fd-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="c43fd-124">A coluna completa definidas para uma tabela, as colunas que estão disponíveis, mas não necessariamente parte do conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="c43fd-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="c43fd-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c43fd-125">Notes to callers</span></span>

<span data-ttu-id="c43fd-126">Se você não definir o sinalizador TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** retorna padrão uma tabela ou conjunto de coluna atual, dependendo se a tabela foi afetada por uma chamada para **IMAPITable::SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="c43fd-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="c43fd-127">**SetColumns** altera o sentido e seleção de colunas no conjunto de colunas de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="c43fd-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="c43fd-128">Se você definir o sinalizador TBL_ALL_COLUMNS, **QueryColumns** retorna todas as colunas que são capazes de sendo no conjunto de coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="c43fd-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="c43fd-129">Libere a memória para a matriz de marca de propriedade apontada pelo parâmetro _lpPropTagArray_ chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c43fd-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c43fd-130">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c43fd-130">MFCMAPI reference</span></span>

<span data-ttu-id="c43fd-131">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c43fd-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c43fd-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c43fd-132">**File**</span></span>|<span data-ttu-id="c43fd-133">**Function**</span><span class="sxs-lookup"><span data-stu-id="c43fd-133">**Function**</span></span>|<span data-ttu-id="c43fd-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c43fd-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c43fd-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c43fd-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c43fd-136">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="c43fd-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="c43fd-137">MFCMAPI usa o método **IMAPITable::QueryColumns** para recuperar a coluna atual, definido para uma tabela para que o usuário possa ser editado.</span><span class="sxs-lookup"><span data-stu-id="c43fd-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c43fd-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c43fd-138">See also</span></span>



[<span data-ttu-id="c43fd-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c43fd-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="c43fd-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c43fd-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c43fd-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c43fd-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c43fd-142">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c43fd-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c43fd-143">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c43fd-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

