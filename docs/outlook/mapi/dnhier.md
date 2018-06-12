---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766460"
---
# <a name="dnhier"></a><span data-ttu-id="62acf-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="62acf-103">DNHIER</span></span>

<span data-ttu-id="62acf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62acf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62acf-105">Informações para download de uma hierarquia do servidor durante o [estado de hierarquia de download](download-hierarchy-state.md), que é parte de uma sincronização de hierarquia completa.</span><span class="sxs-lookup"><span data-stu-id="62acf-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="62acf-106">Este processo de download usa a sincronização de alteração Incremental do Microsoft Exchange (ICS).</span><span class="sxs-lookup"><span data-stu-id="62acf-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="62acf-107">Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="62acf-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="62acf-108">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="62acf-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="62acf-109">Membros</span><span class="sxs-lookup"><span data-stu-id="62acf-109">Members</span></span>

<span data-ttu-id="62acf-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62acf-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="62acf-111">[in] Sinalizadores para determinar o comportamento apropriado durante o download.</span><span class="sxs-lookup"><span data-stu-id="62acf-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="62acf-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="62acf-112">DNH_OK</span></span>
    
   - <span data-ttu-id="62acf-113">[in] Download teve êxito.</span><span class="sxs-lookup"><span data-stu-id="62acf-113">[in] Download was successful.</span></span> <span data-ttu-id="62acf-114">O cliente define esta após fazer o download de informações do servidor.</span><span class="sxs-lookup"><span data-stu-id="62acf-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="62acf-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="62acf-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="62acf-116">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="62acf-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="62acf-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="62acf-117">_pxihc_</span></span>
  
>  <span data-ttu-id="62acf-118">[out] Ponteiro para a interface de hierarquia de **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="62acf-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="62acf-119">Para obter mais informações sobre **IExchangeImportHierarchyChanges**, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="62acf-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="62acf-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="62acf-120">_cEntNew_</span></span>
  
> <span data-ttu-id="62acf-121">[out] Número de pastas adicionados ao armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="62acf-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="62acf-122">Outlook preenche esse valor durante o download quando usando ICS.</span><span class="sxs-lookup"><span data-stu-id="62acf-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="62acf-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="62acf-123">_cEntMod_</span></span>
  
> <span data-ttu-id="62acf-124">[out] Número de pastas a serem modificadas no repositório local.</span><span class="sxs-lookup"><span data-stu-id="62acf-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="62acf-125">Outlook preenche esse valor durante o download quando usando ICS.</span><span class="sxs-lookup"><span data-stu-id="62acf-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="62acf-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="62acf-126">_cEntDel_</span></span>
  
> <span data-ttu-id="62acf-127">[out] Número de pastas a ser excluído no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="62acf-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="62acf-128">Outlook preenche esse valor durante o download quando usando ICS.</span><span class="sxs-lookup"><span data-stu-id="62acf-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62acf-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="62acf-129">See also</span></span>

- [<span data-ttu-id="62acf-130">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="62acf-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="62acf-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="62acf-131">MAPI Constants</span></span>](mapi-constants.md)

