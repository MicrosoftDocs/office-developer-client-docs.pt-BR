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
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418131"
---
# <a name="bookmark"></a><span data-ttu-id="50392-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="50392-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="50392-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50392-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50392-105">Define dados de indicadores para lembrar uma posição em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="50392-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50392-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="50392-106">Header file:</span></span>  <br/> |<span data-ttu-id="50392-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50392-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="50392-108">Métodos relacionados:</span><span class="sxs-lookup"><span data-stu-id="50392-108">Related methods:</span></span>  <br/> |<span data-ttu-id="50392-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="50392-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="50392-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="50392-110">Remarks</span></span>

<span data-ttu-id="50392-111">O MAPI define três indicadores, listados da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="50392-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="50392-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="50392-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="50392-113">Lembra a posição inicial da tabela.</span><span class="sxs-lookup"><span data-stu-id="50392-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="50392-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="50392-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="50392-115">Lembra a posição atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="50392-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="50392-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="50392-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="50392-117">Lembra a posição final da tabela.</span><span class="sxs-lookup"><span data-stu-id="50392-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="50392-118">Os clientes podem criar outros indicadores para lembrar de outras posições de tabela.</span><span class="sxs-lookup"><span data-stu-id="50392-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="50392-119">Os indicadores são válidos somente quando a tabela está aberta.</span><span class="sxs-lookup"><span data-stu-id="50392-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="50392-120">Os clientes devem liberar todos os indicadores criados antes de fechar a tabela associada.</span><span class="sxs-lookup"><span data-stu-id="50392-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50392-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="50392-121">See also</span></span>



[<span data-ttu-id="50392-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="50392-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="50392-123">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="50392-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="50392-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="50392-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="50392-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="50392-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="50392-126">Tipos de dados MAPI</span><span class="sxs-lookup"><span data-stu-id="50392-126">MAPI Data Types</span></span>](mapi-data-types.md)

