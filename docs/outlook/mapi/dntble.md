---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 51a79075dac62a051f5a28dbcb70e7d6ff200e65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766487"
---
# <a name="dntble"></a><span data-ttu-id="79382-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="79382-103">DNTBLE</span></span>

  
  
<span data-ttu-id="79382-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79382-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79382-105">Informações para baixar o conteúdo de uma pasta do servidor durante a [baixar o estado da tabela](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="79382-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="79382-106">Este processo de download usa a sincronização de alteração Incremental do Microsoft Exchange (ICS).</span><span class="sxs-lookup"><span data-stu-id="79382-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="79382-107">Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/pt-br/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="79382-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/pt-br/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79382-108">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="79382-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="79382-109">Membros</span><span class="sxs-lookup"><span data-stu-id="79382-109">Members</span></span>

 <span data-ttu-id="79382-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="79382-110">_cEntNew_</span></span>
  
> <span data-ttu-id="79382-111">[out] Número de itens adicionados ao armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="79382-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="79382-112">Outlook preenche esse valor durante o download quando usando ICS.</span><span class="sxs-lookup"><span data-stu-id="79382-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="79382-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="79382-113">_cEntMod_</span></span>
  
> <span data-ttu-id="79382-114">[out] Número de itens modificados no mesmo armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="79382-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="79382-115">Outlook preenche esse valor durante o download quando usando ICS.</span><span class="sxs-lookup"><span data-stu-id="79382-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="79382-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="79382-116">_cEntRead_</span></span>
  
> <span data-ttu-id="79382-117">[out] Número de itens de leitura ou marcado como não lido no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="79382-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="79382-118">Outlook preenche esse valor durante o download quando usando ICS.</span><span class="sxs-lookup"><span data-stu-id="79382-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="79382-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="79382-119">_cEntDel_</span></span>
  
> <span data-ttu-id="79382-120">[out] Número de itens excluídos no repositório local.</span><span class="sxs-lookup"><span data-stu-id="79382-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="79382-121">Outlook preenche esse valor durante o download quando usando ICS.</span><span class="sxs-lookup"><span data-stu-id="79382-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79382-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="79382-122">See also</span></span>



[<span data-ttu-id="79382-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="79382-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="79382-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="79382-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="79382-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="79382-125">DNTBL</span></span>](dntbl.md)

