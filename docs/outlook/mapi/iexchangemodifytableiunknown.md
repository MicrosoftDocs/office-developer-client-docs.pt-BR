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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766923"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="b1886-103">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1886-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="b1886-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1886-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1886-105">Suporta o acesso a objetos de tabela do Microsoft Exchange Server, especificamente acesso ao sistema controlar objetos da tabela SACL (lista) e regra objetos table em pastas do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b1886-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="b1886-106">Esta interface é semelhante a [IMAPITable: IUnknown](imapitableiunknown.md) interface, mas ele adiciona suporte a estruturas específicas de servidor Microsoft Exchange que são usadas para controlar a SACL e regras.</span><span class="sxs-lookup"><span data-stu-id="b1886-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1886-107">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="b1886-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="b1886-108">None</span><span class="sxs-lookup"><span data-stu-id="b1886-108">None</span></span>  <br/> |
|<span data-ttu-id="b1886-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b1886-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="b1886-110">Objetos de tabela de servidor</span><span class="sxs-lookup"><span data-stu-id="b1886-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="b1886-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b1886-111">Called by:</span></span>  <br/> |<span data-ttu-id="b1886-112">Aplicativos MAPI e cliente</span><span class="sxs-lookup"><span data-stu-id="b1886-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="b1886-113">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="b1886-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b1886-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="b1886-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="b1886-115">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="b1886-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="b1886-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="b1886-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="b1886-117">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="b1886-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="b1886-118">Transacionadas</span><span class="sxs-lookup"><span data-stu-id="b1886-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b1886-119">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="b1886-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b1886-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1886-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="b1886-121">Retorna informações sobre o último erro que ocorreu em um objeto table.</span><span class="sxs-lookup"><span data-stu-id="b1886-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="b1886-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="b1886-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="b1886-123">Retorna um ponteiro para uma interface para um objeto table MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1886-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="b1886-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="b1886-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="b1886-125">Atualiza um objeto table MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1886-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="b1886-126">**Propriedades usadas para modificar uma tabela de regras**</span><span class="sxs-lookup"><span data-stu-id="b1886-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="b1886-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="b1886-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1886-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="b1886-148">**Propriedades usadas para modificar uma tabela SACL**</span><span class="sxs-lookup"><span data-stu-id="b1886-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="b1886-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="b1886-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1886-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="b1886-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1886-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b1886-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1886-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1886-158">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b1886-158">Remarks</span></span>

<span data-ttu-id="b1886-159">Para obter a interface **IExchangeModifyTable** , chame o método MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em uma propriedade do tipo PT_OBJECT em um objeto folder.</span><span class="sxs-lookup"><span data-stu-id="b1886-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="b1886-160">Quando você chama o método **OpenProperty** , passa o valor **IID_IExchangeModifyTable** no parâmetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="b1886-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1886-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1886-161">See also</span></span>



[<span data-ttu-id="b1886-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b1886-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

