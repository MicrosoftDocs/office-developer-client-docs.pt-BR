---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5e9135a52c15c18b70116aaf52e1ee63af413673
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563846"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="0a2d5-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="0a2d5-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="0a2d5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a2d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a2d5-105">Cria um indicador na posição atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="0a2d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a2d5-106">Parameters</span></span>

 <span data-ttu-id="0a2d5-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="0a2d5-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="0a2d5-108">[out] Ponteiro para o valor retornado indicador de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="0a2d5-109">Este indicador posteriormente pode ser passado em uma chamada ao método [IMAPITable::SeekRow](imapitable-seekrow.md) .</span><span class="sxs-lookup"><span data-stu-id="0a2d5-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0a2d5-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0a2d5-110">Return value</span></span>

<span data-ttu-id="0a2d5-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a2d5-111">S_OK</span></span> 
  
> <span data-ttu-id="0a2d5-112">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0a2d5-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="0a2d5-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="0a2d5-114">A operação solicitada não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a2d5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a2d5-115">Remarks</span></span>

<span data-ttu-id="0a2d5-116">O método **IMAPITable::CreateBookmark** marca uma posição tabela criando um valor chamado um indicador.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="0a2d5-117">Um indicador pode ser usado para retornar à posição identificada pelo indicador.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="0a2d5-118">A posição marcado pelo indicador está associada com o objeto nesse objeto row na tabela.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="0a2d5-119">Indicadores não são suportados em tabelas de anexo e implementações de tabela de anexo do **CreateBookmark** retornam MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0a2d5-120">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="0a2d5-120">Notes to implementers</span></span>

<span data-ttu-id="0a2d5-121">Devido a despesa com a memória de manter as posições de cursor com marcadores, limite o número de indicadores que você pode criar.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="0a2d5-122">Quando você chegar a esse número, retorne MAPI_E_UNABLE_TO_COMPLETE de todas as chamadas subsequentes aos **CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="0a2d5-123">Em alguns casos, um indicador aponta para uma linha que não está mais no modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="0a2d5-124">Se um chamador usar tal um indicador, mova o cursor para a próxima linha visível e parar lá.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="0a2d5-125">Quando o chamador tenta usar um indicador que está apontando para uma linha arquvo porque ele ter sido recolhido, retorne MAPI_W_POSITION_CHANGED depois de mover o indicador.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="0a2d5-126">Você pode reposicionar o indicador para a próxima linha visível no momento ou quando o recolhimento ocorre no método **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="0a2d5-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="0a2d5-127">Se você mover o indicador no momento em que a linha estiver recolhida, você deverá manter um pouco no indicador que indica exatamente quando o indicador foi movido: desde que use sua última ou se nunca tiver sido usado desde sua criação.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0a2d5-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0a2d5-128">Notes to callers</span></span>

 <span data-ttu-id="0a2d5-129">**CreateBookmark** aloca memória para o indicador que ele cria.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="0a2d5-130">Libere os recursos para o indicador chamando o método [IMAPITable::FreeBookmark](imapitable-freebookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="0a2d5-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a2d5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a2d5-131">See also</span></span>



[<span data-ttu-id="0a2d5-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="0a2d5-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="0a2d5-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="0a2d5-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="0a2d5-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0a2d5-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

