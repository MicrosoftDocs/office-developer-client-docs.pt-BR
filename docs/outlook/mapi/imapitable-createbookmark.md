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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767314"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="7fd3b-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="7fd3b-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="7fd3b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7fd3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7fd3b-105">Cria um indicador na posição atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="7fd3b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fd3b-106">Parameters</span></span>

 <span data-ttu-id="7fd3b-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="7fd3b-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="7fd3b-108">[out] Ponteiro para o valor retornado indicador de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="7fd3b-109">Este indicador posteriormente pode ser passado em uma chamada ao método [IMAPITable::SeekRow](imapitable-seekrow.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd3b-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7fd3b-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7fd3b-110">Return value</span></span>

<span data-ttu-id="7fd3b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="7fd3b-111">S_OK</span></span> 
  
> <span data-ttu-id="7fd3b-112">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7fd3b-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="7fd3b-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="7fd3b-114">A operação solicitada não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7fd3b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fd3b-115">Remarks</span></span>

<span data-ttu-id="7fd3b-116">O método **IMAPITable::CreateBookmark** marca uma posição tabela criando um valor chamado um indicador.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="7fd3b-117">Um indicador pode ser usado para retornar à posição identificada pelo indicador.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="7fd3b-118">A posição marcado pelo indicador está associada com o objeto nesse objeto row na tabela.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="7fd3b-119">Indicadores não são suportados em tabelas de anexo e implementações de tabela de anexo do **CreateBookmark** retornam MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7fd3b-120">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="7fd3b-120">Notes to implementers</span></span>

<span data-ttu-id="7fd3b-121">Devido a despesa com a memória de manter as posições de cursor com marcadores, limite o número de indicadores que você pode criar.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="7fd3b-122">Quando você chegar a esse número, retorne MAPI_E_UNABLE_TO_COMPLETE de todas as chamadas subsequentes aos **CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="7fd3b-123">Em alguns casos, um indicador aponta para uma linha que não está mais no modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="7fd3b-124">Se um chamador usar tal um indicador, mova o cursor para a próxima linha visível e parar lá.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="7fd3b-125">Quando o chamador tenta usar um indicador que está apontando para uma linha arquvo porque ele ter sido recolhido, retorne MAPI_W_POSITION_CHANGED depois de mover o indicador.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="7fd3b-126">Você pode reposicionar o indicador para a próxima linha visível no momento ou quando o recolhimento ocorre no método **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="7fd3b-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="7fd3b-127">Se você mover o indicador no momento em que a linha estiver recolhida, você deverá manter um pouco no indicador que indica exatamente quando o indicador foi movido: desde que use sua última ou se nunca tiver sido usado desde sua criação.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7fd3b-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7fd3b-128">Notes to callers</span></span>

 <span data-ttu-id="7fd3b-129">**CreateBookmark** aloca memória para o indicador que ele cria.</span><span class="sxs-lookup"><span data-stu-id="7fd3b-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="7fd3b-130">Libere os recursos para o indicador chamando o método [IMAPITable::FreeBookmark](imapitable-freebookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd3b-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7fd3b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fd3b-131">See also</span></span>



[<span data-ttu-id="7fd3b-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="7fd3b-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="7fd3b-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="7fd3b-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="7fd3b-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7fd3b-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

