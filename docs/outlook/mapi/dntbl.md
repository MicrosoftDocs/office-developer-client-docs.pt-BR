---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398119"
---
# <a name="dntbl"></a><span data-ttu-id="02ad2-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="02ad2-103">DNTBL</span></span>
 
<span data-ttu-id="02ad2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02ad2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02ad2-105">Informações para baixar o conteúdo de uma pasta do servidor durante o [estado de download de tabela](download-table-state.md), como parte de uma sincronização completa do conteúdo de um repositório.</span><span class="sxs-lookup"><span data-stu-id="02ad2-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="02ad2-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="02ad2-106">Quick info</span></span>

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a><span data-ttu-id="02ad2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="02ad2-107">Members</span></span>

<span data-ttu-id="02ad2-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="02ad2-108">_ulFlags_</span></span>
  
> <span data-ttu-id="02ad2-109">[in] Sinalizadores para modificar o comportamento</span><span class="sxs-lookup"><span data-stu-id="02ad2-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="02ad2-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="02ad2-110">DNT_OK</span></span>
    
    - <span data-ttu-id="02ad2-111">[in] Download bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="02ad2-111">[in] Download was successful.</span></span> <span data-ttu-id="02ad2-112">O cliente define isso depois de baixar informações do servidor.</span><span class="sxs-lookup"><span data-stu-id="02ad2-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="02ad2-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="02ad2-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="02ad2-114">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="02ad2-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="02ad2-116">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="02ad2-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="02ad2-118">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="02ad2-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="02ad2-120">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="02ad2-121">_pxicc_</span></span>
  
>  <span data-ttu-id="02ad2-122">[out] Ponteiro para a interface de conteúdo **IExchangeImportContentsChanges** que suporta o download de alterações de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="02ad2-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="02ad2-123">Para saber mais sobre **IExchangeImportContentsChanges**, confira [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="02ad2-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="02ad2-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="02ad2-124">_pxihc_</span></span>
  
>  <span data-ttu-id="02ad2-125">[out] Ponteiro para a interface de hierarquia **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="02ad2-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="02ad2-126">Para saber mais sobre **IExchangeImportHierarchyChanges**, confira [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="02ad2-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="02ad2-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="02ad2-127">_pszName_</span></span>
  
>  <span data-ttu-id="02ad2-128">[out] Nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="02ad2-128">Name of the folder page</span></span> 
    
<span data-ttu-id="02ad2-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="02ad2-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="02ad2-130">[out] Hora da última modificação da pasta.</span><span class="sxs-lookup"><span data-stu-id="02ad2-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="02ad2-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="02ad2-131">_ulRights_</span></span>
  
>  <span data-ttu-id="02ad2-132">[out] Valor da propriedade \*\* [PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx) \*\* da pasta.</span><span class="sxs-lookup"><span data-stu-id="02ad2-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="02ad2-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="02ad2-133">_FEID_</span></span>
  
>  <span data-ttu-id="02ad2-134">[out] ID da entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="02ad2-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="02ad2-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="02ad2-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="02ad2-136">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="02ad2-137">_rgte_</span></span>
  
> <span data-ttu-id="02ad2-138">[out] Alterações para itens normais (ou não ocultos) e associados (ou ocultos).</span><span class="sxs-lookup"><span data-stu-id="02ad2-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="02ad2-139">*rgte[0]* destina-se a itens normais, e *rgte[1]* a itens associados.</span><span class="sxs-lookup"><span data-stu-id="02ad2-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="02ad2-140">O Outlook preenche este membro durante o download ao usar a Sincronização de Alteração Incremental (ICS).</span><span class="sxs-lookup"><span data-stu-id="02ad2-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="02ad2-141">Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="02ad2-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="02ad2-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="02ad2-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="02ad2-143">[in]/[out] Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="02ad2-144">_boReserved_</span></span>
  
>  <span data-ttu-id="02ad2-145">[in]Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="02ad2-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="02ad2-147">[out] Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="02ad2-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="02ad2-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="02ad2-149">[in]Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="02ad2-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="02ad2-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="02ad2-150">See also</span></span>

- [<span data-ttu-id="02ad2-151">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="02ad2-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="02ad2-152">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="02ad2-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="02ad2-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="02ad2-153">DNTBLE</span></span>](dntble.md)

