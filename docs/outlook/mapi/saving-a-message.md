---
title: Salvar uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d5ceeb46bded101700aec696a17d690bde80ce6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420926"
---
# <a name="saving-a-message"></a>Salvar uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de uma mensagem ser salva, os clientes normalmente chamam o método [IMAPIProp::SetProps](imapiprop-setprops.md) da mensagem para definir algumas propriedades além das propriedades de texto da mensagem, propriedades de anexo, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e propriedades associadas à lista de destinatários.
  
Definir a **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) para uma cadeia de caracteres como IPM. Observe que descreve a classe da mensagem de saída. Embora os clientes deverão **PR_MESSAGE_CLASS** em todas as mensagens de saída, um valor padrão será fornecido pelo provedor do armazenamento de mensagens se você não defini-lo. A classe de mensagem padrão para mensagens de saída é IPM. 
  
Defina MSGFLAG_UNSENT sinalizador na **propriedade PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Se desejado, de definida também as MSGFLAG_READ e MSGFLAG_UNMODIFIED sinalizadores. Definir o MSGFLAG_UNMODIFIED permite que uma mensagem em composição simule uma mensagem entregue. MSGFLAG_UNMODIFIED pode ser definida apenas por clientes antes que uma mensagem seja salva pela primeira vez. 
  
Quando estiver pronto para fazer uma cópia permanente de uma mensagem não enviada, chame [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sobre a mensagem e todos os seus anexos. Se você pretende enviar a mensagem imediatamente, não é necessário chamar **SaveChanges**. A chamada para **SubmitMessage** salva internamente a mensagem como parte de seu processamento. 
  
Ao chamar **SaveChanges,** é uma boa ideia especificar o sinalizador KEEP_OPEN_READWRITE, que permite que a mensagem seja modificada posteriormente. Outros sinalizadores de tabela de definição incluem FORCE_SAVE, que indica que a mensagem ou anexo deve ser fechado depois que as alterações são comprometidas, KEEP_OPEN_READONLY, o que indica que nenhuma outra alteração será feita e o sinalizador para permitir que o provedor de armazenamento de mensagens lote solicitações de cliente, MAPI_DEFERRED_ERRORS.
  
É essencial que você chame **SaveChanges para** cada anexo na mensagem antes de chamar **SaveChanges** para a mensagem. Se você não conseguir salvar um anexo, ele não será incluído na mensagem quando for enviado e não aparecerá na tabela de anexos da mensagem. Se você não conseguir salvar a mensagem depois de salvar todos os anexos, a mensagem e os anexos serão perdidos. 
  
Quando **SaveChanges é** chamado, o provedor de armazenamento de mensagens atualiza as seguintes propriedades: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) lista todos os destinatários principais.
    
- **PR_DISPLAY_TO** lista todos os destinatários de cópia carbono. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) lista todos os destinatários com cópia carbono.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** define MSGFLAG_HASATTACH se um ou mais anexos foram salvos e limpa MSGFLAG_UNMODIFIED para mostrar que a mensagem foi alterada. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contém o tamanho mais atual da mensagem.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) fornece acesso à tabela de anexos.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) fornece acesso à tabela de destinatários.
    
Algumas propriedades de mensagem geralmente são fornecidas por clientes ou provedores de serviços quando uma mensagem é criada. Se um cliente se esquecer de defini-los, o provedor de armazenamento de mensagens deve atualizá-lo no momento em que **SaveChanges** for chamado. Por exemplo, se as propriedades **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) de uma mensagem foram definidas quando a mensagem foi criada, elas não precisam ser modificadas no momento da gravação. No entanto, os provedores de armazenamento de mensagens que não os definirem na criação da mensagem devem defini-los na primeira vez que **SaveChanges** for chamado. 
  
Se **SaveChanges** retornar MAPI_E_CORRUPT_DATA, suponha que os dados que estão sendo salvos agora foram perdidos. Provedores de armazenamento de mensagens que usam um modelo cliente-servidor para sua implementação podem retornar esse valor quando uma conexão de rede é perdida ou o servidor não está em execução. Antes de retornar um erro para o usuário, tente gravar e salvar os dados uma segunda vez fazendo uma chamada para **SetProps** seguido por outra chamada para **SaveChanges**. Se os dados são armazenados em cache localmente, isso não deve ser um problema. No entanto, se não houver cache local ou a segunda chamada **SaveChanges** falhar, exibirá um erro para alertar o usuário sobre o problema. 
  

