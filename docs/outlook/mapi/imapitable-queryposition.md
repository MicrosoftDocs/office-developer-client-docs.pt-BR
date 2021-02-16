---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415660"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="ef387-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="ef387-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="ef387-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef387-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef387-105">Recupera a posição atual da linha da tabela do cursor, com base em um valor fracionado.</span><span class="sxs-lookup"><span data-stu-id="ef387-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="ef387-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef387-106">Parameters</span></span>

 <span data-ttu-id="ef387-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="ef387-107">_lpulRow_</span></span>
  
> <span data-ttu-id="ef387-108">[out] Ponteiro para o número da linha atual.</span><span class="sxs-lookup"><span data-stu-id="ef387-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="ef387-109">O número da linha é baseado em zero; a primeira linha na tabela é zero.</span><span class="sxs-lookup"><span data-stu-id="ef387-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="ef387-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="ef387-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="ef387-111">[out] Ponteiro para o numerador para a fração que identifica a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="ef387-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="ef387-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="ef387-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="ef387-113">[out] Ponteiro para o denominador da fração que identifica a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="ef387-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="ef387-114">O  _parâmetro lpulDenominator_ não pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="ef387-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ef387-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ef387-115">Return value</span></span>

<span data-ttu-id="ef387-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef387-116">S_OK</span></span> 
  
> <span data-ttu-id="ef387-117">O método retornou valores válidos  _em lpulRow_,  _lpulNumerator_ e  _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="ef387-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef387-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef387-118">Remarks</span></span>

<span data-ttu-id="ef387-119">O **método IMAPITable::QueryPosition** determina a posição da linha atual e retorna o número da linha atual e um valor fracionado indicando sua posição relativa ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="ef387-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="ef387-120">MAPI define a linha atual como a próxima linha a ser lida.</span><span class="sxs-lookup"><span data-stu-id="ef387-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ef387-121">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ef387-121">Notes to implementers</span></span>

<span data-ttu-id="ef387-122">Não é necessário retornar o número exato de linhas na tabela para o parâmetro  _lpulDenominator;_ pode ser uma aproximação.</span><span class="sxs-lookup"><span data-stu-id="ef387-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="ef387-123">Se você não puder determinar a linha atual, retorne um valor de 0xFFFFFFFF em  _lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="ef387-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ef387-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ef387-124">Notes to callers</span></span>

<span data-ttu-id="ef387-125">Você pode usar **QueryPosition para** posicionar uma caixa de rolagem em uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ef387-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="ef387-126">Por exemplo, em uma tabela contendo 100 linhas, se **QueryPosition** retornar um valor de 75 no parâmetro  _lpulNumerator,_ 100 no parâmetro  _lpulDenominator_ e 75 no parâmetro  _lpulRow,_ você poderá posicionar a caixa de rolagem 3/4 do caminho pela barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ef387-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="ef387-127">Não confie no valor em  _lpulDenominator_ sendo o número de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="ef387-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="ef387-128">**QueryPosition** nem sempre pode identificar a linha exata na qual o cursor está posicionado.</span><span class="sxs-lookup"><span data-stu-id="ef387-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="ef387-129">Uma chamada para **QueryPosition pode** envolver grandes quantidades de memória, especialmente para tabelas categorizadas grandes.</span><span class="sxs-lookup"><span data-stu-id="ef387-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="ef387-130">Se o  _parâmetro lpulRow_ estiver definido como 0xFFFFFFFF, muita memória foi necessária para **que QueryPosition** determine a linha atual.</span><span class="sxs-lookup"><span data-stu-id="ef387-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="ef387-131">Chame o método [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) para posicionar a tabela na linha identificada pelos parâmetros _lpulNumerator_ e _lpulDenominator._</span><span class="sxs-lookup"><span data-stu-id="ef387-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="ef387-132">No entanto, nem sempre espere **que SeekRowApprox** estabeleça como a posição atual a mesma **linha que QueryPosition** teria se a memória não tivesse sido um fator.</span><span class="sxs-lookup"><span data-stu-id="ef387-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef387-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef387-133">See also</span></span>



[<span data-ttu-id="ef387-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="ef387-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="ef387-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef387-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

