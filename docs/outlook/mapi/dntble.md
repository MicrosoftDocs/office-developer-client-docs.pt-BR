---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337111"
---
# <a name="dntble"></a><span data-ttu-id="b81b4-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="b81b4-103">DNTBLE</span></span>

  
  
<span data-ttu-id="b81b4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b81b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b81b4-105">Informações para baixar o conteúdo de uma pasta do servidor durante o [estado de download de tabela](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="b81b4-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="b81b4-106">Este processo de download usa a sincronização de Sincronização de Alteração Incremental (ICS) do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="b81b4-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b81b4-107">Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b81b4-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b81b4-108">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b81b4-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="b81b4-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b81b4-109">Members</span></span>

 <span data-ttu-id="b81b4-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="b81b4-110">_cEntNew_</span></span>
  
> <span data-ttu-id="b81b4-111">[out] Número de itens adicionados ao repositório local.</span><span class="sxs-lookup"><span data-stu-id="b81b4-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="b81b4-112">O Outlook preenche esse valor durante o download ao usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b81b4-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b81b4-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="b81b4-113">_cEntMod_</span></span>
  
> <span data-ttu-id="b81b4-114">[out] Número de itens modificados no repositório local.</span><span class="sxs-lookup"><span data-stu-id="b81b4-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="b81b4-115">O Outlook preenche esse valor durante o download ao usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b81b4-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b81b4-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="b81b4-116">_cEntRead_</span></span>
  
> <span data-ttu-id="b81b4-117">[out] Número de itens lidos ou marcados como não lidos no repositório local.</span><span class="sxs-lookup"><span data-stu-id="b81b4-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="b81b4-118">O Outlook preenche esse valor durante o download ao usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b81b4-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b81b4-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="b81b4-119">_cEntDel_</span></span>
  
> <span data-ttu-id="b81b4-120">[out] Número de itens excluídos do repositório local.</span><span class="sxs-lookup"><span data-stu-id="b81b4-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="b81b4-121">O Outlook preenche esse valor durante o download ao usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b81b4-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b81b4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b81b4-122">See also</span></span>



[<span data-ttu-id="b81b4-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="b81b4-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b81b4-124">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="b81b4-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b81b4-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="b81b4-125">DNTBL</span></span>](dntbl.md)

