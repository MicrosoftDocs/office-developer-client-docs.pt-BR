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
ms.openlocfilehash: 031f8f17ae98bd62043a2cd8ce6c8c2d55a19c9f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582333"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Renderizar um anexo em texto sem formatação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para renderizar um anexo em uma mensagem com texto sem formatação, recuperar a propriedade de **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) do anexo e aplicá-lo aos dados da **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) propriedade. Há duas maneiras de se recuperar **PR_RENDERING_POSITION**:
  
- Abra o anexo chamando o método de **IMessage::OpenAttach** da mensagem e, em seguida, peça para a propriedade **PR_RENDERING_POSITION** chamando o método de **IMAPIProp::GetProps** do anexo. Para obter mais informações, consulte [IMessage::OpenAttach](imessage-openattach.md) e [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Chame o método de **IMessage::GetAttachmentTable** da mensagem para acessar sua tabela de anexo e recuperar a coluna que contém a propriedade **PR_RENDERING_POSITION** . Dessa forma sempre é preferível. Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Tenha em mente que muitas lojas RTF reconhecimento de mensagem não calculam **PR_RENDERING_POSITION** até que um cliente solicitar a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de uma mensagem. Até lá, **PR_RENDERING_POSITION** geralmente representa um valor aproximado. Provedores de armazenamento de mensagem são permitidas para fornecer a clientes com um valor aproximado para aprimorar o desempenho. 
  
A renderização de um arquivo ou anexo binário é armazenada em sua propriedade **PR_ATTACH_RENDERING** . Você tem a opção de recuperação **PR_ATTACH_RENDERING** da mesma forma como você recuperou **PR_RENDERING_POSITION**: diretamente a partir de anexo ou a tabela de anexos. Para **PR_ATTACH_RENDERING**, a primeira estratégia, embora mais demorada, é mais seguro. Como alguns provedores de armazenamento de mensagem truncar suas colunas da tabela para 255 bytes ou, em alguns casos 510 bytes, é difícil certificar-se de que a coluna **PR_ATTACH_RENDERING** contém a renderização completa. Ao recuperar a propriedade diretamente do anexo, ele sempre será concluído. 
  
Anexos não OLE nem mensagem definida **PR_ATTACH_RENDERING**. Em vez disso, as informações de renderização de anexos OLE 1 são armazenadas no fluxo de mensagens de texto. Anexos de 2 OLE, ele é armazenado em um stream especiais filho do objeto de armazenamento. Informações de anexos de mensagens de renderização está disponível por meio do Gerenciador de formulário. 
  
 **Para recuperar a renderização de um anexo de mensagem**
  
1. Use a classe de mensagem da mensagem para acessar o Gerenciador de formulário.
    
2. Acesse a propriedade **PR_MINI_ICON** do gerente do formulário. Para obter mais informações, consulte **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

