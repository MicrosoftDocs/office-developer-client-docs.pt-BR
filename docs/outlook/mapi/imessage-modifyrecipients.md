---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3edcef69880dbc2a566a44582113c43802a47324
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767387"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**Aplica-se a**: Outlook 
  
Adiciona, exclui ou modifica os destinatários da mensagem.
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla as alterações do destinatários. Se o zero é passado para o parâmetro _ulFlags_ , **ModifyRecipients** substitui todos os destinatários existentes com a lista de destinatários apontada pelo parâmetro _lpMods_ . Sinalizadores a seguir podem ser definidos para _ulFlags_:
    
MODRECIP_ADD 
  
> Os destinatários apontados pelo parâmetro _lpMods_ devem ser adicionados à lista de destinatários. 
    
MODRECIP_MODIFY 
  
> Os destinatários apontados pelo parâmetro _lpMods_ devem substituir destinatários existentes. Todas as propriedades existentes são substituídas por aqueles na estrutura de [ADRENTRY](adrentry.md) correspondente. 
    
MODRECIP_REMOVE 
  
> Destinatários existentes devem ser removidos da lista de destinatários usando, como um índice, a propriedade **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) incluída na matriz de valor de propriedade de cada entrada do destinatário no parâmetro _lpMods_ . 
    
 _lpMods_
  
> [in] Ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém uma lista de destinatários para ser adicionado, excluído ou modificado na mensagem. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A lista de destinatários com êxito foi modificada.
    
## <a name="remarks"></a>Coment�rios

O método **IMessage::ModifyRecipients** altera a lista de destinatários da mensagem. É a partir dessa lista, mantida em uma estrutura [ADRLIST](adrlist.md) , que a tabela de destinatário é criada. 
  
A estrutura **ADRLIST** contém uma estrutura [ADRENTRY](adrentry.md) para cada destinatário e cada estrutura **ADRENTRY** contém uma matriz de valores de propriedades descrevendo as propriedades do destinatário. 
  
Destinatários na estrutura de **ADRLIST** podem ser resolvidos ou não resolvidos. A diferença é o número e o tipo de propriedades que são incluídos. Um destinatário não resolvido contém somente as propriedades de **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) enquanto um destinatário resolvido contém essas duas propriedades plus **PR_ADDRTYPE **([PidTagAddressType](pidtagaddresstype-canonical-property.md)) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Se **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) estiver disponível, ele pode ser incluído também.
  
No momento em que uma mensagem é enviada, ele deve incluir somente os destinatários resolvidos na sua lista de destinatários. Destinatários não resolvidos causam NDRs seja criado e enviado ao remetente original da mensagem. Para obter mais informações sobre o processo de resolução de nomes da perspectiva do cliente, consulte a [resolução de nomes](resolving-a-recipient-name.md). Para obter mais informações da perspectiva do provedor de catálogo de endereços, consulte [Implementando a resolução de nome](implementing-name-resolution.md).
  
Além dos destinatários resolvidos e não resolvidos, um destinatário pode ser NULL. O membro **cValues** da estrutura **ADRENTRY** para o destinatário está definido como zero e o membro **rgPropVals** é definido como NULL. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode criar uma lista de destinatários chamando [IAddrBook::Address](imapisupport-address.md) para exibir a caixa de diálogo comuns e solicita ao usuário para selecionar entradas. A lista de endereços apontada pelo parâmetro _lppAdrList_ como **endereço** pode ser passada para **ModifyRecipients** como o parâmetro _lpMods_ . 
  
Quando você especificar propriedades para um destinatário na estrutura [ADRLIST](adrlist.md) , inclua todas as propriedades do destinatário, não apenas aqueles novos ou alterados. Quando um destinatário é modificado, todas as propriedades não incluídas na estrutura **ADRLIST** são excluídas. Para recuperar o conjunto atual de propriedades para todos os destinatários da mensagem, chame [GetRecipientTable](imessage-getrecipienttable.md) e recuperar todas as linhas. Como um **SRowSet** é idêntica em estrutura um **ADRLIST**, você pode usá-los de forma intercambiável.
  
 **ModifyRecipients** substitui todas as entradas na lista de destinatários atual com as informações apontadas pela _lpMods_ quando nenhum dos sinalizadores estão definidos no parâmetro _ulFlags_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando você definir o sinalizador MODRECIP_MODIFY, **ModifyRecipients** substitui cada linha inteira de destinatário com a linha associada na estrutura [ADRLIST](adrlist.md) passada em _lpMods_. Tenha cuidado para especificar que todas as propriedades que um destinatário deve ter independentemente se eles foram alterados para impedir que está sendo excluído acidentalmente.
  
Estas são algumas regras para definir as propriedades dos destinatários na estrutura de **ADRLIST** : 
  
- Não use PT_NULL como um tipo de propriedade. **ModifyRecipients** retornará um erro quando se deparar com esse valor. 
    
- Não use PT_ERROR como um tipo de propriedade. **ModifyRecipients** ignora esse valor. 
    
- Inclua a propriedade **PR_ROWID** para todos os destinatários quando você definir o sinalizador o MODRECIP_REMOVE ou MODRECIP_MODIFY no _ulFlags_. 
    
- Não inclua a propriedade **PR_ROWID** para qualquer um dos destinatários quando você definir o sinalizador MODRECIP_ADD no _ulFlags_ ou quando você passá zero em _ulFlags_.
    
Se você incluir a propriedade **PR_ADDRTYPE** ou a propriedade **PR_EMAIL_ADDRESS** para um destinatário e uma ou ambas dessas propriedades são inconsistentes com o tipo de endereço e o endereço do destinatário, conforme identificado pelo **PR_ENTRYID**, o os resultados são indefinidos. Ou seja, há três possibilidades, dependendo do provedor de serviço:
  
- A mensagem será entregue para o endereço descrito pelas propriedades **PR_ADDRTYPE** e **PR_EMAIL_ADDRESS** . 
    
- A mensagem será entregue ao destinatário identificado pela **PR_ENTRYID**.
    
- A mensagem será declarada não entregue devido a ambiguidade das informações de endereço.
    
Use as regras de alocação descritas no [Gerenciamento de memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md) alocar memória para a lista de destinatários. **ModifyRecipients** não liberar a estrutura **ADRLIST** nem qualquer uma das suas subestruturas. A estrutura **ADRLIST** e cada estrutura [SPropValue](spropvalue.md) devem ser alocados separadamente usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , de forma que cada uma pode ser liberada individualmente. Se o método requer espaço adicional para qualquer estrutura **SPropValue** , ele pode substituir a estrutura de **SPropValue** por um novo que posteriormente pode ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md). A estrutura original de **SPropValue** também deve ser liberada usando **MAPIFreeBuffer**.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI usa o método **IMessage::ModifyRecipients** para adicionar um novo destinatário a uma mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

