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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410102"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="339ab-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="339ab-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="339ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="339ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="339ab-105">Retorna uma lista de colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="339ab-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="339ab-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="339ab-106">Parameters</span></span>

 <span data-ttu-id="339ab-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="339ab-107">_ulFlags_</span></span>
  
> <span data-ttu-id="339ab-108">no Bitmask de sinalizadores que indica o conjunto de colunas que deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="339ab-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="339ab-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="339ab-109">The following flag can be set:</span></span>
    
<span data-ttu-id="339ab-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="339ab-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="339ab-111">A tabela deve retornar todas as colunas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="339ab-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="339ab-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="339ab-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="339ab-113">bota Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade para o conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="339ab-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="339ab-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="339ab-114">Return value</span></span>

<span data-ttu-id="339ab-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="339ab-115">S_OK</span></span> 
  
> <span data-ttu-id="339ab-116">O conjunto de colunas foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="339ab-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="339ab-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="339ab-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="339ab-118">Outra operação está em andamento, o que impede a inicialização da operação de recuperação do conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="339ab-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="339ab-119">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="339ab-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="339ab-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="339ab-120">Remarks</span></span>

<span data-ttu-id="339ab-121">O método imApitable **:: QueryColumns** pode ser chamado para recuperar:</span><span class="sxs-lookup"><span data-stu-id="339ab-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="339ab-122">A coluna padrão definida para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="339ab-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="339ab-123">A coluna atual definida para uma tabela, conforme estabelecida por uma chamada para o método imApitable [::](imapitable-setcolumns.md) SetColumns.</span><span class="sxs-lookup"><span data-stu-id="339ab-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="339ab-124">A coluna completa definida para uma tabela, as colunas que estão disponíveis, mas não necessariamente fazem parte do conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="339ab-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="339ab-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="339ab-125">Notes to callers</span></span>

<span data-ttu-id="339ab-126">Se você não definir o sinalizador TBL_ALL_COLUMNS, imApitable **:: QueryColumns** retorna o conjunto de colunas padrão ou atual da tabela, dependendo se a tabela foi afetada por uma chamada a IMAPITable **::** SetColumns.</span><span class="sxs-lookup"><span data-stu-id="339ab-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="339ab-127">\*\*\*\* SetColumns altera a ordem e a seleção de colunas no conjunto de colunas de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="339ab-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="339ab-128">Se você definir o sinalizador TBL_ALL_COLUMNS, **QueryColumns** retornará todas as colunas que forem capazes de estar no conjunto de colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="339ab-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="339ab-129">Libere a memória para a matriz de marca de propriedade apontada pelo parâmetro _lpPropTagArray_ chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="339ab-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="339ab-130">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="339ab-130">MFCMAPI reference</span></span>

<span data-ttu-id="339ab-131">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="339ab-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="339ab-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="339ab-132">**File**</span></span>|<span data-ttu-id="339ab-133">**Função**</span><span class="sxs-lookup"><span data-stu-id="339ab-133">**Function**</span></span>|<span data-ttu-id="339ab-134">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="339ab-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="339ab-135">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="339ab-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="339ab-136">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="339ab-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="339ab-137">MFCMAPI usa o método imApitable **:: QueryColumns** para recuperar o conjunto de colunas atual para uma tabela para que o usuário possa editá-lo.</span><span class="sxs-lookup"><span data-stu-id="339ab-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="339ab-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="339ab-138">See also</span></span>



[<span data-ttu-id="339ab-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="339ab-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="339ab-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="339ab-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="339ab-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="339ab-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="339ab-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="339ab-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="339ab-143">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="339ab-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

