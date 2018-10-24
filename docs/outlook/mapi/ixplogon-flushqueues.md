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
ms.openlocfilehash: 961ac2d26cd58e625c35d00bd1216cdee2ce57a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584727"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que o provedor de transporte imediatamente entrega todas as mensagens de entrada ou saídas pendentes.
  
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
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.
    
 _cbTargetTransport_
  
> [in] Reservado; deve ser zero.
    
 _lpTargetTransport_
  
> [in] Reservado; deve ser NULL.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como liberação de fila de mensagens é realizada. Sinalizadores a seguir podem ser definidos:
    
FLUSH_DOWNLOAD 
  
> A fila de mensagens de entrada ou filas devem ser liberadas.
    
FLUSH_FORCE 
  
> O provedor de transporte deve processar a solicitação, se possível, mesmo se fazer isso é demorado. 
    
FLUSH_NO_UI 
  
> O provedor de transporte não deverá exibir uma interface do usuário.
    
FLUSH_UPLOAD 
  
> A fila de mensagens de saída ou filas devem ser liberadas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método de **IXPLogon::FlushQueues** para avisar o provedor de transporte que o spooler MAPI está prestes a começar o processamento de mensagens. O provedor de transporte deve chamar o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para definir um bit apropriado para seu estado na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da sua linha de status. Depois de atualizar sua linha de status, o provedor de transporte deve retornar S_OK para a chamada **FlushQueues** . O MAPI spooler, em seguida, inicia o envio de mensagens, com a operação que está sendo sincronizada com o spooler MAPI. 
  
Para suportar sua implementação do método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , o MAPI spooler chama **IXPLogon::FlushQueues** para todos os objetos de logon para provedores de transporte ativo que estão executando em uma sessão de perfil. Quando o método de **FlushQueues** de um provedor de transporte é chamado como resultado de uma chamada do aplicativo de cliente para **IMAPIStatus::FlushQueues**, o processamento da mensagem ocorre no cliente de forma assíncrona.
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

