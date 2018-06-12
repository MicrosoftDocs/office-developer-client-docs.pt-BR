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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767688"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="4fc78-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="4fc78-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="4fc78-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fc78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fc78-105">Inicia uma sessão de sincronização e obtém a interface **[IOSTX](iostxiunknown.md)** associada.</span><span class="sxs-lookup"><span data-stu-id="4fc78-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="4fc78-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4fc78-106">Parameters</span></span>

 <span data-ttu-id="4fc78-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="4fc78-107">_ppostx_</span></span>
  
>  <span data-ttu-id="4fc78-108">[out] Ponteiro para a interface **IOSTX** a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="4fc78-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4fc78-109">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4fc78-109">Remarks</span></span>

<span data-ttu-id="4fc78-110">O chamador deve assegurar que a mesma pasta não está sincronizada ao mesmo tempo em mais de um segmento.</span><span class="sxs-lookup"><span data-stu-id="4fc78-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fc78-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fc78-111">See also</span></span>



[<span data-ttu-id="4fc78-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="4fc78-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="4fc78-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4fc78-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

