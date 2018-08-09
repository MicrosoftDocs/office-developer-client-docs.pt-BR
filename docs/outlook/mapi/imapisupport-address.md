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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cb683178a8e258f571cbc3d05a3b030481905433
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767214"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Aplica-se a**: Outlook 
  
Exibe a caixa de diálogo endereço comuns. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parâmetros

 _lpulUIParam_
  
> [além, out] Um ponteiro para o identificador da janela pai da caixa de diálogo. Na entrada, um identificador da janela sempre deve ser passado. Na saída, se o sinalizador DIALOG_SDI é definido na estrutura [ADRPARM](adrparm.md) apontada pelo parâmetro _lpAdrParms_ , o identificador da janela da caixa de diálogo sem janela restrita é retornado. 
    
 _lpAdrParms_
  
> [além, out] Um ponteiro para uma estrutura **ADRPARM** que controla a apresentação e o comportamento da caixa de diálogo endereço. 
    
 _lppAdrList_
  
> [além, out] Um ponteiro para um ponteiro para uma lista de endereços. Na entrada, esta lista é a lista atual de destinatários em uma mensagem ou NULL, se existir lista desse tipo. Na saída, _lppAdrList_ aponta para uma lista atualizada de destinatários da mensagem. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A caixa de diálogo de endereço com êxito foi exibida.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::Address** é implementado para objetos de suporte do provedor de catálogo de endereços. Provedores de catálogo de endereço chamarem **endereço** para criar ou atualizar uma lista de destinatários da mensagem. 
  
Cada destinatário é descrito em uma estrutura [ADRENTRY](adrentry.md) que está incluída na estrutura [ADRLIST](adrlist.md) apontada pelo parâmetro _lppAdrList_ . A estrutura **ADRENTRY** contém uma matriz de valores de propriedade de destinatário, um dos quais é o tipo do destinatário ou propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Essa estrutura **ADRLIST** pode ser passada para um cliente para usar como o parâmetro _lpMods_ em uma chamada para [IMessage::ModifyRecipients](imessage-modifyrecipients.md).
  
Cada destinatário na estrutura de **ADRLIST** pode ser seja resolvido, que indica que um dos seus valores de propriedade é sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou não resolvidos, que indica que a propriedade **PR_ENTRYID** é ausente. 
  
Além das **PR_ENTRYID**, destinatários resolvidos incluem as seguintes propriedades:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Destinatários não resolvidos normalmente incluem somente **PR_DISPLAY_NAME** e **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A estrutura **ADRLIST** que o chamador passa nas pode ser um tamanho diferente da estrutura de MAPI retorna. Quando você alocar memória para a estrutura **ADRLIST** , alocar a memória para cada estrutura [SPropValue](spropvalue.md) separadamente. 
  
Use os ponteiros para as funções de alocação de memória MAPI passados para sua função [ABProviderInit](abproviderinit.md) para alocar memória. Alocar memória com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para **ADRLIST** e cada estrutura de valor de propriedade nas estruturas **ADRENTRY** em **ADRLIST**. 
  
Se o **endereço** deve retornar uma estrutura de **ADRLIST** maior, ou se você tiver passado NULL para _lppAdrList_, o **endereço** libera a estrutura original e aloca um novo. **Endereço** também aloca estruturas de valor de propriedade adicional na estrutura de **ADRLIST** e libera as antigas conforme apropriado. Para obter mais informações sobre como a memória é gerenciada para estruturas **ADRLIST** , consulte [Gerenciando memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Endereço** retorna imediatamente se o sinalizador DIALOG_SDI foi definido na estrutura **ADRPARM** no parâmetro _lpAdrParms_ . 
  
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


[Gerenciar memória das estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

