---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351391"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a várias propriedades que estão associadas a usuários de mensagens. A interface **IMailUser** é implementada por objetos de usuário de mensagens. O **IMailUser** herda da interface [IMAPIProp: IUnknown](imapipropiunknown.md) e não tem métodos exclusivos próprios. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos do usuário de mensagens  <br/> |
|Implementado por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMailUser  <br/> |
|Tipo de ponteiro:  <br/> |LPMAILUSER  <br/> |
|Modelo de transação:  <br/> |Transact  <br/> |
   
## <a name="vtable-order"></a>Vtable order

Esta interface não tem nenhum método exclusivo.
  
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Cinco das propriedades necessárias são conhecidas como as propriedades de endereço base para destinatários:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Essas propriedades são consideradas especiais porque muitos outros grupos de propriedades semelhantes são criados sobre esse grupo base. Os outros grupos são usados para descrever um destinatário em várias funções, como o remetente original ou delegado da mensagem. Para obter mais informações sobre essas propriedades e como usá-las, confira [tipos de endereço MAPI](mapi-address-types.md).
  
Os usuários de mensagens podem exibir uma coleção de suas propriedades ao suportar a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** é uma tabela de exibição que descreve o layout de uma caixa de diálogo de detalhes ou uma página de propriedades com guias que exibe informações sobre as propriedades do destinatário. MAPI cria caixas de diálogo detalhes quando um cliente chama o método [IAddrBook::D etails](iaddrbook-details.md) . 
  
Os objetos do usuário de mensagens podem ter outras propriedades opcionais associadas a eles. O MAPI define muitas propriedades que fornecem informações de endereçamento adicionais sobre um usuário de mensagens. Todas essas propriedades são cadeias de caracteres. A lista a seguir mostra as propriedades mais comumente usadas:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Para obter uma lista completa das propriedades, consulte [mapeamento de nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

