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
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315082"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="57ec0-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="57ec0-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="57ec0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57ec0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57ec0-105">Inicia uma sessão de sincronização e obtém a interface **[IOSTX](iostxiunknown.md)** associada.</span><span class="sxs-lookup"><span data-stu-id="57ec0-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="57ec0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57ec0-106">Parameters</span></span>

 <span data-ttu-id="57ec0-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="57ec0-107">_ppostx_</span></span>
  
>  <span data-ttu-id="57ec0-108">bota Ponteiro para a interface **IOSTX** a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="57ec0-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="57ec0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="57ec0-109">Remarks</span></span>

<span data-ttu-id="57ec0-110">O chamador deve garantir que a mesma pasta não seja sincronizada ao mesmo tempo em mais de um thread.</span><span class="sxs-lookup"><span data-stu-id="57ec0-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57ec0-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="57ec0-111">See also</span></span>



[<span data-ttu-id="57ec0-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="57ec0-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="57ec0-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="57ec0-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

