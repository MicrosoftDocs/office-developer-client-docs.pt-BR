---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585448"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="c9fa8-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="c9fa8-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="c9fa8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9fa8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9fa8-105">Inicia uma sessão de sincronização e obtém a interface **[IOSTX](iostxiunknown.md)** associada.</span><span class="sxs-lookup"><span data-stu-id="c9fa8-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="c9fa8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9fa8-106">Parameters</span></span>

 <span data-ttu-id="c9fa8-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="c9fa8-107">_ppostx_</span></span>
  
>  <span data-ttu-id="c9fa8-108">[out] Ponteiro para a interface **IOSTX** a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="c9fa8-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c9fa8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9fa8-109">Remarks</span></span>

<span data-ttu-id="c9fa8-110">O chamador deve assegurar que a mesma pasta não está sincronizada ao mesmo tempo em mais de um segmento.</span><span class="sxs-lookup"><span data-stu-id="c9fa8-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9fa8-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9fa8-111">See also</span></span>



[<span data-ttu-id="c9fa8-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="c9fa8-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="c9fa8-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c9fa8-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

