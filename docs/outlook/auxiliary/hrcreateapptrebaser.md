---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa um objeto IOlkApptRebaser para uso na alteração da base compromissos no calendário do Outlook.
ms.openlocfilehash: fec0407c3f129290d03f9b26b0b3f072a229b003
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765822"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="a2a72-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="a2a72-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="a2a72-104">Inicializa um objeto [IOlkApptRebaser](iolkapptrebaser.md) para uso na alteração da base compromissos no calendário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="a2a72-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a2a72-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a2a72-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2a72-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a2a72-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2a72-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="a2a72-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="a2a72-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a2a72-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a2a72-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="a2a72-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="a2a72-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a2a72-110">Called by:</span></span>  <br/> |<span data-ttu-id="a2a72-111">Aplicativos de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="a2a72-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="a2a72-112">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a2a72-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="a2a72-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="a2a72-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="a2a72-114">Ponto de entrada DLL:</span><span class="sxs-lookup"><span data-stu-id="a2a72-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="a2a72-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="a2a72-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a><span data-ttu-id="a2a72-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2a72-116">Parameters</span></span>

<span data-ttu-id="a2a72-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2a72-117">_ulFlags_</span></span>
  
> <span data-ttu-id="a2a72-118">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-118">[in] Required.</span></span> <span data-ttu-id="a2a72-119">Uma bitmask dos sinalizadores usados para controlar como a alteração da base é executada.</span><span class="sxs-lookup"><span data-stu-id="a2a72-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="a2a72-120">Sinalizadores a seguir podem ser definidos e definidos no tzmovelib.h:</span><span class="sxs-lookup"><span data-stu-id="a2a72-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="a2a72-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — os itens de compromisso em que o usuário é o organizador da reunião são base alterados.</span><span class="sxs-lookup"><span data-stu-id="a2a72-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="a2a72-122">Observe que, por padrão, isso faz com que o Outlook enviar atualizações de reunião para todos os participantes de qualquer reunião a base que está sendo alterada.</span><span class="sxs-lookup"><span data-stu-id="a2a72-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="a2a72-123">Você pode combinar esse sinalizador com **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** para alterar como as atualizações de reunião são manipuladas.</span><span class="sxs-lookup"><span data-stu-id="a2a72-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="a2a72-124">**REBASE_FLAG_UPDATE_UNMARKED** — atualizar itens de compromisso que não foram marcados com um fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="a2a72-125">Se esse sinalizador for especificado, o valor de *pTZMissing* é usado como o fuso horário que um item é criado em todos os itens que não têm dados de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="a2a72-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** — atualizar apenas itens de compromisso recorrente.</span><span class="sxs-lookup"><span data-stu-id="a2a72-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="a2a72-127">**REBASE_FLAG_NO_UI** — não mostrar nenhuma interface de usuário (UI), incluindo caixas de diálogo de logon geralmente exibidas ao abrir um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a2a72-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="a2a72-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — não alterar a base de itens de compromisso que ocorrem no passado.</span><span class="sxs-lookup"><span data-stu-id="a2a72-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="a2a72-129">**REBASE_FLAG_FORCE_REBASE** — não verificar o organizador para a alteração da Base de decisões, mas alterar a base de itens de compromisso em que o usuário é um participante.</span><span class="sxs-lookup"><span data-stu-id="a2a72-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="a2a72-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** — envia as atualizações somente se o usuário é o organizador e o destinatário não está conectado a um servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="a2a72-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="a2a72-131">**REBASE_FLAG_FORCE_NO_UPDATES** — nunca enviar atualizações.</span><span class="sxs-lookup"><span data-stu-id="a2a72-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="a2a72-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — alterar a base apenas os itens de compromisso de ocorrência única criados antes da aplicação do patch.</span><span class="sxs-lookup"><span data-stu-id="a2a72-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="a2a72-133">**REBASE_FLAG_REPORTING_MODE** — fazer na verdade não alterar, a base do relatório apenas itens de compromisso que seria ser alterado.</span><span class="sxs-lookup"><span data-stu-id="a2a72-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="a2a72-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** — enviar atualizações de reunião para os recursos.</span><span class="sxs-lookup"><span data-stu-id="a2a72-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="a2a72-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="a2a72-135">_pSession_</span></span>
  
> <span data-ttu-id="a2a72-136">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-136">[in] Required.</span></span> <span data-ttu-id="a2a72-137">Um ponteiro para uma interface de sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="a2a72-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="a2a72-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="a2a72-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="a2a72-139">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-139">[in] Required.</span></span> <span data-ttu-id="a2a72-140">Um ponteiro para um armazenamento de mensagens que contêm os itens de compromisso de ser alterada.</span><span class="sxs-lookup"><span data-stu-id="a2a72-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="a2a72-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="a2a72-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="a2a72-142">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-142">[in] Required.</span></span> <span data-ttu-id="a2a72-143">Um ponteiro para uma pasta de calendário que contém itens de compromisso de ser alterada.</span><span class="sxs-lookup"><span data-stu-id="a2a72-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="a2a72-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="a2a72-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="a2a72-145">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2a72-145">[in] Optional.</span></span> <span data-ttu-id="a2a72-146">Um ponteiro para uma cadeia de caracteres que contém o prefixo a serem anexados em solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="a2a72-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="a2a72-147">Pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a2a72-147">May be NULL.</span></span>
    
<span data-ttu-id="a2a72-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="a2a72-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="a2a72-149">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2a72-149">[in] Optional.</span></span> <span data-ttu-id="a2a72-150">Data da instalação do patch de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-150">The time zone patch install date.</span></span> <span data-ttu-id="a2a72-151">Usado somente se o sinalizador **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** está definido.</span><span class="sxs-lookup"><span data-stu-id="a2a72-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="a2a72-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="a2a72-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="a2a72-153">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2a72-153">[in] Optional.</span></span> <span data-ttu-id="a2a72-154">A profundidade de expansão quando Expandindo listas de distribuição para excluir os destinatários conectados ao servidor do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a2a72-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="a2a72-155">Usado somente se o sinalizador **REBASE_FLAG_FORCE_NO_EX_UPDATES** está definido.</span><span class="sxs-lookup"><span data-stu-id="a2a72-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="a2a72-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="a2a72-156">_pTZTo_</span></span>
  
> <span data-ttu-id="a2a72-157">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-157">[in] Required.</span></span> <span data-ttu-id="a2a72-158">Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário de ser alterada para.</span><span class="sxs-lookup"><span data-stu-id="a2a72-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="a2a72-159">**TZDEFINITION** é definido em tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="a2a72-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="a2a72-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="a2a72-160">pTZMissing</span></span>
  
> <span data-ttu-id="a2a72-161">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a2a72-161">[in] Required.</span></span> <span data-ttu-id="a2a72-162">Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário para ser assumido se as informações de fuso horário não estiver marcadas em um item.</span><span class="sxs-lookup"><span data-stu-id="a2a72-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="a2a72-163">Não deve ser nulo, mas somente usado se o sinalizador **REBASE_FLAG_UPDATE_UNMARKED** está definido.</span><span class="sxs-lookup"><span data-stu-id="a2a72-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="a2a72-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="a2a72-164">_ppError_</span></span>
  
> <span data-ttu-id="a2a72-165">[out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** contendo informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="a2a72-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="a2a72-166">Pode ser NULL se não há informações de erro estendidas for desejadas.</span><span class="sxs-lookup"><span data-stu-id="a2a72-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="a2a72-167">Livre com [MAPIFreeBuffer](http://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a2a72-167">Free with [MAPIFreeBuffer](http://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="a2a72-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="a2a72-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="a2a72-169">[out] Um ponteiro para um ponteiro para a interface **IOlkApptRebaser** retornado.</span><span class="sxs-lookup"><span data-stu-id="a2a72-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a2a72-170">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a2a72-170">Return values</span></span>

<span data-ttu-id="a2a72-171">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a2a72-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2a72-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2a72-172">Remarks</span></span>

<span data-ttu-id="a2a72-173">Ao usar o [GetProcAddress](http://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para procurar o endereço desta função no tzmovelib.dll, especifique **HrCreateApptRebaser@44** como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="a2a72-173">When using [GetProcAddress](http://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="a2a72-174">Nem todos os sinalizadores são válidos em combinação com umas às outras.</span><span class="sxs-lookup"><span data-stu-id="a2a72-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="a2a72-175">Para obter mais informações sobre as várias opções, consulte a seção "Glossário de opções de linha de comando da ferramenta de atualização de dados de fuso horário do Outlook" em [KB 931667: alterações de fuso horário do endereço, usando a ferramenta de atualização de dados de fuso horário para Microsoft Office Outlook como](http://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="a2a72-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](http://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2a72-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2a72-176">See also</span></span>

- [<span data-ttu-id="a2a72-177">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="a2a72-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

