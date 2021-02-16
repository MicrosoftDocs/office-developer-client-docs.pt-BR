---
title: Suporte a anexos de mensagem para provedores de armazenamento de mensagens
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
# <a name="supporting-message-attachments-for-message-store-providers"></a>Suporte a anexos de mensagem para provedores de armazenamento de mensagens

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Seu provedor de armazenamento de mensagens não precisa dar suporte a anexos de mensagens. No entanto, muitos aplicativos cliente esperam ser capazes de adicionar anexos às mensagens. Se o armazenamento de mensagens for usado para criar ou armazenar o IPM. Observe as mensagens e, em seguida, você deve dar suporte a anexos de mensagens. Os provedores de armazenamento de mensagens padrão também devem suportar anexos de mensagens. Para obter mais informações, [consulte CLASSES de mensagens MAPI](mapi-message-classes.md)e [armazenamentos de mensagens padrão.](default-message-stores.md)
  
Há cinco tipos de anexos aos quais o MAPI oferece suporte: anexos de arquivo, anexos de dados, anexos de mensagem, anexos de objeto OLE e links. Os requisitos para dar suporte a cada tipo são diferentes. Os clientes diferenciam entre os dois tipos de anexos por meio da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) em objetos anexos.
  
O suporte a anexos significa implementar a interface [IAttach : IMAPIProp.](iattachimapiprop.md) A interface **IAttach** não tem seus próprios métodos; ele tem apenas métodos que são herdados da interface [IMAPIProp.](imapipropiunknown.md) Como seu provedor de armazenamento de mensagens já deve implementar propriedades para objetos de mensagem, isso simplifica bastante a tarefa de suporte a anexos. Implementar **IAttach basicamente** significa fornecer uma maneira para os clientes acessarem uma tabela de propriedades para anexos específicos em mensagens. 
  
Os anexos de dados são simplesmente anexos para os quais o conteúdo do anexo é armazenado diretamente na propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo. Os anexos de dados existem principalmente para permitir que os clientes anexem arquivos a uma mensagem quando o remetente e o destinatário da mensagem não têm acesso a um servidor de arquivos comum. Para obter mais informações, **consulte PR_ATTACH_METHOD** propriedade ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Anexos de mensagem são anexos para os quais o subobjeto do anexo é outro [IMessage: objeto MAPIProp.](imessageimapiprop.md) Como os provedores de armazenamento de mensagens já suportam a interface **IMessage,** o suporte a anexos de mensagens não é difícil. 
  
Oferecer suporte a anexos de objeto OLE significa implementar as interfaces **OLE IStorage**, **IStream** e **IStreamDocfile.** Seu provedor de armazenamento de mensagens deve ser capaz de converter dados de objeto OLE armazenados na mensagem em um objeto OLE ativo quando um cliente abre o objeto. 
  
Os links são de dois tipos: links para arquivos e links para outras mensagens. Links para arquivos usam o valor ATTACH_BY_REF_ONLY para **a** propriedade PR_ATTACH_METHOD juntamente com **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) para especificar o local de um arquivo.
  
Como implementar links para mensagens pode depender de aspectos do sistema de mensagens local e, como tal, não pode ser totalmente documentado aqui. Por exemplo, enviar um link para uma mensagem armazenada em um armazenamento de mensagens baseado em servidor geralmente é apenas uma questão de enviar o identificador de entrada da mensagem vinculada, desde que o remetente e o destinatário tenham acesso a esse servidor. Outras configurações do sistema de mensagens apresentam outros requisitos e desafios para implementar links para mensagens.
  
## <a name="see-also"></a>Confira também



[Recursos do Armazenamento de Mensagens](message-store-features.md)

