---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766984"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="13370-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="13370-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="13370-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13370-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13370-105">Define a ordem de classificação padrão para a tabela de conteúdo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="13370-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="13370-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13370-106">Parameters</span></span>

 <span data-ttu-id="13370-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="13370-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="13370-108">[in] Um ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém a ordem de classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="13370-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="13370-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13370-109">_ulFlags_</span></span>
  
> <span data-ttu-id="13370-110">[in] Uma bitmask dos sinalizadores que controla como a ordem de classificação padrão é definida.</span><span class="sxs-lookup"><span data-stu-id="13370-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="13370-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="13370-111">The following flag can be set:</span></span>
    
<span data-ttu-id="13370-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="13370-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="13370-113">O conjunto de ordem de classificação padrão se aplica à pasta indicada e todas as suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="13370-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13370-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="13370-114">Return value</span></span>

<span data-ttu-id="13370-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="13370-115">S_OK</span></span> 
  
> <span data-ttu-id="13370-116">A ordem de classificação for salva com êxito.</span><span class="sxs-lookup"><span data-stu-id="13370-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="13370-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="13370-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="13370-118">O provedor de armazenamento de mensagem não suporta a salvando uma ordem de classificação para suas tabelas de conteúdo de pasta.</span><span class="sxs-lookup"><span data-stu-id="13370-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13370-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="13370-119">Remarks</span></span>

<span data-ttu-id="13370-120">O método **IMAPIFolder::SaveContentsSort** estabelece uma ordem de classificação padrão para a tabela de conteúdo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="13370-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="13370-121">Ou seja, quando um cliente chama o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta após o código chama **SaveContentsSort**, as linhas da tabela de conteúdo retornado aparecerá na ordem estabelecida pelo **SaveContentsSort**.</span><span class="sxs-lookup"><span data-stu-id="13370-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="13370-122">Nem todos os provedores de armazenamento de mensagem suportam **SaveContentsSort**; é aceitável para provedores de armazenamento de mensagem retornar MAPI_E_NO_SUPPORT do método **SaveContentsSort** .</span><span class="sxs-lookup"><span data-stu-id="13370-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13370-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="13370-123">See also</span></span>



[<span data-ttu-id="13370-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="13370-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="13370-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="13370-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="13370-126">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="13370-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

