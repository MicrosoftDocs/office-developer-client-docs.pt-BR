---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1526ed54fd3773856b009c7c3570064f5a66df28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594940"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um identificador de entrada para um endereço one-off.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpszName_
  
> [in] Um ponteiro para o nome de exibição do destinatário a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). O parâmetro _lpszName_ pode ser NULL. 
    
 _lpszAdrType_
  
> [in] Um ponteiro para o tipo de endereço (por exemplo, FAX, SMTP ou X500) do destinatário. O parâmetro _lpszAdrType_ não pode ser NULL. 
    
 _lpszAddress_
  
> [in] Um ponteiro para o endereço de mensagens do destinatário. O parâmetro _lpszAddress_ não pode ser NULL. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que afeta o destinatário único. Sinalizadores a seguir podem ser definidos:
    
MAPI_SEND_NO_RICH_INFO 
  
> O destinatário não pode manipular o conteúdo da mensagem formatada. Se MAPI_SEND_NO_RICH_INFO for definido, o MAPI define a propriedade de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como FALSE. Se MAPI_SEND_NO_RICH_INFO não estiver definida, o MAPI define essa propriedade como TRUE, a menos que o endereço do destinatário mensagens apontado pela _lpszAddress_ é interpretado como um endereço de Internet. Nesse caso, MAPI define **PR_SEND_RICH_INFO** como FALSE. 
    
MAPI_UNICODE 
  
> O nome para exibição, tipo de endereço e endereço estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada para o destinatário único.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada únicos foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::CreateOneOff** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços de chamarem **CreateOneOff** para criar um identificador de entrada para um destinatário único (um destinatário que não pertençam a qualquer um dos contêineres de qualquer um dos provedores de catálogo de endereços carregado no momento). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando tiver terminado, usando o identificador de entrada retornado por **CreateOneOff**, libere a memória alocada para o identificador de entrada usando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Observações para provedores de transporte

Suportar o TNEF Transport Neutral Encapsulation Format () e use o valor da propriedade **PR_SEND_RICH_INFO** para determinar quando usar o TNEF quando você uma mensagem de transporte. Não suporte TNEF ou não enviar uma mensagem neste formato, quando ele for solicitado pode ser um problema para clientes baseados no formulário ou clientes que requerem propriedades personalizadas de MAPI. Isso ocorre porque o TNEF é geralmente usada para enviar propriedades personalizadas para classes de mensagem personalizada. 
  
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônico de PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriedade canônico de PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

