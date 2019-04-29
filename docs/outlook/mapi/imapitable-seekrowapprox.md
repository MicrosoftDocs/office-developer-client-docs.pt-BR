---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412146"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="3921b-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="3921b-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="3921b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3921b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3921b-105">Move o cursor para uma posição fracionária aproximada na tabela.</span><span class="sxs-lookup"><span data-stu-id="3921b-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="3921b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3921b-106">Parameters</span></span>

 <span data-ttu-id="3921b-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="3921b-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="3921b-108">no Ponteiro para o numerador da fração que representa a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="3921b-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="3921b-109">Se o parâmetro _ulNumerator_ for zero, o cursor será posicionado no início da tabela, independente do valor do denominador.</span><span class="sxs-lookup"><span data-stu-id="3921b-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="3921b-110">Se _ulNumerator_ for igual ao parâmetro _ulDenominator_ , o cursor será posicionado após a última linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="3921b-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="3921b-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="3921b-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="3921b-112">no Ponteiro para o denominador da fração que representa a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="3921b-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="3921b-113">O parâmetro _ulDenominator_ não pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="3921b-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3921b-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3921b-114">Return value</span></span>

<span data-ttu-id="3921b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="3921b-115">S_OK</span></span> 
  
> <span data-ttu-id="3921b-116">A operação de busca foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3921b-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="3921b-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3921b-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3921b-118">Outra operação está em andamento, o que impede a inicialização da operação de busca da linha.</span><span class="sxs-lookup"><span data-stu-id="3921b-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="3921b-119">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="3921b-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3921b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3921b-120">Remarks</span></span>

<span data-ttu-id="3921b-121">A posição do cursor em uma tabela após uma chamada para o método imApitable **:: SeekRowApprox** é a fração heurística e pode não ser exata.</span><span class="sxs-lookup"><span data-stu-id="3921b-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="3921b-122">Por exemplo, determinados provedores podem implementar uma tabela na parte superior de uma árvore binária, tratando o ponto intermediário da tabela como a parte superior da árvore por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="3921b-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="3921b-123">Se a árvore não for balanceada, o ponto intermediário usado poderá não ser exatamente no meio da tabela.</span><span class="sxs-lookup"><span data-stu-id="3921b-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3921b-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="3921b-124">Notes to callers</span></span>

<span data-ttu-id="3921b-125">Chame **SeekRowApprox** para fornecer os dados de uma implementação de barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="3921b-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="3921b-126">Por exemplo, se o usuário posicionar a caixa de rolagem 2/3 para baixo na barra de rolagem, você poderá modelar essa ação chamando **SeekRowApprox** e passando um valor fracionário equivalente usando o _UlNumerator_ e o _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="3921b-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="3921b-127">A pesquisa do **SeekRowApprox** sempre é absoluta do início da tabela.</span><span class="sxs-lookup"><span data-stu-id="3921b-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="3921b-128">Para mover para o final da tabela, os valores em _ulNumerator_ e _ulDenominator_ devem ser os mesmos.</span><span class="sxs-lookup"><span data-stu-id="3921b-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="3921b-129">Use qualquer esquema de números apropriado.</span><span class="sxs-lookup"><span data-stu-id="3921b-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="3921b-130">Ou seja, para buscar uma posição na metade da tabela, você pode especificar 1/2, 10/20 ou 50/100.</span><span class="sxs-lookup"><span data-stu-id="3921b-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3921b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3921b-131">See also</span></span>



[<span data-ttu-id="3921b-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3921b-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

