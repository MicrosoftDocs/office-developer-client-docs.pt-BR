---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389082"
---
# <a name="dnhier"></a><span data-ttu-id="2b675-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="2b675-103">DNHIER</span></span>

<span data-ttu-id="2b675-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b675-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b675-105">Informações para baixar uma hierarquia do servidor durante o [estado hierarquia de download](download-hierarchy-state.md), que é parte de uma sincronização de hierarquia completa.</span><span class="sxs-lookup"><span data-stu-id="2b675-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="2b675-106">Este processo de download usa a sincronização de Sincronização de Alteração Incremental (ICS) do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="2b675-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="2b675-107">Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b675-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2b675-108">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2b675-108">Quick info</span></span>

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="2b675-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2b675-109">Members</span></span>

<span data-ttu-id="2b675-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2b675-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="2b675-111">[in] Sinaliza para determinar o comportamento apropriado durante o download.</span><span class="sxs-lookup"><span data-stu-id="2b675-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="2b675-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="2b675-112">DNH_OK</span></span>
    
   - <span data-ttu-id="2b675-113">[in] Download bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2b675-113">[in] Download was successful.</span></span> <span data-ttu-id="2b675-114">O cliente define isso depois de baixar informações do servidor.</span><span class="sxs-lookup"><span data-stu-id="2b675-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="2b675-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="2b675-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="2b675-116">[uto] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="2b675-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="2b675-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="2b675-117">_pxihc_</span></span>
  
>  <span data-ttu-id="2b675-118">[uto] Ponteiro para a hierarquia de hierarquia **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="2b675-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="2b675-119">Para saber mais sobre **IExchangeImportHierarchyChanges**, confira [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b675-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="2b675-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="2b675-120">_cEntNew_</span></span>
  
> <span data-ttu-id="2b675-121">[out] Número de pastas adicionadas ao repositório local.</span><span class="sxs-lookup"><span data-stu-id="2b675-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="2b675-122">O Outlook preenche esse valor durante o download ao usar a ICS.</span><span class="sxs-lookup"><span data-stu-id="2b675-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="2b675-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="2b675-123">_cEntMod_</span></span>
  
> <span data-ttu-id="2b675-124">[out] Número de pastas a serem modificadas no repositório local.</span><span class="sxs-lookup"><span data-stu-id="2b675-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="2b675-125">O Outlook preenche esse valor durante o download ao usar a ICS.</span><span class="sxs-lookup"><span data-stu-id="2b675-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="2b675-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="2b675-126">_cEntDel_</span></span>
  
> <span data-ttu-id="2b675-127">[out] Número de pastas a serem excluídas do repositório local.</span><span class="sxs-lookup"><span data-stu-id="2b675-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="2b675-128">O Outlook preenche esse valor durante o download ao usar a ICS.</span><span class="sxs-lookup"><span data-stu-id="2b675-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b675-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b675-129">See also</span></span>

- [<span data-ttu-id="2b675-130">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="2b675-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="2b675-131">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="2b675-131">MAPI Constants</span></span>](mapi-constants.md)

