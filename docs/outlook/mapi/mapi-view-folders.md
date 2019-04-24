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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357334"
---
# <a name="mapi-view-folders"></a>Pastas de exibição MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As pastas de exibição são pastas raiz que contêm informações associadas para definir layouts de exibição alternativos para o conteúdo de pastas de mensagens interpessoais (IPM). As pastas de exibição residem na raiz do repositório de mensagens e, portanto, não são visíveis no aplicativo cliente típico. Nem todos os repositórios de mensagens incluem pastas de exibição; somente os repositórios de mensagens que estão configurados para funcionar como o repositório de mensagens padrão para a sessão devem incluí-los.  
  
O MAPI dá suporte a duas pastas de exibição:
  
- Comum — a pasta de modo de exibição comum contém modos de exibição padrão para o repositório de mensagens e pode ser usada por qualquer usuário de um cliente que acessa o repositório de mensagens. O identificador de entrada para a pasta de modo de exibição comum é armazenado na propriedade **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) da loja.
    
- Pessoal — a pasta de exibição pessoal contém exibições definidas por um usuário específico. MAPI define a propriedade **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) para conter o identificador de entrada da pasta de exibição pessoal. Usando modos de exibição pessoais, por exemplo, um usuário pode ver um grupo de mensagens classificadas por remetente, listando apenas o assunto da mensagem e a data de recebimento; outro usuário pode ver o mesmo grupo classificado por data, listando o assunto, o remetente e o tamanho da mensagem.
    
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

