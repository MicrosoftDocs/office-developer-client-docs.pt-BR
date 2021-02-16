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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 07e1c2104068a6eb242e8ba81f91655edaa92cd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426237"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona, exclui ou modifica destinatários de mensagens.
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Máscara de bits de sinalizadores que controla as alterações do destinatário. Se zero for passado para o parâmetro _ulFlags,_ **ModifyRecipients** substituirá todos os destinatários existentes pela lista de destinatários apontada pelo parâmetro _lpMods._ Os sinalizadores a seguir podem ser _definidos para ulFlags:_
    
MODRECIP_ADD 
  
> Os destinatários apontados pelo  _parâmetro lpMods_ devem ser adicionados à lista de destinatários. 
    
MODRECIP_MODIFY 
  
> Os destinatários apontados pelo  _parâmetro lpMods_ devem substituir os destinatários existentes. Todas as propriedades existentes são substituídas por aquelas na estrutura [ADRENTRY](adrentry.md) correspondente. 
    
MODRECIP_REMOVE 
  
> Os destinatários existentes devem ser removidos da lista de destinatários usando como índice a propriedade **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) incluída na matriz de valores de propriedade de cada entrada de destinatário no parâmetro _lpMods._ 
    
 _lpMods_
  
> [in] Ponteiro para uma [estrutura ADRLIST](adrlist.md) que contém uma lista de destinatários a serem adicionados, excluídos ou modificados na mensagem. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A lista de destinatários foi modificada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMessage::ModifyRecipients** altera a lista de destinatários da mensagem. É dessa lista, mantida em uma estrutura [ADRLIST,](adrlist.md) que a tabela de destinatários é criada. 
  
A **estrutura ADRLIST** contém uma estrutura [ADRENTRY](adrentry.md) para cada destinatário e cada estrutura **ADRENTRY** contém uma matriz de valores de propriedade que descrevem as propriedades do destinatário. 
  
Os destinatários na **estrutura ADRLIST** podem ser resolvidos ou não resolvidos. A diferença está no número e no tipo de propriedades incluídas. Um destinatário não resolvido contém apenas as propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) enquanto um destinatário resolvido contém essas duas propriedades mais **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Se **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) estiver disponível, ele também pode ser incluído.
  
No momento em que uma mensagem é enviada, ela deve incluir somente destinatários resolvidos em sua lista de destinatários. Destinatários não resolvidos causam relatórios de não entrega a serem criados e enviados ao remetente original da mensagem. Para obter mais informações sobre o processo de resolução de nomes da perspectiva do cliente, [consulte Resolvendo um nome.](resolving-a-recipient-name.md) Para obter mais informações da perspectiva do provedor de agendamento de endereços, consulte [Implementando a resolução de nomes.](implementing-name-resolution.md)
  
Além de destinatários resolvidos e não resolvidos, um destinatário pode ser NULL. O **membro cValues** da estrutura **ADRENTRY** do destinatário é definido como zero e o membro **rgPropVals** é definido como NULL. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode criar uma lista de destinatários chamando [IAddrBook::Address](imapisupport-address.md) para exibir a caixa de diálogo comum e solicitar que o usuário selecione entradas. A lista de endereços apontada pelo parâmetro _lppAdrList_ para **Address** pode ser passada para **ModifyRecipients** como o _parâmetro lpMods._ 
  
Quando você especificar propriedades para um destinatário na estrutura [ADRLIST,](adrlist.md) inclua todas as propriedades do destinatário, não apenas as novas ou alteradas. Quando um destinatário é modificado, todas as propriedades não incluídas na estrutura **ADRLIST** são excluídas. Para recuperar o conjunto atual de propriedades de todos os destinatários de uma mensagem, chame [GetRecipientTable](imessage-getrecipienttable.md) e recupere todas as linhas. Como um **SRowSet** é idêntico na estrutura a uma **ADRLIST,** você pode usá-lo de forma intercambiável.
  
 **ModifyRecipients** substitui todas as entradas na lista de destinatários atual pelas informações apontadas por _lpMods_ quando nenhum dos sinalizadores é definido no _parâmetro ulFlags._ 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando você definir o sinalizador MODRECIP_MODIFY, **ModifyRecipients** substituirá cada linha de destinatário inteira pela linha associada na estrutura [ADRLIST](adrlist.md) passada  _em lpMods_. Tenha cuidado para especificar todas as propriedades que um destinatário deve ter, independentemente de ele ter sido alterado para impedir a exclusão não intencional.
  
A seguir estão algumas regras para definir as propriedades dos destinatários na estrutura **ADRLIST:** 
  
- Não use PT_NULL como um tipo de propriedade. **ModifyRecipients** retorna um erro ao encontrar esse valor. 
    
- Não use PT_ERROR como um tipo de propriedade. **ModifyRecipients** ignora esse valor. 
    
- Inclua a **PR_ROWID** para todos os destinatários quando você definir o sinalizador MODRECIP_REMOVE ou MODRECIP_MODIFY em  _ulFlags_. 
    
- Não inclua a **PR_ROWID** para nenhum dos destinatários quando você definir o sinalizador MODRECIP_ADD em  _ulFlags_ ou quando passar zero em  _ulFlags_.
    
Se você incluir  **PR_ADDRTYPE** propriedade PR_ADDRTYPE ou PR_EMAIL_ADDRESS para um destinatário e uma ou ambas as propriedades são inconsistentes com o tipo de endereço e o endereço do destinatário conforme identificado pelo **PR_ENTRYID**, os resultados serão indefinido. Ou seja, há três possibilidades, dependendo do provedor de serviços:
  
- A mensagem será entregue no endereço descrito pelas propriedades **PR_ADDRTYPE** e **PR_EMAIL_ADDRESS** usuário. 
    
- A mensagem será entregue ao destinatário identificado por **PR_ENTRYID**.
    
- A mensagem será declarada como não entregue devido à ambiguidade das informações de endereço.
    
Use as regras de alocação descritas em [Managing Memory for ADRLIST e SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) para alocar memória para a lista de destinatários. **ModifyRecipients** não libera a estrutura **ADRLIST** nem qualquer uma de suas subestruturas. A **estrutura ADRLIST** e cada [estrutura SPropValue](spropvalue.md) devem ser alocadas separadamente usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) de forma que cada uma possa ser liberada individualmente. Se o método exigir espaço adicional para qualquer estrutura **SPropValue,** ele poderá substituir a estrutura **SPropValue** por uma nova que pode ser liberada posteriormente usando [MAPIFreeBuffer](mapifreebuffer.md). A estrutura **SPropValue** original também deve ser liberada usando **MAPIFreeBuffer**.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI usa o **método IMessage::ModifyRecipients** para adicionar um novo destinatário a uma mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

