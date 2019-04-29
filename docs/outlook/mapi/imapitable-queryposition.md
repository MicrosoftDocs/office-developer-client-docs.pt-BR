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
# <a name="imapitablequeryposition"></a><span data-ttu-id="d2eac-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="d2eac-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="d2eac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2eac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2eac-105">Recupera a posição de linha atual da tabela do cursor, com base em um valor fracionário.</span><span class="sxs-lookup"><span data-stu-id="d2eac-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="d2eac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2eac-106">Parameters</span></span>

 <span data-ttu-id="d2eac-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="d2eac-107">_lpulRow_</span></span>
  
> <span data-ttu-id="d2eac-108">bota Ponteiro para o número da linha atual.</span><span class="sxs-lookup"><span data-stu-id="d2eac-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="d2eac-109">O número da linha é baseado em zero; a primeira linha da tabela é zero.</span><span class="sxs-lookup"><span data-stu-id="d2eac-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="d2eac-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="d2eac-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="d2eac-111">bota Ponteiro para o numerador da fração que identifica a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="d2eac-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="d2eac-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="d2eac-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="d2eac-113">bota Ponteiro para o denominador da fração que identifica a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="d2eac-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="d2eac-114">O parâmetro _lpulDenominator_ não pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2eac-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d2eac-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d2eac-115">Return value</span></span>

<span data-ttu-id="d2eac-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2eac-116">S_OK</span></span> 
  
> <span data-ttu-id="d2eac-117">O método retornou valores válidos em _lpulRow_, _lpulNumerator_e _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="d2eac-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2eac-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2eac-118">Remarks</span></span>

<span data-ttu-id="d2eac-119">O método imApitable **:: QueryPosition** determina a posição da linha atual e retorna o número da linha atual e um valor fracionário que indica sua posição relativa ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="d2eac-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="d2eac-120">MAPI define a linha atual como a próxima linha a ser lida.</span><span class="sxs-lookup"><span data-stu-id="d2eac-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d2eac-121">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="d2eac-121">Notes to implementers</span></span>

<span data-ttu-id="d2eac-122">Você não precisa retornar o número exato de linhas na tabela para o parâmetro _lpulDenominator_ ; pode ser uma aproximação.</span><span class="sxs-lookup"><span data-stu-id="d2eac-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="d2eac-123">Se você não puder determinar a linha atual, retorne um valor de 0xFFFFFFFF no _lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="d2eac-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d2eac-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d2eac-124">Notes to callers</span></span>

<span data-ttu-id="d2eac-125">Você pode usar o **QueryPosition** para posicionar uma caixa de rolagem em uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="d2eac-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="d2eac-126">Por exemplo, em uma tabela contendo 100 linhas, se **QueryPosition** retornar um valor de 75 no parâmetro _lpulNumerator_ , 100 no parâmetro _LpulDenominator_ e 75 no parâmetro _lpulRow_ , você poderá posicionar a caixa de rolagem 3/4 de a maneira pela barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="d2eac-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="d2eac-127">Não confie no valor no _lpulDenominator_ como o número de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="d2eac-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="d2eac-128">**QueryPosition** não pode sempre identificar a linha exata em que o cursor está posicionado.</span><span class="sxs-lookup"><span data-stu-id="d2eac-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="d2eac-129">Uma chamada para **QueryPosition** pode envolver grandes quantidades de memória, particularmente para grandes tabelas categorizadas.</span><span class="sxs-lookup"><span data-stu-id="d2eac-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="d2eac-130">Se o parâmetro _lpulRow_ for definido como 0xFFFFFFFF, muita memória era necessária para o **QueryPosition** para determinar a linha atual.</span><span class="sxs-lookup"><span data-stu-id="d2eac-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="d2eac-131">Chame o método imApitable [:: SeekRowApprox](imapitable-seekrowapprox.md) para posicionar a tabela na linha identificada pelos parâmetros _lpulNumerator_ e _lpulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="d2eac-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="d2eac-132">No enTanto, nem sempre espere **SeekRowApprox** estabelecer como a posição atual o mesmo **QueryPosition** de linha teria se a memória não tivesse sido um fator.</span><span class="sxs-lookup"><span data-stu-id="d2eac-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2eac-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2eac-133">See also</span></span>



[<span data-ttu-id="d2eac-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="d2eac-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="d2eac-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2eac-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

