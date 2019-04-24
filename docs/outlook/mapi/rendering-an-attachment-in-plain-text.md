---
title: Renderizar um anexo em texto sem formatação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328354"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Renderizar um anexo em texto sem formatação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para renderizar um anexo em uma mensagem com texto sem formatação, recupere a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) do anexo e aplique-a aos dados no **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) Propriedades. Há duas maneiras de recuperar o **PR_RENDERING_POSITION**:
  
- Abra o anexo chamando o método **IMessage:: OpenAttach** da mensagem e, em seguida, solicite a propriedade **PR_RENDERING_POSITION** chamando o método **IMAPIProp::** GetProps do anexo. Para obter mais informações, consulte [IMessage:: OpenAttach](imessage-openattach.md) e [IMAPIProp::](imapiprop-getprops.md)GetProps.
    
- Chame o método **IMessage::** GetAttachmentTable da mensagem para acessar sua tabela de anexos e recuperar a coluna que contém a propriedade **PR_RENDERING_POSITION** . Dessa forma é sempre preferível. Para obter mais informações, consulte [IMessage::](imessage-getattachmenttable.md)GetAttachmentTable.
    
Tenha em mente que muitos repositórios de mensagens com reconhecimento de RTF não calculam **PR_RENDERING_POSITION** até que um cliente solicite a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de uma mensagem. Até esse momento, **PR_RENDERING_POSITION** geralmente representa um valor aproximado. Os provedores de repositórios de mensagens têm permissão para fornecer aos clientes um valor aproximado para melhorar o desempenho. 
  
O processamento para um arquivo ou anexo binário é armazenado em sua propriedade **PR_ATTACH_RENDERING** . Você tem a opção de recuperar o **PR_ATTACH_RENDERING** da mesma maneira que você recuperou **PR_RENDERING_POSITION**: diretamente do anexo ou da tabela de anexos. Para o **PR_ATTACH_RENDERING**, a primeira estratégia, embora mais demorada, é mais segura. Como alguns provedores de repositório de mensagens truncam suas colunas da tabela para 255 bytes, ou em alguns casos 510 bytes, é difícil garantir que a coluna **PR_ATTACH_RENDERING** contenha a renderização completa. Ao recuperar a propriedade diretamente do anexo, ela sempre estará concluída. 
  
Nenhum anexo OLE e de mensagem definiu **PR_ATTACH_RENDERING**. Em vez disso, as informações de renderização de anexos OLE 1 são armazenadas no fluxo de texto da mensagem. Para anexos OLE 2, ele é armazenado em um fluxo de filho especial do objeto de armazenamento. As informações de renderização para anexos de mensagens estão disponíveis por meio do Gerenciador de formulários. 
  
 **Para recuperar o processamento de um anexo de mensagem**
  
1. Use a classe de mensagem da mensagem para acessar o Gerenciador de formulários.
    
2. Acessar a propriedade **PR_MINI_ICON** do Gerenciador de formulários. Para obter mais informações, consulte **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

