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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339267"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="dbacd-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="dbacd-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="dbacd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbacd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbacd-105">Remove o catálogo de endereços de contatos (CAB) especificado pela ID de entrada fornecida na hierarquia do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="dbacd-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="dbacd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbacd-106">Parameters</span></span>

 <span data-ttu-id="dbacd-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dbacd-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="dbacd-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="dbacd-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dbacd-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dbacd-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="dbacd-110">no Um ponteiro para o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="dbacd-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

