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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322397"
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
  
> no Um ponteiro para o nome de exibição do destinatário da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). O parâmetro _lpszName_ pode ser NULL. 
    
 _lpszAdrType_
  
> no Um ponteiro para o tipo de endereço (como FAX, SMTP ou X500) do destinatário. O parâmetro _lpszAdrType_ não pode ser nulo. 
    
 _lpszAddress_
  
> no Um ponteiro para o endereço de mensagens do destinatário. O parâmetro _lpszAddress_ não pode ser nulo. 
    
 _ulFlags_
  
> no Uma máscara de bits de sinalizadores que afeta o destinatário one-off. Os seguintes sinalizadores podem ser definidos:
    
MAPI_SEND_NO_RICH_INFO 
  
> O destinatário não pode lidar com o conteúdo de mensagens formatados. Se MAPI_SEND_NO_RICH_INFO for definido, MAPI definirá a propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como false. Se MAPI_SEND_NO_RICH_INFO não for definido, MAPI definirá essa propriedade como TRUE, a menos que o endereço de email do destinatário apontado por _lpszAddress_ seja interpretado como um endereço de Internet. Nesse caso, o MAPI define **PR_SEND_RICH_INFO** como false. 
    
MAPI_UNICODE 
  
> O nome de exibição, o tipo de endereço e o endereço estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estarão no formato ANSI.
    
 _lpcbEntryID_
  
> bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> bota Um ponteiro para um ponteiro para o identificador de entrada para o destinatário one-off.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada one-off foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: CreateOneOff** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços chamam o **CreateOneOff** para criar um identificador de entrada para um destinatário individual (um destinatário que não pertence a nenhum contêiner de qualquer um dos provedores de catálogos de endereços carregados no momento). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando você terminar de usar o identificador de entrada retornado por **CreateOneOff**, libere a memória alocada para o identificador de entrada usando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Observações para provedores de transporte

Dê suporte ao TNEF (Transport neutral Encapsulation Format) e use o valor da propriedade **PR_SEND_RICH_INFO** para determinar se usará TNEF quando você transportar uma mensagem. Não oferecer suporte a TNEF ou não enviar uma mensagem neste formato quando solicitado pode ser um problema para clientes baseados em formulário ou clientes que exigem propriedades MAPI personalizadas. Isso ocorre porque o TNEF geralmente é usado para enviar propriedades personalizadas para classes de mensagens personalizadas. 
  
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriedade canônica PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

