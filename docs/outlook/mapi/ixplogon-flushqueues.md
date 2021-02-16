---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421967"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que o provedor de transporte entregue imediatamente todas as mensagens de entrada ou de saída pendentes.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _cbTargetTransport_
  
> [in] Reservado; deve ser zero.
    
 _lpTargetTransport_
  
> [in] Reservado; deve ser NULL.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a liberação da fila de mensagens é realizada. Os sinalizadores a seguir podem ser definidos:
    
FLUSH_DOWNLOAD 
  
> A fila ou filas de mensagens de entrada devem ser liberados.
    
FLUSH_FORCE 
  
> O provedor de transporte deve processar essa solicitação, se possível, mesmo que isso seja demorado. 
    
FLUSH_NO_UI 
  
> O provedor de transporte não deve exibir uma interface do usuário.
    
FLUSH_UPLOAD 
  
> A fila ou filas de mensagens de saída devem ser liberados.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon::FlushQueues** para avisar o provedor de transporte de que o spooler MAPI está prestes a começar o processamento de mensagens. O provedor de transporte deve chamar o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para definir um bit apropriado para seu estado na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sua linha de status. Depois de atualizar sua linha de status, o provedor de transporte deve retornar S_OK para a **chamada FlushQueues.** Em seguida, o spooler MAPI começa a enviar mensagens, com a operação sendo síncrona para o spooler MAPI. 
  
Para dar suporte à implementação do método [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) o spooler MAPI chama **IXPLogon::FlushQueues** para todos os objetos de logon para provedores de transporte ativos que estão sendo executados em uma sessão de perfil. Quando o método **FlushQueues** de um provedor de transporte é chamado como resultado de uma chamada de aplicativo cliente para **IMAPIStatus::FlushQueues**, o processamento da mensagem ocorre de forma assíncrona para o cliente.
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

