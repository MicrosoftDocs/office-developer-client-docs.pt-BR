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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408765"
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
  
> [in] Um ponteiro para a mensagem para a qual o relatório deve ser gerado.
    
 _lpRecipList_
  
> [in] Um ponteiro para uma [estrutura ADRLIST](adrlist.md) que descreve os destinatários da mensagem apontados por  _lpMessage_.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O relatório foi gerado com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida em geral, mas não há opções de destinatário para esse tipo de destinatário. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::StatusRecips** é implementado para objetos de suporte do provedor de transporte. Os provedores de transporte chamam **StatusRecips** para solicitar que o MAPI envie um relatório de entrega ou não entrega a um conjunto de um ou mais destinatários de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode chamar **StatusRecips** várias vezes durante o processamento de uma mensagem. No entanto, se você chamar **StatusRecips** para uma mensagem aberta, faça o melhor possível para coletar todas as informações de entrega e não entrega para os destinatários da mensagem e chamar **StatusRecips** para essa lista de destinatários. Um único ponto de coleta é importante, porque várias **chamadas StatusRecips** para um destinatário podem resultar em vários relatórios idênticos sendo enviados. 
  
Armazene propriedades relacionadas à entrega de mensagens ou não entrega na estrutura **ADRLIST** indicada pelo _parâmetro lpRecipList._ Para uma lista completa das propriedades opcionais e necessárias para relatórios de entrega e relatórios sem entrega, consulte [Propriedades](required-report-message-properties.md) de mensagem de relatório necessárias e propriedades opcionais de mensagem [de relatório.](optional-report-message-properties.md) 
  
Aloque memória para a estrutura **ADRLIST** em _lpRecipList_ usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore.](mapiallocatemore.md) O MAPI libera a memória chamando a [função MAPIFreeBuffer](mapifreebuffer.md) somente se **StatusRecips** tiver êxito. 
  
Para uma visão geral dos relatórios de entrega e não entrega, consulte [MAPI Report Messages](mapi-report-messages.md).
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

