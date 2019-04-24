---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339183"
---
# <a name="upmov"></a><span data-ttu-id="83bc7-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="83bc7-103">UPMOV</span></span>
 
<span data-ttu-id="83bc7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83bc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83bc7-105">Informações para carregar itens que foram movidos.</span><span class="sxs-lookup"><span data-stu-id="83bc7-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="83bc7-106">Essas informações são usadas durante o [carregamento do status de exclusão](upload-delete-status-state.md) e o [estado da tabela de carregamento](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="83bc7-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="83bc7-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="83bc7-107">Quick info</span></span>

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a><span data-ttu-id="83bc7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="83bc7-108">Members</span></span>

<span data-ttu-id="83bc7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="83bc7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="83bc7-110">no Sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="83bc7-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="83bc7-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="83bc7-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="83bc7-112">no Problema ao abrir a pasta do servidor.</span><span class="sxs-lookup"><span data-stu-id="83bc7-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="83bc7-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="83bc7-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="83bc7-114">no O estado de carregamento foi alterado.</span><span class="sxs-lookup"><span data-stu-id="83bc7-114">[in] The upload state has changed.</span></span> <span data-ttu-id="83bc7-115">Isso é usado pelo cliente para rastrear a alteração no estado do repositório local.</span><span class="sxs-lookup"><span data-stu-id="83bc7-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="83bc7-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="83bc7-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="83bc7-117">no Confirme o estado de carregamento.</span><span class="sxs-lookup"><span data-stu-id="83bc7-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="83bc7-118">_Enquanto_</span><span class="sxs-lookup"><span data-stu-id="83bc7-118">_pReserved_</span></span>
  
>  <span data-ttu-id="83bc7-119">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="83bc7-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="83bc7-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="83bc7-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="83bc7-121">[uto] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="83bc7-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="83bc7-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="83bc7-122">_pszName_</span></span>
  
>  <span data-ttu-id="83bc7-123">bota Nome da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="83bc7-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="83bc7-124">Este membro não dá suporte a UNICODE.</span><span class="sxs-lookup"><span data-stu-id="83bc7-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="83bc7-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="83bc7-125">_feid_</span></span>
  
>  <span data-ttu-id="83bc7-126">bota ID de entrada da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="83bc7-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="83bc7-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="83bc7-127">_pfld_</span></span>
  
>  <span data-ttu-id="83bc7-128">no Ponteiro para a pasta do servidor.</span><span class="sxs-lookup"><span data-stu-id="83bc7-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="83bc7-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="83bc7-129">_pxicc_</span></span>
  
>  <span data-ttu-id="83bc7-130">no Ponteiro para a interface de conteúdo do **IExchangeImportContentsChanges** que oferece suporte ao carregamento de alterações de conteúdo ao usar a sincronização de alteração incremental (ICS).</span><span class="sxs-lookup"><span data-stu-id="83bc7-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="83bc7-131">Para obter mais informações sobre o **IExchangeImportContentsChanges** e o ICS, consulte [critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="83bc7-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="83bc7-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="83bc7-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="83bc7-133">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="83bc7-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="83bc7-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="83bc7-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="83bc7-135">bota Próximo contexto de movimentação.</span><span class="sxs-lookup"><span data-stu-id="83bc7-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="83bc7-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="83bc7-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="83bc7-137">no Número de itens movidos aqui.</span><span class="sxs-lookup"><span data-stu-id="83bc7-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="83bc7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="83bc7-138">See also</span></span>

- [<span data-ttu-id="83bc7-139">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="83bc7-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="83bc7-140">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="83bc7-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="83bc7-141">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="83bc7-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="83bc7-142">FEID</span><span class="sxs-lookup"><span data-stu-id="83bc7-142">FEID</span></span>](feid.md)

