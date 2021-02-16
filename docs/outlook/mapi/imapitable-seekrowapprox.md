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
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="ebbf0-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="ebbf0-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="ebbf0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebbf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebbf0-105">Move o cursor para uma posição fracionada aproximada na tabela.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="ebbf0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebbf0-106">Parameters</span></span>

 <span data-ttu-id="ebbf0-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="ebbf0-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="ebbf0-108">[in] Ponteiro para o numerador da fração que representa a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="ebbf0-109">Se o  _parâmetro ulNumerator_ for zero, o cursor será posicionado no início da tabela, independentemente do valor do denominador.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="ebbf0-110">Se  _ulNumerator for_ igual ao  _parâmetro ulDenominator,_ o cursor será posicionado após a última linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="ebbf0-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="ebbf0-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="ebbf0-112">[in] Ponteiro para o denominador da fração que representa a posição da tabela.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="ebbf0-113">O  _parâmetro ulDenominator_ não pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebbf0-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ebbf0-114">Return value</span></span>

<span data-ttu-id="ebbf0-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebbf0-115">S_OK</span></span> 
  
> <span data-ttu-id="ebbf0-116">A operação de busca foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="ebbf0-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ebbf0-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ebbf0-118">Outra operação está em andamento que impede o início da operação de busca de linha.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="ebbf0-119">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebbf0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebbf0-120">Remarks</span></span>

<span data-ttu-id="ebbf0-121">A posição do cursor em uma tabela após uma chamada para o método **IMAPITable::SeekRowApprox** é heuristicamente a fração e pode não ser exata.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="ebbf0-122">Por exemplo, certos provedores podem implementar uma tabela sobre uma árvore binária, tratando o ponto de metade da tabela como parte superior da árvore por motivos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="ebbf0-123">Se a árvore não estiver equilibrada, o ponto de metade usado pode não estar exatamente no meio da tabela.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ebbf0-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ebbf0-124">Notes to callers</span></span>

<span data-ttu-id="ebbf0-125">Chame **SeekRowApprox para** fornecer os dados para uma implementação de barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="ebbf0-126">Por exemplo, se o usuário posicionar a caixa de rolagem 2/3 abaixo da barra de rolagem, você poderá modelar essa ação chamando **SeekRowApprox** e passando um valor fracionado equivalente usando  _ulNumerator_ e  _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="ebbf0-127">A **pesquisa SeekRowApprox** é sempre absoluta desde o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="ebbf0-128">Para mover para o final da tabela, os valores em  _ulNumerator_ e  _ulDenominator_ devem ser os mesmos.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="ebbf0-129">Use qualquer esquema de números apropriado.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="ebbf0-130">Ou seja, para procurar uma posição no meio da tabela, você pode especificar 1/2, 10/20 ou 50/100.</span><span class="sxs-lookup"><span data-stu-id="ebbf0-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ebbf0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebbf0-131">See also</span></span>



[<span data-ttu-id="ebbf0-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebbf0-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

