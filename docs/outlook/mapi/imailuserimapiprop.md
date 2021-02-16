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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436591"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a muitas propriedades associadas a usuários de mensagens. A interface **IMailUser** é implementada por objetos de usuário de mensagens. **IMailUser** herda da interface [IMAPIProp : IUnknown](imapipropiunknown.md) e não tem métodos exclusivos próprios. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Objetos de usuário de mensagens  <br/> |
|Implementado por:  <br/> |Provedores de lista de endereços  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMailUser  <br/> |
|Tipo de ponteiro:  <br/> |LPMAILUSER  <br/> |
|Modelo de transação:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

Essa interface não tem métodos exclusivos.
  
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

Cinco das propriedades necessárias são conhecidas como propriedades de endereço base para destinatários:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Essas propriedades são consideradas especiais porque muitos outros grupos de propriedades semelhantes são construídos sobre esse grupo base. Os outros grupos são usados para descrever um destinatário em várias funções, como o remetente original ou delegado de uma mensagem. Para obter mais informações sobre essas propriedades e como usá-las, consulte [MAPI Address Types](mapi-address-types.md).
  
Os usuários de mensagens podem exibir uma coleção de suas propriedades dando suporte à **propriedade PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** é uma tabela de exibição que descreve o layout de uma caixa de diálogo de detalhes ou uma página de propriedades com guias que exibe informações de propriedade do destinatário. MAPI creates details dialog boxes when a client calls the [IAddrBook::D etails](iaddrbook-details.md) method. 
  
Os objetos de usuário de mensagens podem ter outras propriedades opcionais associadas a eles. MAPI define muitas propriedades que fornecem informações de endereçamento adicionais sobre um usuário de mensagens. Todas essas propriedades são cadeias de caracteres. A lista a seguir mostra as propriedades mais comumente usadas:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Para uma lista completa de propriedades, consulte Mapeamento de nomes de propriedades [canônicas para nomes MAPI.](mapping-canonical-property-names-to-mapi-names.md)
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

