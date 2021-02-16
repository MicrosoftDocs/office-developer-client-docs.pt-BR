---
title: Renderização de um anexo em texto sem texto simples
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410872"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Renderização de um anexo em texto sem texto simples

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para renderizar um anexo em uma mensagem com texto sem texto, recupere a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) do anexo e aplique-o aos dados na propriedade **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)). Há duas maneiras de **recuperar** PR_RENDERING_POSITION:
  
- Abra o anexo chamando o método **IMessage::OpenAttach** da mensagem e, em **seguida,** peça a propriedade PR_RENDERING_POSITION chamando o método **IMAPIProp::GetProps** do anexo. Para obter mais informações, consulte [IMessage::OpenAttach](imessage-openattach.md) e [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Chame o método **IMessage::GetAttachmentTable** da mensagem para acessar sua tabela de anexos e recuperar a coluna que contém a **PR_RENDERING_POSITION** propriedade. Dessa forma, é sempre preferível. Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Tenha em mente que muitos armazenamentos de  mensagens com conhecimento de RTF não calculam PR_RENDERING_POSITION até que um cliente solicita a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de uma mensagem. Até esse momento, **PR_RENDERING_POSITION** geralmente representa um valor aproximado. Os provedores de armazenamento de mensagens têm permissão para fornecer aos clientes um valor aproximado para melhorar o desempenho. 
  
A renderização de um arquivo ou anexo binário é armazenada em sua **PR_ATTACH_RENDERING** propriedade. Você tem a opção de  recuperar PR_ATTACH_RENDERING da mesma maneira que recuperou PR_RENDERING_POSITION **:** diretamente do anexo ou da tabela de anexos. Por **PR_ATTACH_RENDERING**, a primeira estratégia, embora mais demorada, é mais segura. Como alguns provedores de armazenamento de mensagens truncam suas colunas de tabela em 255 bytes ou, em alguns casos, 510 bytes, é difícil ter certeza de que a coluna **PR_ATTACH_RENDERING** contém a renderização completa. Ao recuperar a propriedade diretamente do anexo, ela sempre será concluída. 
  
Nem anexos de mensagem nem OLE definidos **PR_ATTACH_RENDERING**. Em vez disso, as informações de renderização para anexos OLE 1 são armazenadas no fluxo de texto da mensagem. Para anexos OLE 2, ele é armazenado em um fluxo filho especial do objeto de armazenamento. Informações de renderização para anexos de mensagens estão disponíveis por meio do gerenciador de formulário. 
  
 **Para recuperar a renderização de um anexo de mensagem**
  
1. Use a classe de mensagem da mensagem para acessar o gerenciador de formulário.
    
2. Acessar a propriedade de PR_MINI_ICON do gerenciador **de** formulário. Para obter mais informações, **consulte PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

