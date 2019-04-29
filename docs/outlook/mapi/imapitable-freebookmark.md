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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409451"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="3c24f-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="3c24f-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="3c24f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c24f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c24f-105">Libera a memória associada a um indicador.</span><span class="sxs-lookup"><span data-stu-id="3c24f-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="3c24f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c24f-106">Parameters</span></span>

 <span data-ttu-id="3c24f-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="3c24f-107">_bkPosition_</span></span>
  
> <span data-ttu-id="3c24f-108">no O indicador a ser liberado, criado chamando o método [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="3c24f-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3c24f-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3c24f-109">Return value</span></span>

<span data-ttu-id="3c24f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c24f-110">S_OK</span></span> 
  
> <span data-ttu-id="3c24f-111">O indicador foi liberado com êxito.</span><span class="sxs-lookup"><span data-stu-id="3c24f-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="3c24f-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="3c24f-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="3c24f-113">O indicador especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="3c24f-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c24f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c24f-114">Remarks</span></span>

<span data-ttu-id="3c24f-115">O método imApitable **:: FreeBookmark** libera um indicador que não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="3c24f-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="3c24f-116">O indicador não é mais válido após esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3c24f-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="3c24f-117">Sempre que uma tabela é liberada da memória, todos os indicadores associados também são lançados.</span><span class="sxs-lookup"><span data-stu-id="3c24f-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3c24f-118">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="3c24f-118">Notes to implementers</span></span>

<span data-ttu-id="3c24f-119">Se o chamador transmitir um dos três indicadores predefinidos no parâmetro _bkPosition_ , ignore a solicitação e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="3c24f-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c24f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c24f-120">See also</span></span>



[<span data-ttu-id="3c24f-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="3c24f-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="3c24f-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c24f-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

