---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767330"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="4a773-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="4a773-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="4a773-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a773-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a773-105">Libera a memória associada a um indicador.</span><span class="sxs-lookup"><span data-stu-id="4a773-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="4a773-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4a773-106">Parameters</span></span>

 <span data-ttu-id="4a773-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="4a773-107">_bkPosition_</span></span>
  
> <span data-ttu-id="4a773-108">[in] O indicador para ser liberada, criados chamando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="4a773-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4a773-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4a773-109">Return value</span></span>

<span data-ttu-id="4a773-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a773-110">S_OK</span></span> 
  
> <span data-ttu-id="4a773-111">O indicador foi liberado com êxito.</span><span class="sxs-lookup"><span data-stu-id="4a773-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="4a773-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="4a773-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="4a773-113">O indicador especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="4a773-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a773-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4a773-114">Remarks</span></span>

<span data-ttu-id="4a773-115">O método **IMAPITable::FreeBookmark** libera um indicador que não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="4a773-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="4a773-116">O indicador não é mais válido após essa chamada.</span><span class="sxs-lookup"><span data-stu-id="4a773-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="4a773-117">Sempre que uma tabela é liberada da memória, todos seus indicadores associadas também sejam liberados.</span><span class="sxs-lookup"><span data-stu-id="4a773-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4a773-118">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="4a773-118">Notes to implementers</span></span>

<span data-ttu-id="4a773-119">Se o chamador passa uma dos três indicadores predefinidos no parâmetro _bkPosition_ , ignore a solicitação e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="4a773-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a773-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a773-120">See also</span></span>



[<span data-ttu-id="4a773-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="4a773-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="4a773-122">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a773-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

