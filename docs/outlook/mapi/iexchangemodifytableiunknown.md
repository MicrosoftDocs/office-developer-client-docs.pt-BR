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
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766923"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="a1404-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1404-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="a1404-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1404-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1404-105">Suporta o acesso a objetos de tabela do Microsoft Exchange Server, especificamente acesso ao sistema controlar objetos da tabela SACL (lista) e regra objetos table em pastas do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a1404-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="a1404-106">Esta interface é semelhante a [IMAPITable: IUnknown](imapitableiunknown.md) interface, mas ele adiciona suporte a estruturas específicas de servidor Microsoft Exchange que são usadas para controlar a SACL e regras.</span><span class="sxs-lookup"><span data-stu-id="a1404-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1404-107">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="a1404-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="a1404-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a1404-108">None</span></span>  <br/> |
|<span data-ttu-id="a1404-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a1404-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1404-110">Objetos de tabela de servidor</span><span class="sxs-lookup"><span data-stu-id="a1404-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="a1404-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a1404-111">Called by:</span></span>  <br/> |<span data-ttu-id="a1404-112">Aplicativos MAPI e cliente</span><span class="sxs-lookup"><span data-stu-id="a1404-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="a1404-113">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="a1404-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a1404-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="a1404-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="a1404-115">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a1404-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="a1404-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="a1404-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="a1404-117">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="a1404-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="a1404-118">Transacionadas</span><span class="sxs-lookup"><span data-stu-id="a1404-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a1404-119">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="a1404-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a1404-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a1404-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="a1404-121">Retorna informações sobre o último erro que ocorreu em um objeto table.</span><span class="sxs-lookup"><span data-stu-id="a1404-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="a1404-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="a1404-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="a1404-123">Retorna um ponteiro para uma interface para um objeto table MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1404-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="a1404-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="a1404-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="a1404-125">Atualiza um objeto table MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1404-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="a1404-126">**Propriedades usadas para modificar uma tabela de regras**</span><span class="sxs-lookup"><span data-stu-id="a1404-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="a1404-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="a1404-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1404-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="a1404-148">**Propriedades usadas para modificar uma tabela SACL**</span><span class="sxs-lookup"><span data-stu-id="a1404-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="a1404-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="a1404-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1404-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="a1404-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a1404-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a1404-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1404-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1404-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1404-158">Remarks</span></span>

<span data-ttu-id="a1404-159">Para obter a interface **IExchangeModifyTable** , chame o método MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em uma propriedade do tipo PT_OBJECT em um objeto folder.</span><span class="sxs-lookup"><span data-stu-id="a1404-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="a1404-160">Quando você chama o método **OpenProperty** , passa o valor **IID_IExchangeModifyTable** no parâmetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="a1404-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1404-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1404-161">See also</span></span>



[<span data-ttu-id="a1404-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a1404-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

