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
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411992"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um identificador de entrada para um endereço único.
  
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
  
> [in] Um ponteiro para o nome de exibição do **destinatário PR_DISPLAY_NAME** propriedade ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). O  _parâmetro lpszName_ pode ser NULL. 
    
 _lpszAdrType_
  
> [in] Um ponteiro para o tipo de endereço (como FAX, SMTP ou X500) do destinatário. O  _parâmetro lpszAdrType_ não pode ser NULL. 
    
 _lpszAddress_
  
> [in] Um ponteiro para o endereço de mensagens do destinatário. O  _parâmetro lpszAddress_ não pode ser NULL. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que afeta o destinatário único. Os sinalizadores a seguir podem ser definidos:
    
MAPI_SEND_NO_RICH_INFO 
  
> O destinatário não pode manipular o conteúdo da mensagem formatada. Se MAPI_SEND_NO_RICH_INFO for definida, MAPI definirá a propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como FALSE. Se MAPI_SEND_NO_RICH_INFO não estiver definido, o MAPI definirá essa propriedade como TRUE, a menos que o endereço de mensagens do destinatário apontado por  _lpszAddress_ seja interpretado como um endereço da Internet. Nesse caso, MAPI **define** PR_SEND_RICH_INFO como FALSE. 
    
MAPI_UNICODE 
  
> O nome de exibição, o tipo de endereço e o endereço estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo _parâmetro lppEntryID._ 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada para o destinatário único.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada único foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::CreateOneOff** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços chamam **CreateOneOff** para criar um identificador de entrada para um destinatário único (um destinatário que não pertence a nenhum dos contêineres de nenhum dos provedores de agendamento carregados no momento). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando terminar de usar o identificador de entrada retornado por **CreateOneOff,** livre a memória alocada para o identificador de entrada usando a função [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="notes-to-transport-providers"></a>Observações para provedores de transporte

Suporte ao TNEF (Transport Neutral Encapsulation Format) e use o valor da propriedade **PR_SEND_RICH_INFO** para determinar se o TNEF deve ser usado ao transportar uma mensagem. Não oferecer suporte a TNEF ou não enviar uma mensagem nesse formato quando solicitado pode ser um problema para clientes baseados em formulário ou clientes que exigem propriedades MAPI personalizadas. Isso porque o TNEF normalmente é usado para enviar propriedades personalizadas para classes de mensagens personalizadas. 
  
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriedade canônica PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

