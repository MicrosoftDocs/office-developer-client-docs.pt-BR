---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425320"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gera um relatório lido ou não lido para uma mensagem.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o relatório lido ou não lido é gerado. O sinalizador a seguir pode ser definido:
    
MAPI_NON_READ 
  
> Um relatório não lido é gerado. Se MAPI_NON_READ não estiver definido, será gerado um relatório de leitura.
    
 _lpReadMessage_
  
> [in] Um ponteiro para a mensagem sobre a qual o relatório deve ser gerado.
    
 _lppEmptyMessage_
  
> [in, out] Na entrada,  _lppEmptyMessage_ aponta para um ponteiro para uma mensagem vazia. Na saída,  _lppEmptyMessage_ aponta para um ponteiro para a mensagem de relatório. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O relatório foi gerado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::ReadReceipt** é implementado somente para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens chamam **ReadReceipt** para instruir o MAPI a gerar um relatório lido ou não lido para a mensagem apontada pelo _parâmetro lpReadMessage._ 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **ReadReceipt** quando a **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida e uma das seguintes condições for verdadeira:
  
- A mensagem foi lida.
    
- A mensagem foi movida.
    
- A mensagem foi copiada.
    
- O método [IMessage::SetReadFlag](imessage-setreadflag.md) da mensagem foi chamado. 
    
Não chame **ReadReceipt** quando uma mensagem for excluída. 
  
Um relatório lido ou não lido deve ser enviado apenas uma vez para uma mensagem. Acompanhe o status de leitura de uma mensagem e não envie vários relatórios para uma única mensagem.
  
Se o parâmetro _lppEmptyMessage_ aponta para uma mensagem de relatório válida quando MAPI retorna de **ReadReceipt**, chame o método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar a mensagem e liberar o ponteiro chamando seu método **IUnknown:s:Release.** 
  
Se **ReadReceipt** falhar, a mensagem deverá ser liberada sem ser enviada. Se você armazenar o status de leitura da mensagem, poderá tentar gerar o relatório lido ou não lido posteriormente. 
  
Você pode ocultar ou exibir relatórios lidos e não lidos gerados por armazenamentos em suas pastas. Armazenar relatórios lidos e não lidos em pastas ocultas permite implementar uma segurança mais rígida.
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propriedade canônica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

