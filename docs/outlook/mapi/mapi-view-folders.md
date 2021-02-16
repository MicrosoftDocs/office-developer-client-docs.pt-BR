---
title: Pastas de exibição MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ca9e5138d3ded13dfe33037f75e43ef1098f3c2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412531"
---
# <a name="mapi-view-folders"></a>Pastas de exibição MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As pastas de exibição são pastas raiz que contêm informações associadas para definir layouts de exibição alternativos para o conteúdo de pastas de mensagens interpersonalas (IPM). As pastas de exibição residem na raiz do armazenamento de mensagens e, portanto, não são visíveis no aplicativo cliente típico. Nem todo armazenamento de mensagens inclui pastas de exibição; somente os armazenamentos de mensagens configurados para funcionar como o armazenamento de mensagens padrão da sessão devem incluí-los.  
  
MAPI supports two view folders:
  
- Comum — A pasta de exibição comum contém exibições que são padrão para o armazenamento de mensagens e podem ser usadas por qualquer usuário de um cliente que acesse o armazenamento de mensagens. O identificador de entrada para a pasta de exibição comum é armazenado na propriedade **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) do armazenamento.
    
- Pessoal — A pasta de exibição pessoal contém exibições definidas por um usuário específico. MAPI define a **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) para manter o identificador de entrada da pasta de exibição pessoal. Usando exibições pessoais, por exemplo, um usuário pode olhar para um grupo de mensagens ordenadas por remetente, listando apenas o assunto da mensagem e a data de recebimento; outro usuário pode olhar para o mesmo grupo, organizado por data, listando o assunto, o remetente e o tamanho da mensagem.
    
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

