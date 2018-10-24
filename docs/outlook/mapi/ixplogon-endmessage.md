---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582466"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informa o provedor de transporte que o MAPI spooler concluído seu processamento em uma mensagem de saída.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulMsgRef_
  
> [in] Um valor de referência de mensagem específicos que foi obtido em uma chamada anterior para o método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . 
    
 _lpulFlags_
  
> [out] Uma bitmask dos sinalizadores que indica o MAPI spooler o que ele deve fazer com a mensagem. Se nenhum sinalizador estiverem definidas, a mensagem foi enviada. Sinalizadores a seguir podem ser definidos:
    
END_DONT_RESEND 
  
> O provedor de transporte tem todas as informações necessárias sobre essa mensagem por enquanto. Quando o provedor de transporte requer mais informações ou ele enviou a mensagem, ela notifica o MAPI spooler chamando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED e passando o identificador de entrada da mensagem. 
    
END_RESEND_LATER 
  
> O provedor de transporte não está enviando a mensagem na hora atual por motivos que não sejam condições de erro. O provedor de transporte deve ser chamado novamente mais tarde para enviar a mensagem.
    
END_RESEND_NOW 
  
> O provedor de transporte precisa reiniciar a mensagem passada em uma chamada de método [IMessage::SubmitMessage](imessage-submitmessage.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método de **IXPLogon::EndMessage** após ele concluir o processamento envolvidos no fornecimento de entrega estendida ou informações de não entrega. 
  
Depois que essa chamada retorna, o valor no parâmetro _ulMsgRef_ não é válido para esta mensagem. O provedor de transporte pode reutilizar o mesmo valor em uma mensagem de futuro. 
  
Todos os objetos que o provedor de transporte abre durante a transferência de uma mensagem devem ser liberados antes dos retornos de chamada **EndMessage** , com exceção do objeto de mensagem que o MAPI spooler passa para o provedor de transporte. O objeto de mensagem passado pelo spooler MAPI é inválido após a chamada **EndMessage** . 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

