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
ms.openlocfilehash: fcb5486cc96403b872e07ab597545ca6f493907d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581318"
---
# <a name="saving-a-message"></a>Salvar uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de uma mensagem é salva, os clientes geralmente chamar [IMAPIProp::SetProps](imapiprop-setprops.md) método da mensagem para definir algumas propriedades além de propriedades de texto da mensagem, as propriedades de anexo, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e propriedades associado com a lista de destinatários.
  
Defina a propriedade de **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) como uma cadeia de caracteres, como IPM. Observe que descreve a classe de mensagem de saída. Embora os clientes devem definir **PR_MESSAGE_CLASS** em todas as mensagens de saída, um valor padrão é fornecido pelo provedor de armazenamento de mensagem se você não defini-la. A classe de mensagem padrão para mensagens de saída é IPM. 
  
Defina o sinalizador MSGFLAG_UNSENT na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Se desejado, defina também os sinalizadores MSGFLAG_READ e MSGFLAG_UNMODIFIED. Definir o MSGFLAG_UNMODIFIED permite que uma mensagem de composição simular uma mensagem entregue. MSGFLAG_UNMODIFIED só pode ser definida pelos clientes antes de uma mensagem foi salvo pela primeira vez. 
  
Quando você estiver pronto para fazer uma cópia permanente de uma mensagem não enviada, chame [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na mensagem e todos os seus respectivos anexos. Se você pretende enviar a mensagem imediatamente, você não precisará chamar **SaveChanges**. A chamada para **SubmitMessage** internamente salva a mensagem como parte do seu processamento. 
  
Ao chamar **SaveChanges**, é uma boa ideia para especificar o sinalizador KEEP_OPEN_READWRITE, que permite a mensagem a ser modificado mais tarde. Outros sinalizadores definíveis incluem FORCE_SAVE, que indica que a mensagem ou um anexo deve ser fechado depois que as alterações sejam confirmadas, KEEP_OPEN_READONLY, que indica que nenhuma alteração será feita, e o sinalizador para permitir que o provedor de armazenamento de mensagem para lote de solicitações de clientes, MAPI_DEFERRED_ERRORS.
  
É essencial que você chamar **SaveChanges** para cada anexo na mensagem antes de chamar **SaveChanges** da mensagem. Se você não conseguir salvar um anexo, o anexo não será incluído com a mensagem quando ele é enviado e ele não aparecerá na tabela de anexos da mensagem. Se você não conseguir salvar a mensagem depois de salvar todos os anexos, a mensagem e os anexos serão perdidos. 
  
Quando **SaveChanges** é chamado, o provedor de armazenamento de mensagem atualiza as propriedades a seguir: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) lista todos os destinatários principais.
    
- **PR_DISPLAY_TO** lista todos os destinatários de cópia carbono. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) lista todos os destinatários de cópia oculta.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** define MSGFLAG_HASATTACH se um ou mais anexos foram salvos e limpa MSGFLAG_UNMODIFIED para mostrar que a mensagem foi alterada. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contém o tamanho mais recente da mensagem.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) fornece acesso à tabela de anexo.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) fornece acesso à tabela de destinatário.
    
Algumas propriedades de mensagem são geralmente fornecidas por clientes ou provedores de serviços quando uma mensagem é criada. Se um cliente não defini-las, é do provedor de repositório de mensagem para atualizá-los no momento **que SaveChanges** é chamado. Por exemplo, se **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e as propriedades de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) uma mensagem foram definidas quando a mensagem foi criada, eles precisam não ser modificados no economizar tempo. No entanto, provedores de armazenamento de mensagem que esquecer de defini-las na criação de mensagem devem defini-los na primeira vez que **SaveChanges** é chamado. 
  
Se **SaveChanges** retornar MAPI_E_CORRUPT_DATA, pressupõem que os dados que está sendo salvos são agora perdido. Provedores de armazenamento de mensagem que usam um modelo de cliente-servidor para sua implementação podem retornar esse valor quando uma conexão de rede é perdida ou o servidor não está em execução. Antes de retornar um erro ao usuário, tente gravar e salvar os dados de uma segunda vez fazendo uma chamada para **SetProps** seguido por outra chamada para **SaveChanges**. Se os dados é armazenado em cache localmente, isso não deve ser um problema. No entanto, se não há nenhum cache local ou a segunda chamada **SaveChanges** falha, exibe um erro para alertar o usuário para o problema. 
  

