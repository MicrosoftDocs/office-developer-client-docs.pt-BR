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
ms.openlocfilehash: 51a83e1e28534cc237419d9c4ae475c1d719c5de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565071"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Suporta o acesso a objetos de tabela do Microsoft Exchange Server, especificamente acesso ao sistema controlar objetos da tabela SACL (lista) e regra objetos table em pastas do Microsoft Exchange Server. Esta interface é semelhante a [IMAPITable: IUnknown](imapitableiunknown.md) interface, mas ele adiciona suporte a estruturas específicas de servidor Microsoft Exchange que são usadas para controlar a SACL e regras. 
  
|||
|:-----|:-----|
|Expostos pelo:  <br/> |Nenhum  <br/> |
|Implementada por:  <br/> |Objetos de tabela de servidor  <br/> |
|Chamado pelo:  <br/> |Aplicativos MAPI e cliente  <br/> |
|Identificador de interface:  <br/> |IID_IExchangeModifyTable  <br/> |
|Tipo de ponteiro:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modelo de transação:  <br/> |Transacionadas  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Retorna informações sobre o último erro que ocorreu em um objeto table.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Retorna um ponteiro para uma interface para um objeto table MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Atualiza um objeto table MAPI.  <br/> |
   
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

Para obter a interface **IExchangeModifyTable** , chame o método MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em uma propriedade do tipo PT_OBJECT em um objeto folder. Quando você chama o método **OpenProperty** , passa o valor **IID_IExchangeModifyTable** no parâmetro _lpiid_ . 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

