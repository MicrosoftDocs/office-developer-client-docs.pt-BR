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
ms.openlocfilehash: 7a6971504ec8f4f5ac8593b6b78777a12ff92b3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564560"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso às propriedades muitos que estão associados aos usuários de mensagens. A interface de **IMailUser** é implementada por objetos de usuário de mensagens. **IMailUser** herde a [IMAPIProp: IUnknown](imapipropiunknown.md) interface e não possui exclusivos métodos sua própria conta. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de usuário de mensagens  <br/> |
|Implementada por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMailUser  <br/> |
|Tipo de ponteiro:  <br/> |LPMAILUSER  <br/> |
|Modelo de transação:  <br/> |Transacionadas  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

Essa interface não tem quaisquer métodos exclusivos.
  
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

Cinco das propriedades necessárias são conhecidos como as propriedades de um endereço base para destinatários:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Essas propriedades serão consideradas especiais porque muitos outros grupos de propriedades semelhantes se baseiam neste grupo base. Os outros grupos são usados para descrever um destinatário em várias funções, tais como uma mensagem original ou delegar o remetente. Para obter mais informações sobre essas propriedades e como usá-las, consulte [Tipos de endereço de MAPI](mapi-address-types.md).
  
Mensagens de usuários podem exibir uma coleção de suas propriedades, oferecendo suporte a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** é uma tabela de exibição que descreve o layout de uma caixa de diálogo detalhes ou uma página de propriedades com guias que exibe informações de propriedade do destinatário. MAPI cria detalhes caixas de diálogo quando um cliente chama o método [IAddrBook::Details](iaddrbook-details.md) . 
  
Objetos de usuário de mensagens podem ter outras propriedades opcionais associadas a eles. MAPI define várias propriedades que fornecem informações adicionais sobre um usuário de mensagens de endereçamento. Todas essas propriedades são cadeias de caracteres. A lista a seguir mostra mais comumente usadas propriedades:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([Pidtagassistant de MAPI](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Para obter uma lista completa das propriedades, consulte [Mapeamento canônico nomes de propriedade para nomes de MAPI](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

