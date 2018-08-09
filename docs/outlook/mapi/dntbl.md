---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766459"
---
# <a name="dntbl"></a><span data-ttu-id="8a6e1-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="8a6e1-103">DNTBL</span></span>
 
<span data-ttu-id="8a6e1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a6e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a6e1-105">Informações para baixar o conteúdo de uma pasta do servidor durante a [baixar o estado da tabela](download-table-state.md), como parte de uma sincronização completa para conteúdo em um repositório.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8a6e1-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8a6e1-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8a6e1-107">Members</span><span class="sxs-lookup"><span data-stu-id="8a6e1-107">Members</span></span>

<span data-ttu-id="8a6e1-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-108">_ulFlags_</span></span>
  
> <span data-ttu-id="8a6e1-109">[in] Sinalizadores para modificar o comportamento</span><span class="sxs-lookup"><span data-stu-id="8a6e1-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="8a6e1-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="8a6e1-110">DNT_OK</span></span>
    
    - <span data-ttu-id="8a6e1-111">[in] Download teve êxito.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-111">[in] Download was successful.</span></span> <span data-ttu-id="8a6e1-112">O cliente define esta após fazer o download de informações do servidor.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="8a6e1-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="8a6e1-114">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="8a6e1-116">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="8a6e1-118">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="8a6e1-120">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-121">_pxicc_</span></span>
  
>  <span data-ttu-id="8a6e1-122">[out] Ponteiro para a interface de conteúdo **IExchangeImportContentsChanges** que suporta o download de alterações de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="8a6e1-123">Para obter mais informações sobre **IExchangeImportContentsChanges**, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a6e1-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="8a6e1-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-124">_pxihc_</span></span>
  
>  <span data-ttu-id="8a6e1-125">[out] Ponteiro para a interface de hierarquia de **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="8a6e1-126">Para obter mais informações sobre **IExchangeImportHierarchyChanges**, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a6e1-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="8a6e1-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-127">_pszName_</span></span>
  
>  <span data-ttu-id="8a6e1-128">[out] Nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="8a6e1-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="8a6e1-130">[out] Hora da última modificação da pasta.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="8a6e1-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-131">_ulRights_</span></span>
  
>  <span data-ttu-id="8a6e1-132">[out] Valor da propriedade **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** da pasta.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-132">[out] Value of the **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="8a6e1-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-133">_feid_</span></span>
  
>  <span data-ttu-id="8a6e1-134">[out] Identificação de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="8a6e1-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="8a6e1-136">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-137">_rgte_</span></span>
  
> <span data-ttu-id="8a6e1-138">[out] Alterações para normal (ou não ocultos) e os itens associados (ou ocultos).</span><span class="sxs-lookup"><span data-stu-id="8a6e1-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="8a6e1-139">*rgte [0]* é para itens normais e *rgte [1]* é para itens associados.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="8a6e1-140">Outlook preenche este membro durante o download ao usar a sincronização de alteração Incremental (ICS).</span><span class="sxs-lookup"><span data-stu-id="8a6e1-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="8a6e1-141">Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a6e1-141">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="8a6e1-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="8a6e1-143">[in] / [out] este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-144">_boReserved_</span></span>
  
>  <span data-ttu-id="8a6e1-145">[in] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="8a6e1-147">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8a6e1-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="8a6e1-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="8a6e1-149">[in] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="8a6e1-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8a6e1-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a6e1-150">See also</span></span>

- [<span data-ttu-id="8a6e1-151">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="8a6e1-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="8a6e1-152">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8a6e1-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="8a6e1-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="8a6e1-153">DNTBLE</span></span>](dntble.md)

