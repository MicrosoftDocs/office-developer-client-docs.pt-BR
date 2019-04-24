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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282828"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que o provedor de transporte entregue imediatamente todas as mensagens pendentes de entrada ou saída.
  
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
  
> no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _cbTargetTransport_
  
> no Serve deve ser zero.
    
 _lpTargetTransport_
  
> no Serve deve ser nulo.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam como a liberação da fila de mensagens é realizada. Os seguintes sinalizadores podem ser definidos:
    
FLUSH_DOWNLOAD 
  
> A fila de mensagens de entrada ou filas deve ser liberada.
    
FLUSH_FORCE 
  
> O provedor de transporte deve processar essa solicitação, se possível, mesmo que isso seja um tempo demorado. 
    
FLUSH_NO_UI 
  
> O provedor de transporte não deve exibir uma interface de usuário.
    
FLUSH_UPLOAD 
  
> A fila de mensagens de saída ou filas devem ser liberadas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon:: FlushQueues** para informar ao provedor de transporte que o spooler MAPI está prestes a iniciar o processamento de mensagens. O provedor de transporte deve chamar o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para definir um bit apropriado para seu estado na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sua linha de status. Depois de atualizar sua linha de status, o provedor de transporte deve retornar S_OK para a chamada **FlushQueues** . O spooler MAPI, em seguida, inicia o envio de mensagens, com a operação síncrona para o spooler MAPI. 
  
Para dar suporte à sua implementação do método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) , o spooler MAPI chama **IXPLogon:: FlushQueues** para todos os objetos de logon para provedores de transporte ativos que estão sendo executados em uma sessão de perfil. Quando um método **FlushQueues** do provedor de transporte é chamado como resultado de uma chamada de aplicativo cliente para **IMAPIStatus:: FlushQueues**, o processamento da mensagem ocorre de forma assíncrona com o cliente.
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

