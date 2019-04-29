---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407904"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe a caixa de diálogo catálogo de endereços do Outlook. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parâmetros

 _lpulUIParam_
  
> [in, out] Um ponteiro para um identificador da janela pai da caixa de diálogo. Na entrada, um identificador de janela deve sempre ser aprovado. Na saída, se o membro **parâmetroulflags** do parâmetro _lpAdrParms_ for definido como DIALOG_SDI, o identificador de janela da caixa de diálogo sem-modo será retornado. Consulte Comentários. 
    
 _lpAdrParms_
  
> [in, out] Um ponteiro para uma estrutura [ADRPARM](adrparm.md) que controla a apresentação e o comportamento da caixa de diálogo de endereço. 
    
 _lppAdrList_
  
> [in, out] Um ponteiro para um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que contém informações do destinatário. Na entrada, esse parâmetro pode ser nulo ou apontar para um ponteiro válido. Na saída, esse parâmetro aponta para um ponteiro para obter informações válidas do destinatário. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo endereço comum foi exibida com êxito.
    
## <a name="remarks"></a>Comentários

Se o membro **parâmetroulflags** do parâmetro _lpAdrParms_ estiver definido como DIALOG_SDI antecipando o retorno do identificador de janela da caixa de diálogo sem-modo na saída, ele será ignorado no Outlook; a versão modal da caixa de diálogo sempre é mostrada em clientes não-Outlook. 
  
A estrutura **das ADRLIST** passada de volta por MAPI para o chamador através do parâmetro _lppAdrList_ contém uma matriz de estruturas do [ADRENTRY](adrentry.md) , uma estrutura para cada destinatário. Quando passadas para o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) de uma mensagem de saída no parâmetro _lpMods_ , a estrutura **das ADRLIST** pode ser usada para atualizar sua lista de destinatários. 
  
Cada estrutura **ADRENTRY** na estrutura **das ADRLIST** contém zero ou mais estruturas de [SPropValue](spropvalue.md) , uma estrutura para cada conjunto de propriedades para o destinatário. Pode haver nenhuma estrutura **SPropValue** quando a caixa de diálogo apresentada pelo método **Address** é usada para remover um destinatário. Quando há uma ou mais estruturas **SPropValue** , a estrutura **ADRENTRY** correspondente é usada para adicionar ou atualizar um destinatário. O destinatário pode ser resolvido, o que indica que uma das estruturas **SPropValue** descreve a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do destinatário, ou não resolvida, que indica que a propriedade **PR_ENTRYID** é encontrado. 
  
Além de **PR_ENTRYID**, os destinatários resolvidos incluem as seguintes propriedades:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
A estrutura **das ADRLIST** que o chamador transmite pode ser um tamanho diferente da estrutura que o MAPI retorna. Se o MAPI deve retornar uma estrutura **das ADRLIST** maior, ele libera a estrutura original e aloca um novo. Ao alocar memória para a estrutura **das ADRLIST** , aloque a memória de cada estrutura do **SPropValue** separadamente. Para obter mais informações sobre como alocar e liberar estruturas do **das ADRLIST** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md)
  
 O **endereço** retorna imediatamente se o sinalizador DIALOG_SDI estiver definido no membro **Parâmetroulflags** da estrutura **ADRPARM** no parâmetro _lpAdrParms_ . O sinalizador DIALOG_SDI é ignorado para clientes que não são do Outlook. Se DIALOG_SDI for ignorado, a versão modal da caixa de diálogo será exibida e um ponteiro para um identificador não deverá ser esperado no _lpulUIParam_.
  
 O **endereço** oferece suporte a cadeias de caracteres Unicode na estrutura **ADRPARM** se AB_UNICODEUI foi especificado no membro **Parâmetroulflags** de **ADRPARM** no parâmetro _LpAdrParms_ e oferece suporte a cadeias de caracteres Unicode no ** DAS ADRLIST**. As cadeias de caracteres Unicode são convertidas no formato MBCS (cadeia de caracteres multibyte) antes de serem exibidas na caixa de diálogo catálogo de endereços do Outlook.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI usa o método **Address** para permitir que o usuário selecione qual caixa de correio abrir.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

