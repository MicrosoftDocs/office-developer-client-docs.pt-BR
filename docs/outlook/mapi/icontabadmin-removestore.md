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
ms.openlocfilehash: 868f38eaf52d3d0a3787623983a4a587de8fdc3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766896"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="1635b-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="1635b-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="1635b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1635b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1635b-105">Remove o contato endereço CAB (catálogo) especificado pela ID de entrada determinada da hierarquia de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1635b-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="1635b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1635b-106">Parameters</span></span>

 <span data-ttu-id="1635b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1635b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="1635b-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1635b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1635b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1635b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="1635b-110">[in] Um ponteiro para o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="1635b-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

