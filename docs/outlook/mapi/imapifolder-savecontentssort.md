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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351202"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="11682-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="11682-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="11682-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11682-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11682-105">Define a ordem de classificação padrão para a tabela de conteúdo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="11682-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="11682-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11682-106">Parameters</span></span>

 <span data-ttu-id="11682-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="11682-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="11682-108">no Um ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém a ordem de classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="11682-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="11682-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11682-109">_ulFlags_</span></span>
  
> <span data-ttu-id="11682-110">no Uma bitmask de sinalizadores que controla como a ordem de classificação padrão é definida.</span><span class="sxs-lookup"><span data-stu-id="11682-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="11682-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="11682-111">The following flag can be set:</span></span>
    
<span data-ttu-id="11682-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="11682-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="11682-113">O conjunto de ordem de classificação padrão se aplica à pasta indicada e a todas as suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="11682-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11682-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="11682-114">Return value</span></span>

<span data-ttu-id="11682-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="11682-115">S_OK</span></span> 
  
> <span data-ttu-id="11682-116">A ordem de classificação foi salva com êxito.</span><span class="sxs-lookup"><span data-stu-id="11682-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="11682-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="11682-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="11682-118">O provedor de repositório de mensagens não oferece suporte para salvar uma ordem de classificação para suas tabelas de conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="11682-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11682-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="11682-119">Remarks</span></span>

<span data-ttu-id="11682-120">O método **IMAPIFolder:: SaveContentsSort** estabelece uma ordem de classificação padrão para a tabela de conteúdo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="11682-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="11682-121">Ou seja, quando um cliente chama o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable da pasta após o código chamar **SaveContentsSort**, as linhas na tabela de conteúdo retornada aparecerão na ordem estabelecida por **SaveContentsSort**.</span><span class="sxs-lookup"><span data-stu-id="11682-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="11682-122">Nem todos os provedores de repositório de mensagens dão suporte a **SaveContentsSort**; é aceitável que os provedores de repositórios de mensagens retornem MAPI_E_NO_SUPPORT do método **SaveContentsSort** .</span><span class="sxs-lookup"><span data-stu-id="11682-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11682-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="11682-123">See also</span></span>



[<span data-ttu-id="11682-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="11682-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="11682-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="11682-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="11682-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="11682-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

