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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283118"
---
# <a name="saving-a-message"></a>Salvar uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de uma mensagem ser salva, os clientes normalmente chamam o método [IMAPIProp::](imapiprop-setprops.md) SetProps da mensagem para definir algumas propriedades além das propriedades do texto da mensagem, das propriedades do anexo, do **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e das propriedades associado à lista de destinatários.
  
Defina a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) como uma cadeia de caracteres como IPM. Observe que descreve a classe da mensagem de saída. Embora os clientes devam definir **PR_MESSAGE_CLASS** em todas as mensagens de saída, um valor padrão é fornecido pelo provedor de armazenamento de mensagens se você não defini-lo. A classe de mensagem padrão para mensagens de saída é IPM. 
  
Defina o sinalizador MSGFLAG_UNSENT na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Se desejar, defina também os sinalizadores MSGFLAG_READ e MSGFLAG_UNMODIFIED. A configuração do MSGFLAG_UNMODIFIED permite uma mensagem em composição para simular uma mensagem entregue. O MSGFLAG_UNMODIFIED só pode ser definido por clientes antes de uma mensagem ser salva pela primeira vez. 
  
Quando estiver pronto para fazer uma cópia permanente de uma mensagem não enviada, chame [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) na mensagem e em todos os seus anexos. Se você pretende enviar a mensagem imediatamente, não é necessário chamar **SaveChanges**. A chamada ao **SubmitMessage** internamente salva a mensagem como parte de seu processamento. 
  
Ao chamar o **SaveChanges**, é uma boa ideia especificar o sinalizador KEEP_OPEN_READWRITE, que permite que a mensagem seja modificada mais tarde. Outros sinalizadores settable incluem FORCE_SAVE, que indica que a mensagem ou o anexo deve ser fechado depois que as alterações são confirmadas, KEEP_OPEN_READONLY, que indica que nenhuma outra alteração será feita e o sinalizador para permitir que o provedor de repositório de mensagens solicitações de clientes em lote, MAPI_DEFERRED_ERRORS.
  
É essencial que você chame **SaveChanges** para cada anexo da mensagem antes de chamar **SaveChanges** para a mensagem. Se você não salvar um anexo, o anexo não será incluído na mensagem quando ele for enviado e não será exibido na tabela de anexos da mensagem. Se você não salvar a mensagem após salvar todos os anexos, a mensagem e os anexos serão perdidos. 
  
Quando **SaveChanges** é chamado, o provedor de armazenamento de mensagens atualiza as seguintes propriedades: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) lista todos os destinatários primários.
    
- **PR_DISPLAY_TO** lista todos os destinatários de cópia carbono. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) lista todos os destinatários de cópia oculta.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** define MSGFLAG_HASATTACH se um ou mais anexos foram salvos e limpa o MSGFLAG_UNMODIFIED para mostrar que a mensagem foi alterada. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contém o tamanho mais atual da mensagem.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) fornece acesso à tabela de anexos.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) fornece acesso à tabela de destinatários.
    
Algumas propriedades de mensagem são geralmente fornecidas por clientes ou provedores de serviços quando uma mensagem é criada. Se um cliente ficar inativo para defini-los, ele estará no provedor de armazenamento de mensagens para atualizá-los no momento em que **SaveChanges** for chamado. Por exemplo, se as propriedades de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) da mensagem foram definidas quando a mensagem foi criada, elas não precisam ser modificadas no momento da gravação. No enTanto, os provedores de repositórios de mensagens que negligenciam defini-los na criação de mensagens devem defini-los pela primeira vez que **SaveChanges** for chamado. 
  
Se **SaveChanges** retornar MAPI_E_CORRUPT_DATA, presuma que os dados que estão sendo salvos serão perdidos. Os provedores de repositório de mensagens que usam um modelo de servidor cliente para sua implementação podem retornar esse valor quando uma conexão de rede é perdida ou o servidor não está em execução. Antes de retornar um erro ao usuário, tente gravar e salvar os dados uma segunda vez fazendo uma chamada para setProps seguida de outra chamada para **SaveChanges**. **** Se os dados são armazenados em cache localmente, isso não deve ser um problema. No enTanto, se não houver cache local ou a segunda chamada **SaveChanges** falhar, exibirá um erro para alertar o usuário sobre o problema. 
  

