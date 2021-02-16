---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa um objeto IOlkApptRebaser para uso em alteração da base de compromissos no calendário do Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317609"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="a421d-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="a421d-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="a421d-104">Inicializa um objeto [IOlkApptRebaser](iolkapptrebaser.md) para uso em alteração programática de compromissos em calendários do Outlook.</span><span class="sxs-lookup"><span data-stu-id="a421d-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a421d-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a421d-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a421d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a421d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a421d-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="a421d-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="a421d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a421d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a421d-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="a421d-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="a421d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a421d-110">Called by:</span></span>  <br/> |<span data-ttu-id="a421d-111">Aplicativos clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="a421d-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="a421d-112">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a421d-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="a421d-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="a421d-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="a421d-114">Ponto de entrada DLL:</span><span class="sxs-lookup"><span data-stu-id="a421d-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="a421d-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="a421d-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a421d-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a421d-116">Parameters</span></span>

<span data-ttu-id="a421d-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a421d-117">_ulFlags_</span></span>
  
> <span data-ttu-id="a421d-118">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a421d-118">[in] Required.</span></span> <span data-ttu-id="a421d-119">Uma máscara de bits de sinalizadores usados para controlar como a alteração da base será executada.</span><span class="sxs-lookup"><span data-stu-id="a421d-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="a421d-120">Os procedimentos sinalizadores podem ser definidos e definidos tzmovelib.h:</span><span class="sxs-lookup"><span data-stu-id="a421d-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="a421d-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS**, base de itens de compromisso em que o usuário é o organizador da reunião alterada.</span><span class="sxs-lookup"><span data-stu-id="a421d-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="a421d-122">Observe que, por padrão, isso faz com que o Outlook envie atualizações da reunião aos participantes qualquer reunião que na base que está sendo alterada.</span><span class="sxs-lookup"><span data-stu-id="a421d-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="a421d-123">Você pode combinar esse sinalizador com um **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** para alterar como são tratadas as atualizações da reunião.</span><span class="sxs-lookup"><span data-stu-id="a421d-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="a421d-124">**REBASE_FLAG_UPDATE_UNMARKED**, atualizar itens de compromisso que não foram marcados com um fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a421d-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="a421d-125">Se esse sinalizador for especificado, o valor *pTZMissing* será usado como o fuso horário criado em um item para todos os itens que não têm dados fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a421d-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="a421d-126">**REBASE_FLAG_UPDATE_ONLYRECURRING**, atualiza os únicos itens de compromisso recorrentes.</span><span class="sxs-lookup"><span data-stu-id="a421d-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="a421d-127">**REBASE_FLAG_NO_UI**, não mostram uma interface do usuário (UI), incluindo caixas de diálogo de logon geralmente exibidas ao abrir um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a421d-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="a421d-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — não altera a base de itens de compromisso que ocorrem no passado.</span><span class="sxs-lookup"><span data-stu-id="a421d-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="a421d-129">**REBASE_FLAG_FORCE_REBASE**, não marca o organizador para a alteração da Base de decisões, mas altera a base de itens de compromisso em que o usuário é participante.</span><span class="sxs-lookup"><span data-stu-id="a421d-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="a421d-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES**, envia atualizações somente se o usuário for o organizador e o destinatário e não estiver conectado a um Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a421d-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="a421d-131">**REBASE_FLAG_FORCE_NO_UPDATES**, nunca enviar atualizações.</span><span class="sxs-lookup"><span data-stu-id="a421d-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="a421d-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH**, alterar a base apenas itens de compromisso criados antes da aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="a421d-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="a421d-133">**REBASE_FLAG_REPORTING_MODE**, não altera a  base, apenas faz o relatório de itens de compromisso que teriam a base alterada.</span><span class="sxs-lookup"><span data-stu-id="a421d-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="a421d-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES**, envia atualizações da reunião para os recursos.</span><span class="sxs-lookup"><span data-stu-id="a421d-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="a421d-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="a421d-135">_pSession_</span></span>
  
> <span data-ttu-id="a421d-136">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a421d-136">[in] Required.</span></span> <span data-ttu-id="a421d-137">Ponteiro para uma interface de sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="a421d-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="a421d-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="a421d-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="a421d-139">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a421d-139">[in] Required.</span></span> <span data-ttu-id="a421d-140">Ponteiro para um repositório de mensagem que contém itens de compromisso para serem alterados.</span><span class="sxs-lookup"><span data-stu-id="a421d-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="a421d-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="a421d-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="a421d-142">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a421d-142">[in] Required.</span></span> <span data-ttu-id="a421d-143">Ponteiro para uma pasta de calendário que contém itens compromisso de para serem alterados.</span><span class="sxs-lookup"><span data-stu-id="a421d-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="a421d-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="a421d-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="a421d-145">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a421d-145">[in] Optional.</span></span> <span data-ttu-id="a421d-146">Ponteiro para conter o prefixo anexado em solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="a421d-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="a421d-147">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="a421d-147">May be NULL.</span></span>
    
<span data-ttu-id="a421d-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="a421d-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="a421d-149">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a421d-149">[in] Optional.</span></span> <span data-ttu-id="a421d-150">Data da instalação o caminho do patch fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a421d-150">The time zone patch install date.</span></span> <span data-ttu-id="a421d-151">Usados somente se a **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** sinalizador estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a421d-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="a421d-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="a421d-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="a421d-153">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a421d-153">[in] Optional.</span></span> <span data-ttu-id="a421d-154">A profundidade de expansão quando se está expandindo a listas de distribuição para excluir os destinatários conectados ao servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="a421d-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="a421d-155">Usada apenas se o sinalizador **REBASE_FLAG_FORCE_NO_EX_UPDATES** sinalizador estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a421d-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="a421d-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="a421d-156">_pTZTo_</span></span>
  
> <span data-ttu-id="a421d-157">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a421d-157">[in] Required.</span></span> <span data-ttu-id="a421d-158">Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="a421d-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="a421d-159">**TZDEFINITION** definido no tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="a421d-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="a421d-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="a421d-160">pTZMissing</span></span>
  
> <span data-ttu-id="a421d-161">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a421d-161">[in] Required.</span></span> <span data-ttu-id="a421d-162">Um ponteiro para uma estrutura **TZDEFINITION** descrevendo o fuso horário a ser considerado se as informações sobre fuso horário não estiverem marcadas em um item.</span><span class="sxs-lookup"><span data-stu-id="a421d-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="a421d-163">Não pode ser nulo, mas somente será usado se o sinalizador **REBASE_FLAG_UPDATE_UNMARKED** estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a421d-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="a421d-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="a421d-164">_ppError_</span></span>
  
> <span data-ttu-id="a421d-165">[out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** contendo informações de versão, componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="a421d-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="a421d-166">Pode ser nulo se nenhuma informação estendida de erro for desejada.</span><span class="sxs-lookup"><span data-stu-id="a421d-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="a421d-167">Gratuito com [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a421d-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="a421d-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="a421d-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="a421d-169">[o] Um ponteiro para um ponteiro para a interface retornada **IOlkApptRebaser**.</span><span class="sxs-lookup"><span data-stu-id="a421d-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a421d-170">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a421d-170">Return values</span></span>

<span data-ttu-id="a421d-171">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a421d-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a421d-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="a421d-172">Remarks</span></span>

<span data-ttu-id="a421d-173">Ao usar [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para procurar o endereço dessa função em tzmovelib especifique **ApptRebaser@44** como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="a421d-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="a421d-174">Nem todos os sinalizadores são válidos nas combinações entre si.</span><span class="sxs-lookup"><span data-stu-id="a421d-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="a421d-175">Para saber mais sobre as diversas opções, confira a seção "Opções de glossário de linha de comando para a ferramenta de atualização de dados de fuso horário do Outlook " no [931667 KB: como alterar o fuso horário endereço usando a ferramenta de atualização de dados de fuso horário do Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="a421d-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a421d-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="a421d-176">See also</span></span>

- [<span data-ttu-id="a421d-177">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="a421d-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

