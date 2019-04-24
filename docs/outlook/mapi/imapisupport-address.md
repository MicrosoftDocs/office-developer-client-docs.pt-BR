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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331602"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe a caixa de diálogo endereço comum. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parâmetros

 _lpulUIParam_
  
> [in, out] Um ponteiro para o identificador da janela pai da caixa de diálogo. Na entrada, um identificador de janela deve sempre ser aprovado. Na saída, se o sinalizador DIALOG_SDI estiver definido na estrutura [ADRPARM](adrparm.md) apontada pelo parâmetro _lpAdrParms_ , o identificador de janela da caixa de diálogo sem-modo será retornado. 
    
 _lpAdrParms_
  
> [in, out] Um ponteiro para uma estrutura **ADRPARM** que controla a apresentação e o comportamento da caixa de diálogo de endereço. 
    
 _lppAdrList_
  
> [in, out] Um ponteiro para um ponteiro para uma lista de endereços. Na entrada, essa lista é a lista atual de destinatários em uma mensagem ou nulo, se não houver essa lista. Na saída, _lppAdrList_ aponta para uma lista atualizada de destinatários da mensagem. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo endereço foi exibida com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: address** é implementado para objetos de suporte do provedor de catálogo de endereços. Os provedores de catálogo de endereços chamam o **endereço** para criar ou atualizar uma lista de destinatários de mensagens. 
  
Cada destinatário é descrito em uma estrutura [ADRENTRY](adrentry.md) que é incluída na estrutura [das ADRLIST](adrlist.md) indicada pelo parâmetro _lppAdrList_ . A estrutura **ADRENTRY** contém uma matriz de valores de propriedade de destinatário, uma das quais é o tipo do destinatário ou a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Essa estrutura **das ADRLIST** pode ser passada para um cliente para uso como o parâmetro _lpMods_ em uma chamada para [IMessage:: ModifyRecipients](imessage-modifyrecipients.md).
  
Cada destinatário na estrutura **das ADRLIST** pode ser resolvido, o que indica que um de seus valores de propriedade é sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou não resolvido, o que indica que a propriedade **PR_ENTRYID** é encontrado. 
  
Além de **PR_ENTRYID**, os destinatários resolvidos incluem as seguintes propriedades:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Os destinatários não resolvidos normalmente incluem apenas **PR_DISPLAY_NAME** e **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A estrutura **das ADRLIST** que o chamador transmite pode ser um tamanho diferente da estrutura que o MAPI retorna. Ao alocar memória para a estrutura **das ADRLIST** , aloque a memória de cada estrutura do [SPropValue](spropvalue.md) separadamente. 
  
Use os ponteiros para as funções de alocação de memória MAPI passadas para sua função [ABProviderInit](abproviderinit.md) para alocar memória. Alocar memória com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para **das ADRLIST** e cada estrutura de valor de propriedade nas estruturas **ADRENTRY** no **das ADRLIST**. 
  
Se o **endereço** deve retornar uma estrutura **das ADRLIST** maior, ou se você tiver passado nulo para o _lppAdrList_, o **endereço** liberará a estrutura original e alocará uma nova. O **endereço** também aloca estruturas de valor de propriedade adicionais na estrutura **das ADRLIST** e libera as antigas conforme apropriado. Para obter mais informações sobre como a memória é gerenciada para estruturas **das ADRLIST** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
 O **endereço** retorna imediatamente se o sinalizador DIALOG_SDI foi definido na estrutura **ADRPARM** no parâmetro _lpAdrParms_ . 
  
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


[Gerenciando memória para estruturas das ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

