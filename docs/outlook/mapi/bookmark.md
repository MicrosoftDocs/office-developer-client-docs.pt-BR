---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594478"
---
# <a name="bookmark"></a><span data-ttu-id="efd37-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="efd37-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="efd37-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efd37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efd37-105">Define os dados de indicadores para memorizar uma posição em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="efd37-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="efd37-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="efd37-106">Header file:</span></span>  <br/> |<span data-ttu-id="efd37-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efd37-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="efd37-108">Métodos relacionados:</span><span class="sxs-lookup"><span data-stu-id="efd37-108">Related methods:</span></span>  <br/> |<span data-ttu-id="efd37-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="efd37-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="efd37-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="efd37-110">Remarks</span></span>

<span data-ttu-id="efd37-111">MAPI define três indicadores, listadas a seguir:</span><span class="sxs-lookup"><span data-stu-id="efd37-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="efd37-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="efd37-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="efd37-113">Lembra-se a posição inicial da tabela.</span><span class="sxs-lookup"><span data-stu-id="efd37-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="efd37-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="efd37-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="efd37-115">Lembra-se a posição atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="efd37-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="efd37-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="efd37-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="efd37-117">Lembra-se a posição final da tabela.</span><span class="sxs-lookup"><span data-stu-id="efd37-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="efd37-118">Os clientes podem criar outros indicadores lembrando outras posições de tabela.</span><span class="sxs-lookup"><span data-stu-id="efd37-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="efd37-119">Indicadores são válidas somente quando a tabela é aberta.</span><span class="sxs-lookup"><span data-stu-id="efd37-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="efd37-120">Clientes devem liberar todos os indicadores que eles criaram antes de fechar a tabela associada.</span><span class="sxs-lookup"><span data-stu-id="efd37-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efd37-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="efd37-121">See also</span></span>



[<span data-ttu-id="efd37-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="efd37-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="efd37-123">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="efd37-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="efd37-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="efd37-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="efd37-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="efd37-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="efd37-126">Tipos de dados MAPI</span><span class="sxs-lookup"><span data-stu-id="efd37-126">MAPI Data Types</span></span>](mapi-data-types.md)

