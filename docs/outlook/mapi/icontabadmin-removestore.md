---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2ec8a28dc52e2aa1f1fa63410b6bd6c13fb5bd57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583982"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="5f96e-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="5f96e-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="5f96e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f96e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f96e-105">Remove o contato endereço CAB (catálogo) especificado pela ID de entrada determinada da hierarquia de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5f96e-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="5f96e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f96e-106">Parameters</span></span>

 <span data-ttu-id="5f96e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5f96e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="5f96e-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5f96e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5f96e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5f96e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="5f96e-110">[in] Um ponteiro para o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="5f96e-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

