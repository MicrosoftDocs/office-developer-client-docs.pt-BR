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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e6803c54ddd60c1bcebbe7a139c2edf2e7f4449d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572080"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="52ece-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="52ece-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="52ece-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52ece-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52ece-105">Move o cursor para uma posição fracional aproximada na tabela.</span><span class="sxs-lookup"><span data-stu-id="52ece-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="52ece-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52ece-106">Parameters</span></span>

 <span data-ttu-id="52ece-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="52ece-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="52ece-108">[in] Ponteiro para o numerador da fração que representa a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="52ece-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="52ece-109">Se o parâmetro _ulNumerator_ for zero, o cursor é posicionado no início da tabela independente do valor do denominador.</span><span class="sxs-lookup"><span data-stu-id="52ece-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="52ece-110">Se não for igual ao parâmetro _ulDenominator_ _ulNumerator_ , o cursor é posicionado após a última linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="52ece-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="52ece-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="52ece-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="52ece-112">[in] Ponteiro para o denominador da fração que representa a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="52ece-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="52ece-113">O parâmetro _ulDenominator_ não pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="52ece-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="52ece-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52ece-114">Return value</span></span>

<span data-ttu-id="52ece-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="52ece-115">S_OK</span></span> 
  
> <span data-ttu-id="52ece-116">A operação de busca foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="52ece-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="52ece-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="52ece-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="52ece-118">Outra operação está em andamento que impede que a linha que buscam início da operação.</span><span class="sxs-lookup"><span data-stu-id="52ece-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="52ece-119">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="52ece-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52ece-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="52ece-120">Remarks</span></span>

<span data-ttu-id="52ece-121">A posição do cursor em uma tabela depois de uma chamada para o método **IMAPITable:: SeekRowApprox** heuristicamente é a fração e pode não ser exata.</span><span class="sxs-lookup"><span data-stu-id="52ece-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="52ece-122">Por exemplo, certos provedores podem implementar uma tabela na parte superior de uma árvore binária, tratando ponto intermediário da tabela como parte superior da árvore por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="52ece-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="52ece-123">Se a árvore não é balanceada, em seguida, o ponto intermediário usado pode não ser exatamente na metade a tabela.</span><span class="sxs-lookup"><span data-stu-id="52ece-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="52ece-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="52ece-124">Notes to callers</span></span>

<span data-ttu-id="52ece-125">Chame **SeekRowApprox** para fornecer os dados para uma implementação da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="52ece-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="52ece-126">Por exemplo, se o usuário posiciona o 2/3 de caixa de rolagem para baixo da barra de rolagem, você pode modelar essa ação chamando **SeekRowApprox** e passando um valor fracionário equivalente usando _ulNumerator_ e _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="52ece-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="52ece-127">A pesquisa **SeekRowApprox** é sempre absoluta desde o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="52ece-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="52ece-128">Para mover para o final da tabela, os valores em _ulNumerator_ e _ulDenominator_ devem ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="52ece-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="52ece-129">Use o esquema de qualquer número é apropriado.</span><span class="sxs-lookup"><span data-stu-id="52ece-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="52ece-130">Ou seja, para buscar para uma posição na metade a tabela, você pode especificar 1/2, 10/20 ou 50/100.</span><span class="sxs-lookup"><span data-stu-id="52ece-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52ece-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="52ece-131">See also</span></span>



[<span data-ttu-id="52ece-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52ece-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

