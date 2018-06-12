---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1d325c67c836e727d8285bd2dceecf88bf68327c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767392"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Aplica-se a**: Outlook 
  
Salva todas as propriedades da mensagem e marca a mensagem como pronta para ser enviada.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores usadas para controlar como uma mensagem é enviada. O seguinte sinalizador pode ser definido:
    
FORCE_SUBMIT 
  
> MAPI deve enviar a mensagem imediatamente. Esse sinalizador não está atualmente em uso.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_RECIPIENTS 
  
> Tabela de destinatário da mensagem está vazia.
    
## <a name="remarks"></a>Coment�rios

O método **IMessage::SubmitMessage** marca uma mensagem como pronto para ser transmitidos. MAPI passa mensagens para o sistema de mensagens subjacente na ordem em que estão marcados para envio. Devido a essa funcionalidade, uma mensagem pode ficar em um armazenamento de mensagens, por algum tempo antes que o sistema de mensagens subjacente pode assumir a responsabilidade para ele. A ordem de recebimento no destino está no controle do sistema de mensagens subjacentes e não necessariamente correspondem a ordem na qual as mensagens foram enviadas. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem para salvá-lo e, em seguida, verifique a propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem. Se o sinalizador MSGFLAG_RESEND estiver definido, chame [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** atualiza o tipo de destinatário e a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos os destinatários da mensagem de reenvio.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **SubmitMessage** retorna, todos os ponteiros para a mensagem e suas mensagens associadas subobjetos, pastas, anexos, fluxos, tabelas e assim por diante não estão mais válidos. MAPI não permite que quaisquer operações mais sobre esses ponteiros, exceto para chamar seus métodos **IUnknown:: Release** . MAPI destina-se a forma que depois é chamado **SubmitMessage** , você deve liberar a mensagem e todos os respectivos subobjetos. No entanto, se **SubmitMessage** retorna um valor de erro indicando informações ausentes ou inválidas, a mensagem permanecerá aberta e os ponteiros permanecem válidos. 
  
Para cancelar uma operação de envio, obtenha e armazenar um ponteiro para a propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem antes que a mensagem é enviada. Porque o identificador de entrada da mensagem é invalidado depois que a mensagem foi enviada, é necessário para salvá-lo antes de chamar **SubmitMessage**. Para cancelar a enviar, aponte o parâmetro _lpEntryId_ para esse identificador de entrada e chamadas [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI usa o método **IMessage::SubmitMessage** para enviar a mensagem selecionada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

