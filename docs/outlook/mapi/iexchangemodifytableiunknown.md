---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418103"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="bd87a-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd87a-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="bd87a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd87a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd87a-105">Oferece suporte ao acesso a objetos de tabela do Microsoft Exchange Server, especificamente objetos de tabela sacl (lista de controle de acesso ao sistema) e objetos de tabela de regras em pastas do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bd87a-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="bd87a-106">Essa interface se parece com a interface [IMAPITable : IUnknown,](imapitableiunknown.md) mas adiciona suporte a estruturas específicas do Microsoft Exchange Server que são usadas para controlar SACLs e regras.</span><span class="sxs-lookup"><span data-stu-id="bd87a-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd87a-107">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="bd87a-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="bd87a-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bd87a-108">None</span></span>  <br/> |
|<span data-ttu-id="bd87a-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bd87a-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="bd87a-110">Objetos de tabela de servidor</span><span class="sxs-lookup"><span data-stu-id="bd87a-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="bd87a-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="bd87a-111">Called by:</span></span>  <br/> |<span data-ttu-id="bd87a-112">MAPI e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="bd87a-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="bd87a-113">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="bd87a-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bd87a-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="bd87a-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="bd87a-115">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="bd87a-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="bd87a-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="bd87a-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="bd87a-117">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="bd87a-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="bd87a-118">Transacted</span><span class="sxs-lookup"><span data-stu-id="bd87a-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bd87a-119">Vtable order</span><span class="sxs-lookup"><span data-stu-id="bd87a-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bd87a-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="bd87a-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="bd87a-121">Retorna informações sobre o último erro que ocorreu em um objeto table.</span><span class="sxs-lookup"><span data-stu-id="bd87a-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="bd87a-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="bd87a-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="bd87a-123">Retorna um ponteiro para uma interface para um objeto de tabela MAPI.</span><span class="sxs-lookup"><span data-stu-id="bd87a-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="bd87a-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="bd87a-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="bd87a-125">Atualiza um objeto de tabela MAPI.</span><span class="sxs-lookup"><span data-stu-id="bd87a-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="bd87a-126">**Propriedades usadas para modificar uma tabela de regras**</span><span class="sxs-lookup"><span data-stu-id="bd87a-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="bd87a-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="bd87a-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd87a-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="bd87a-148">**Propriedades usadas para modificar uma tabela SACL**</span><span class="sxs-lookup"><span data-stu-id="bd87a-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="bd87a-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="bd87a-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd87a-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd87a-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd87a-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd87a-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd87a-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd87a-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd87a-158">Remarks</span></span>

<span data-ttu-id="bd87a-159">Para obter a interface **IExchangeModifyTable,** chame o método [MAPI IMAPIProp::OpenProperty](imapiprop-openproperty.md) em uma propriedade do tipo PT_OBJECT em um objeto folder.</span><span class="sxs-lookup"><span data-stu-id="bd87a-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="bd87a-160">Ao chamar o **método OpenProperty,** passe o valor **IID_IExchangeModifyTable** no _parâmetro lpiid._</span><span class="sxs-lookup"><span data-stu-id="bd87a-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd87a-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd87a-161">See also</span></span>



[<span data-ttu-id="bd87a-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="bd87a-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

