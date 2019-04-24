---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341766"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gera relatórios de entrega e não entrega.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> no Um ponteiro para a mensagem para a qual o relatório deve ser gerado.
    
 _lpRecipList_
  
> no Um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que descreve os destinatários da mensagem indicada por _lpMessage_.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O relatório foi gerado com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi concluída de modo geral, mas não há opções de destinatário para esse tipo de destinatário. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: StatusRecips** é implementado para objetos de suporte do provedor de transporte. Os provedores de transporte chamam o **StatusRecips** para solicitar que o MAPI envie um relatório de entrega ou de não-entrega para um conjunto de um ou mais destinatários de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode chamar **StatusRecips** várias vezes durante o processamento de uma mensagem. No enTanto, se você chamar **StatusRecips** para uma mensagem aberta, faça o melhor para coletar todas as informações de entrega e de não entrega para os destinatários da mensagem e chame **StatusRecips** para essa lista de destinatários. Um único ponto de coleção é importante, porque várias chamadas **StatusRecips** para um destinatário podem resultar em vários relatórios idênticos sendo enviados. 
  
Armazenar propriedades relacionadas à entrega de mensagens ou à não entrega na estrutura **das ADRLIST** indicada pelo parâmetro _lpRecipList_ . Para obter uma lista completa de propriedades obrigatórias e opcionais para relatórios de entrega e relatórios de não-entrega, consulte [Required Report Message Properties](required-report-message-properties.md) e [optional Report Message Properties](optional-report-message-properties.md). 
  
Alocar memória para a estrutura **das ADRLIST** no _lpRecipList_ usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) . MAPI libera a memória chamando a função [MAPIFreeBuffer](mapifreebuffer.md) somente se o **StatusRecips** for bem-sucedido. 
  
Para obter uma visão geral de relatórios de entrega e não entrega, consulte [MAPI Report messages](mapi-report-messages.md).
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

