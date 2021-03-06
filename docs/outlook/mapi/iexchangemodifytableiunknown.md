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
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oferece suporte ao acesso a objetos de tabela do Microsoft Exchange Server, especificamente objetos de tabela sacl (lista de controle de acesso ao sistema) e objetos de tabela de regras em pastas do Microsoft Exchange Server. Essa interface se parece com a interface [IMAPITable : IUnknown,](imapitableiunknown.md) mas adiciona suporte a estruturas específicas do Microsoft Exchange Server que são usadas para controlar SACLs e regras. 
  
|||
|:-----|:-----|
|Exposto por:  <br/> |Nenhum  <br/> |
|Implementado por:  <br/> |Objetos de tabela de servidor  <br/> |
|Chamado por:  <br/> |MAPI e aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IExchangeModifyTable  <br/> |
|Tipo de ponteiro:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modelo de transação:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Retorna informações sobre o último erro que ocorreu em um objeto table.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Retorna um ponteiro para uma interface para um objeto de tabela MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Atualiza um objeto de tabela MAPI.  <br/> |
   
|**Propriedades usadas para modificar uma tabela de regras**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
|**Propriedades usadas para modificar uma tabela SACL**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter a interface **IExchangeModifyTable,** chame o método [MAPI IMAPIProp::OpenProperty](imapiprop-openproperty.md) em uma propriedade do tipo PT_OBJECT em um objeto folder. Ao chamar o **método OpenProperty,** passe o valor **IID_IExchangeModifyTable** no _parâmetro lpiid._ 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

