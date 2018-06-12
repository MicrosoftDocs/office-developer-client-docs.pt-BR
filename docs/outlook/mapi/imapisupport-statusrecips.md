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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f3642c890c3922611d57dea6f03aca5606876864
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767307"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Aplica-se a**: Outlook 
  
Gera os relatórios de entrega e de não entrega.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Par�metros

 _lpMessage_
  
> [in] Um ponteiro para a mensagem para o qual o relatório deve ser gerado.
    
 _lpRecipList_
  
> [in] Um ponteiro para uma estrutura [ADRLIST](adrlist.md) que descreve os destinatários da mensagem apontado pela _lpMessage_.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O relatório foi gerado com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> Chamada bem-sucedida, mas não existem opções destinatários para esse tipo de destinatário. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::StatusRecips** é implementado para objetos de suporte do provedor de transporte. Provedores de transporte chamarem **StatusRecips** para solicitar que enviam MAPI em um relatório de entrega ou não entrega a um conjunto de um ou mais dos destinatários de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

É possível chamar **StatusRecips** várias vezes durante o processamento de uma mensagem. No entanto, se você chamar **StatusRecips** para uma mensagem aberta, fazer o melhor para coletar todas as informações de entrega e de não entrega para os destinatários da mensagem e chame **StatusRecips** para essa lista de destinatários. Um único ponto de conjunto é importante, porque várias chamadas **StatusRecips** para um destinatário podem resultar em vários relatórios idênticos que estão sendo enviados. 
  
Armazena propriedades relacionadas a entrega da mensagem ou não de entrega na estrutura **ADRLIST** indicada pelo parâmetro _lpRecipList_ . Para obter uma lista completa de propriedades obrigatórios e opcionais de relatórios de entrega e NDRs, consulte [Propriedades de mensagem de relatório necessárias](required-report-message-properties.md) e [Propriedades de mensagem opcional do relatório](optional-report-message-properties.md). 
  
Alocar memória para a estrutura **ADRLIST** no _lpRecipList_ usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) . MAPI libera a memória chamando-se a função [MAPIFreeBuffer](mapifreebuffer.md) somente se **StatusRecips** for bem-sucedido. 
  
Para obter uma visão geral dos relatórios de entrega e de não entrega, consulte [As mensagens de relatório de MAPI](mapi-report-messages.md).
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

