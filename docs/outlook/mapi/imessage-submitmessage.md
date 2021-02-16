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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437361"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Salva todas as propriedades da mensagem e marca a mensagem como pronta para ser enviada.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Bitmask de sinalizadores usados para controlar como uma mensagem é enviada. O sinalizador a seguir pode ser definido:
    
FORCE_SUBMIT 
  
> O MAPI deve enviar a mensagem imediatamente. Esse sinalizador não está em uso no momento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NO_RECIPIENTS 
  
> A tabela de destinatários da mensagem está vazia.
    
## <a name="remarks"></a>Comentários

O **método IMessage::SubmitMessage** marca uma mensagem como pronta para ser transmitida. O MAPI passa mensagens para o sistema de mensagens subjacente na ordem em que são marcadas para envio. Devido a essa funcionalidade, uma mensagem pode permanecer em um armazenamento de mensagens por algum tempo antes que o sistema de mensagens subjacente possa assumir a responsabilidade por ela. A ordem de recebimento no destino está no controle do sistema de mensagens subjacente e não necessariamente corresponder à ordem na qual as mensagens foram enviadas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Chame o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem para salvá-la e verifique a propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem. Se o MSGFLAG_RESEND sinalizador estiver definido, chame [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** atualiza o tipo de destinatário **e** PR_RESPONSIBILITY ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos os destinatários na mensagem de reemissão.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **SubmitMessage** retorna, todos os ponteiros para a mensagem e suas mensagens, pastas, anexos, fluxos, tabelas e assim por diante associados não são mais válidos. MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods. O MAPI foi projetado de forma que, depois **que SubmitMessage** for chamado, você deverá liberar a mensagem e todos os subobjetos associados. No entanto, se **SubmitMessage** retornar um valor de erro indicando informações ausentes ou inválidas, a mensagem permanecerá aberta e os ponteiros permanecerão válidos. 
  
Para cancelar uma operação de envio, obter e armazenar um ponteiro para a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem antes de a mensagem ser enviada. Como o identificador de entrada de uma mensagem é invalidado após o envio da mensagem, é necessário salvá-la antes de chamar **SubmitMessage**. Para cancelar o envio, aponte o parâmetro  _lpEntryId_ para esse identificador de entrada e chame [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI usa o **método IMessage::SubmitMessage** para enviar a mensagem selecionada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

