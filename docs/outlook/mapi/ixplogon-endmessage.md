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
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414155"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informa ao provedor de transporte que o spooler MAPI concluiu o processamento em uma mensagem de saída.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulMsgRef_
  
> [in] Um valor de referência específico da mensagem que foi obtido em uma chamada anterior para o [método IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) 
    
 _lpulFlags_
  
> [out] Uma máscara de bits de sinalizadores que indica ao spooler MAPI o que ele deve fazer com a mensagem. Se nenhum sinalizador estiver definido, a mensagem foi enviada. Os sinalizadores a seguir podem ser definidos:
    
END_DONT_RESEND 
  
> O provedor de transporte tem todas as informações necessárias sobre essa mensagem por enquanto. Quando o provedor de transporte exige mais informações ou quando ela envia a mensagem, ele notifica o spooler MAPI chamando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) com o sinalizador NOTIFY_SENTDEFERRED e passando o identificador de entrada da mensagem. 
    
END_RESEND_LATER 
  
> O provedor de transporte não está enviando a mensagem no momento por motivos que não são condições de erro. O provedor de transporte deve ser chamado novamente mais tarde para enviar a mensagem.
    
END_RESEND_NOW 
  
> O provedor de transporte precisa reiniciar a mensagem passada para ele em uma chamada de método [IMessage::SubmitMessage.](imessage-submitmessage.md) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon::EndMessage** depois de concluir o processamento envolvido no fornecimento de informações de entrega estendida ou não entrega. 
  
Depois que essa chamada retorna, o valor no  _parâmetro ulMsgRef_ não é mais válido para essa mensagem. O provedor de transporte pode reutilizar o mesmo valor em uma mensagem futura. 
  
Todos os objetos que o provedor de transporte abre durante a transferência de uma mensagem devem ser liberados antes que a chamada **EndMessage** retorne, com exceção do objeto de mensagem que o spooler MAPI passa para o provedor de transporte. O objeto de mensagem passado pelo spooler MAPI é inválido após a **chamada EndMessage.** 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

