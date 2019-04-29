---
title: Suporte a anexos de mensagens para provedores de repositórios de mensagens
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412132"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Suporte a anexos de mensagens para provedores de repositórios de mensagens

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O seu provedor de repositório de mensagens não precisa dar suporte a anexos de mensagens. No enTanto, muitos aplicativos cliente esperam ser capazes de adicionar anexos a mensagens. Se o repositório de mensagens for usado para criar ou armazenar IPM. Observação mensagens, então você deve dar suporte a anexos de mensagens. Os provedores de repositórios de mensagens padrão também devem oferecer suporte a anexos de mensagens. Para obter mais informações, consulte [MAPI Message classes](mapi-message-classes.md)e [Default Message Stores](default-message-stores.md).
  
Há cinco tipos de anexos que o MAPI suporta: anexos de arquivo, anexos de dados, anexos de mensagem, anexos de objeto OLE e links. Os requisitos para suporte a cada tipo são diferentes. Os clientes diferenciam entre os dois tipos de anexos por meio da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) em objetos Attachment.
  
Os anexos de suporte significam a implementação da interface [IAttach: IMAPIProp](iattachimapiprop.md) . A interface **IAttach** não tem métodos próprios; Ele tem apenas métodos herdados da interface [IMAPIProp](imapipropiunknown.md) . Como o seu provedor de repositório de mensagens já deve implementar propriedades para objetos de mensagem, isso simplifica muito a tarefa de suporte a anexos. Implementar o **IAttach** basicamente significa fornecer uma maneira de os clientes acessarem uma tabela de propriedades para determinados anexos em mensagens. 
  
Os anexos de dados são apenas anexos para os quais o conteúdo do anexo é armazenado diretamente na propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo. Os anexos de dados existem principalmente para permitir que os clientes anexem arquivos a uma mensagem quando o remetente e o destinatário da mensagem não têm acesso a um servidor de arquivos comum. Para obter mais informações, consulte a propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Os anexos de mensagem são anexos para os quais o subobjeto Attachment é outro objeto [IMessage: MAPIProp](imessageimapiprop.md) . Como os provedores de repositórios de mensagens já dão suporte à interface **IMessage** , os anexos de mensagens de suporte não são difíceis. 
  
O suporte a anexos de objeto OLE significa implementar as interfaces OLE **IStorage**, **IStream**e **IStreamDocfile** . Seu provedor de repositório de mensagens deve ser capaz de converter dados de objeto OLE armazenados na mensagem em um objeto OLE ativo quando um cliente abre o objeto. 
  
Os links têm dois tipos: links para arquivos e links para outras mensagens. Links para arquivos usam o valor ATTACH_BY_REF_ONLY para a propriedade **PR_ATTACH_METHOD** junto com **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) para especificar o local de um arquivo.
  
O modo como um implementa links para mensagens pode depender de aspectos do sistema de mensagens local e, como tal, não pode ser totalmente documentado aqui. Por exemplo, enviar um link para uma mensagem armazenada em um repositório de mensagens baseado em servidor é normalmente apenas uma questão de enviar o identificador de entrada da mensagem vinculada, permitindo que tanto o remetente quanto o destinatário tenham acesso a esse servidor. Outras configurações do sistema de mensagens apresentam outros requisitos e desafios para a implementação de links para mensagens.
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

