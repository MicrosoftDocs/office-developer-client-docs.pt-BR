---
title: Anexos de mensagens de suporte para provedores de armazenamento de mensagens
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: e3d6844f8fe6121d6ea063a9594aaf1fed581ee5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770521"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Anexos de mensagens de suporte para provedores de armazenamento de mensagens

 
  
**Aplica-se a**: Outlook 
  
Seu provedor de armazenamento de mensagem não precisa suportar anexos de mensagens. No entanto, muitos aplicativos de cliente esperam poder adicionar anexos de mensagens. Se o armazenamento de mensagens será usado para criar ou armazenar IPM. Observe as mensagens, e em seguida, você deve dar suporte a anexos de mensagens. Provedores de armazenamento de mensagem padrão também devem oferecer suporte a anexos de mensagens. Para obter mais informações, consulte [Classes de mensagem MAPI](mapi-message-classes.md)e [Armazenamentos de mensagem padrão](default-message-stores.md).
  
Há cinco tipos de anexos que ofereça suporte a MAPI: anexos, anexos de dados, anexos de mensagens, os anexos de objeto OLE e links de arquivo. Os requisitos para cada tipo de suporte são diferentes. Clientes diferenciam entre os dois tipos de anexos por meio da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) em objetos de anexo.
  
Suporte de anexos significa Implementando o [IAttach: IMAPIProp](iattachimapiprop.md) interface. A interface **IAttach** não possui métodos da própria; tem apenas os métodos que são herdados da interface [IMAPIProp](imapipropiunknown.md) . Porque seu provedor de armazenamento de mensagem já deve implementar as propriedades de objetos de mensagem, isso simplifica bastante a tarefa de suportar anexos. Implementar **IAttach** basicamente significa fornecendo uma maneira para os clientes acessar uma tabela de propriedades de anexos em mensagens, em particular. 
  
Anexos de dados são simplesmente anexos para o qual o conteúdo do anexo é armazenado diretamente na propriedade de **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo. Anexos de dados existem principalmente para permitir que clientes anexar arquivos a uma mensagem quando o remetente e o destinatário da mensagem não têm acesso a um servidor de arquivos comuns. Para obter mais informações, consulte a propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Anexos de mensagens são anexos para o qual o subobjeto anexo é outra [IMessage: MAPIProp](imessageimapiprop.md) objeto. Como provedores de armazenamento de mensagem já oferecem suporte a interface **IMessage** , anexos de mensagens de suporte não é difícil. 
  
Suporte a anexos de objeto OLE significa implementar as interfaces OLE **IStorage**e **IStream** **IStreamDocfile** . Seu provedor de armazenamento de mensagem deve ser capaz de converter armazenados na mensagem em um objeto OLE ativo quando um cliente abre o objeto de dados de objeto OLE. 
  
Links são fornecidos em dois tipos: links para arquivos e links para outras mensagens. Links para arquivos usam o valor ATTACH_BY_REF_ONLY para a propriedade **PR_ATTACH_METHOD** juntamente com **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) para especificar o local de um arquivo.
  
Como um implementa links para mensagens pode depender aspectos do sistema de mensagens local e, como tal, não pode ser totalmente documentada aqui. Por exemplo, enviando um link para uma mensagem que é armazenada em um repositório de mensagens baseado em servidor geralmente é apenas uma questão de enviar o identificador de entrada da mensagem vinculado, fornecendo que o remetente e o destinatário tenham acesso a esse servidor. Outras configurações do sistema de mensagens apresentam outros requisitos e desafios para a implementação de links para as mensagens.
  
## <a name="see-also"></a>Confira também



[Recursos de armazenamento de mensagens](message-store-features.md)

