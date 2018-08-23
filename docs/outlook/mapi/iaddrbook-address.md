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
ms.openlocfilehash: a13696b355e6fd815cd6bda42843505d9fc3d1f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579953"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe a caixa de diálogo do catálogo de endereços do Outlook. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parâmetros

 _lpulUIParam_
  
> [além, out] Um ponteiro para um identificador da janela pai da caixa de diálogo. Na entrada, um identificador da janela sempre deve ser passado. Na saída, se o membro **ulFlags** do parâmetro _lpAdrParms_ estiver definido como DIALOG_SDI, o identificador da janela da caixa de diálogo sem janela restrita é retornado. Consulte os comentários. 
    
 _lpAdrParms_
  
> [além, out] Um ponteiro para uma estrutura [ADRPARM](adrparm.md) que controla a apresentação e o comportamento da caixa de diálogo endereço. 
    
 _lppAdrList_
  
> [além, out] Um ponteiro para um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém informações do destinatário. Na entrada, esse parâmetro pode ser NULL ou apontar para um ponteiro válido. Na saída, este parâmetro aponta para um ponteiro para informações do destinatário válidos. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A caixa de diálogo endereço comuns com êxito foi exibida.
    
## <a name="remarks"></a>Comentários

Se o membro **ulFlags** do parâmetro _lpAdrParms_ estiver definido como DIALOG_SDI prevendo o retorno da alça de janela da caixa de diálogo sem janela restrita na saída, ele é ignorado no Outlook; a versão modal da caixa de diálogo sempre é mostrada nos clientes não do Outlook. 
  
A estrutura **ADRLIST** passada volta pelo MAPI para o chamador através do parâmetro _lppAdrList_ contém uma matriz de estruturas [ADRENTRY](adrentry.md) , uma estrutura de cada destinatário. Quando passados ao método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) de uma mensagem de saída no parâmetro _lpMods_ , a estrutura **ADRLIST** pode ser usada para atualizar sua lista de destinatários. 
  
Cada estrutura **ADRENTRY** na estrutura **ADRLIST** contém zero ou mais estruturas de [SPropValue](spropvalue.md) , uma estrutura para cada propriedade definida para o destinatário. Pode haver zero estruturas **SPropValue** quando a caixa de diálogo apresentada pelo método **endereço** é usada para remover um destinatário. Quando houver uma ou mais estruturas de **SPropValue** , a estrutura **ADRENTRY** correspondente é usada para adicionar ou atualizar um destinatário. O destinatário pode ser resolvido, que indica que uma das estruturas **SPropValue** descreve a propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do destinatário, ou não resolvidos, que indica que a propriedade **PR_ENTRYID** é ausente. 
  
Além das **PR_ENTRYID**, destinatários resolvidos incluem as seguintes propriedades:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
A estrutura **ADRLIST** que o chamador passa nas pode ser um tamanho diferente da estrutura de MAPI retorna. Se o MAPI deve retornar uma estrutura maior de **ADRLIST** , ele libera a estrutura original e aloca um novo. Quando você alocar memória para a estrutura **ADRLIST** , alocar a memória para cada estrutura **SPropValue** separadamente. Para obter mais informações sobre como alocar e liberar **ADRLIST** estruturas, consulte [Gerenciando memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Endereço** retorna imediatamente se o sinalizador DIALOG_SDI é definido no membro **ulFlags** da estrutura **ADRPARM** no parâmetro _lpAdrParms_ . O sinalizador DIALOG_SDI é ignorado para clientes não do Outlook. Se DIALOG_SDI será ignorada, a versão modal da caixa de diálogo será exibida e um ponteiro para uma alça não deve ser esperado em _lpulUIParam_.
  
 **Endereço** suporta as sequências de caracteres Unicode na estrutura de **ADRPARM** se AB_UNICODEUI foi especificado no membro **ulFlags** **ADRPARM** no parâmetro _lpAdrParms_ e oferece suporte a cadeias de caracteres Unicode no ** ADRLIST**. As cadeias de caracteres Unicode são convertidas para o formato de cadeia de caracteres (MBCS) caracteres multibyte antes que eles sejam exibidos na caixa de diálogo do catálogo de endereços do Outlook.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI usa o método de **endereço** para permitir que o usuário selecione qual caixa de correio para abrir.  <br/> |
   
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


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

