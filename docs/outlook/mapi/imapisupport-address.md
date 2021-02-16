---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407316"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe a caixa de diálogo de endereço comum. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parâmetros

 _lpulUIParam_
  
> [in, out] Um ponteiro para o alça da janela pai da caixa de diálogo. Na entrada, uma alça de janela sempre deve ser passada. Na saída, se o sinalizador DIALOG_SDI for definido na estrutura [ADRPARM](adrparm.md) apontada pelo parâmetro  _lpAdrParms,_ a alça da janela da caixa de diálogo sem janela será retornada. 
    
 _lpAdrParms_
  
> [in, out] Um ponteiro para uma **estrutura ADRPARM** que controla a apresentação e o comportamento da caixa de diálogo de endereço. 
    
 _lppAdrList_
  
> [in, out] Um ponteiro para um ponteiro para uma lista de endereços. Na entrada, essa lista é a lista atual de destinatários em uma mensagem ou NULL, caso essa lista não exista. Na saída,  _lppAdrList_ aponta para uma lista atualizada de destinatários de mensagens. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo de endereço foi exibida com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::Address** é implementado para objetos de suporte do provedor de agendas de endereços. Os provedores de agendamento de endereços chamam **Address** para criar ou atualizar uma lista de destinatários de mensagens. 
  
Cada destinatário é descrito em uma estrutura [ADRENTRY](adrentry.md) incluída na estrutura [ADRLIST](adrlist.md) apontada pelo parâmetro _lppAdrList._ A **estrutura ADRENTRY** contém uma matriz de valores de propriedade de destinatário, um dos quais é o tipo do destinatário ou PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) . Essa **estrutura ADRLIST** pode ser passada para um cliente para usar como o parâmetro  _lpMods_ em uma chamada para [IMessage::ModifyRecipients](imessage-modifyrecipients.md).
  
Cada destinatário na estrutura **ADRLIST** pode ser resolvido, o que indica que um de seus valores de propriedade é sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ou não resolvido, o que indica que a propriedade **PR_ENTRYID** está ausente. 
  
Além de **PR_ENTRYID** destinatários resolvidos, incluem as seguintes propriedades:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Destinatários não resolvidos geralmente incluem apenas **PR_DISPLAY_NAME** e **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A **estrutura ADRLIST** que o chamador passa pode ter um tamanho diferente da estrutura que o MAPI retorna. Quando você alocar memória para **a estrutura ADRLIST,** aloce a memória para cada [estrutura SPropValue](spropvalue.md) separadamente. 
  
Use os ponteiros para as funções de alocação de memória MAPI passadas para sua função [ABProviderInit](abproviderinit.md) para alocar memória. Aloque memória com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para **ADRLIST** e cada estrutura de valor de propriedade nas estruturas **ADRENTRY** em **ADRLIST**. 
  
Se **Address** deve retornar uma estrutura **ADRLIST** maior, ou se você tiver passado NULL para  _lppAdrList_, **Address** libera a estrutura original e aloca uma nova. **O** endereço também aloca estruturas de valor de propriedade adicionais na estrutura **ADRLIST** e libera as antigas conforme apropriado. Para obter mais informações sobre como a memória é gerenciada para estruturas **ADRLIST,** consulte Gerenciando memória [para estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Address** retorna imediatamente se o DIALOG_SDI sinalizador foi definido na estrutura **ADRPARM** no _parâmetro lpAdrParms._ 
  
## <a name="see-also"></a>Confira também



[ABProviderInit](abproviderinit.md)
  
[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagAddressType](pidtagaddresstype-canonical-property.md)
  
[Propriedade canônica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriedade canônica PidTagDisplayType](pidtagdisplaytype-canonical-property.md)
  
[Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[Propriedade canônica PidTagRecipientType](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Gerenciando memória para estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

