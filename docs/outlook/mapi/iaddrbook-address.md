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
  
Exibe a caixa de diálogo do livro de endereços do Outlook. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parâmetros

 _lpulUIParam_
  
> [in, out] Um ponteiro para uma alça da janela pai da caixa de diálogo. Na entrada, uma alça de janela sempre deve ser passada. Na saída, se o membro **ulFlags** do parâmetro  _lpAdrParms_ estiver definido como DIALOG_SDI, o alça da janela da caixa de diálogo sem janela será retornado. Consulte os comentários. 
    
 _lpAdrParms_
  
> [in, out] Um ponteiro para uma [estrutura ADRPARM](adrparm.md) que controla a apresentação e o comportamento da caixa de diálogo de endereço. 
    
 _lppAdrList_
  
> [in, out] Um ponteiro para um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém informações de destinatário. Na entrada, esse parâmetro pode ser NULL ou apontar para um ponteiro válido. Na saída, esse parâmetro aponta para um ponteiro para informações válidas do destinatário. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo de endereço comum foi exibida com êxito.
    
## <a name="remarks"></a>Comentários

Se o membro **ulFlags** do parâmetro  _lpAdrParms_ estiver definido como DIALOG_SDI prevendo o retorno do alça de janela da caixa de diálogo sem janela na saída, ele será ignorado no Outlook; a versão modal da caixa de diálogo é sempre mostrada em clientes que não são do Outlook. 
  
A **estrutura ADRLIST** passada por MAPI para o chamador por meio do parâmetro  _lppAdrList_ contém uma matriz de estruturas [ADRENTRY,](adrentry.md) uma estrutura para cada destinatário. Quando passada para o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) de uma mensagem de saída no parâmetro  _lpMods,_ a estrutura **ADRLIST** pode ser usada para atualizar sua lista de destinatários. 
  
Cada **estrutura ADRENTRY** na estrutura **ADRLIST** contém zero ou mais estruturas [SPropValue,](spropvalue.md) uma estrutura para cada conjunto de propriedades para o destinatário. Pode haver zero **estruturas SPropValue** quando a caixa de diálogo apresentada pelo **método Address** é usada para remover um destinatário. Quando há uma ou mais **estruturas SPropValue,** a estrutura **ADRENTRY** correspondente é usada para adicionar ou atualizar um destinatário. O destinatário pode ser resolvido, o que indica que uma das estruturas **SPropValue** descreve a propriedade **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)do destinatário ou não resolvida, o que indica que a propriedade **PR_ENTRYID** está ausente. 
  
Além de **PR_ENTRYID** destinatários resolvidos, incluem as seguintes propriedades:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
A **estrutura ADRLIST** que o chamador passa pode ter um tamanho diferente da estrutura que o MAPI retorna. Se MAPI deve retornar uma estrutura **ADRLIST** maior, ele libera a estrutura original e aloca uma nova. Quando você alocar memória para **a estrutura ADRLIST,** aloce a memória para cada **estrutura SPropValue** separadamente. Para obter mais informações sobre como alocar e liberar estruturas **ADRLIST,** consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **O** endereço retornará imediatamente se DIALOG_SDI sinalizador for definido no membro **ulFlags** da estrutura **ADRPARM** no _parâmetro lpAdrParms._ O DIALOG_SDI sinalizador é ignorado para clientes que não são do Outlook. Se DIALOG_SDI for ignorado, a versão modal da caixa de diálogo será exibida e um ponteiro para um indicador não deve ser esperado em  _lpulUIParam_.
  
 **Address** dá suporte a cadeias de caracteres Unicode na estrutura **ADRPARM** se AB_UNICODEUI foi especificado no membro **ulFlags** de **ADRPARM** no parâmetro  _lpAdrParms_ e dá suporte a cadeias de caracteres Unicode em **ADRLIST**. As cadeias de caracteres Unicode são convertidas para o formato de cadeia de caracteres multibyte (MBCS) antes de serem exibidas na caixa de diálogo do livro de endereços do Outlook.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI usa o **método Address** para permitir que o usuário selecione qual caixa de correio abrir.  <br/> |
   
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

