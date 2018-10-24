---
title: Exibir as pastas de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3a89588294f07dca97fb48e56d2cde890c3f80ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568816"
---
# <a name="mapi-view-folders"></a>Exibir as pastas de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibir pastas são pastas raiz que contêm informações associadas para definir layouts de exibição alternativo para o conteúdo das pastas de mensagem interpessoais (IPM). Exibir pastas residem sob a raiz para o armazenamento de mensagens e, portanto, não são visíveis no aplicativo cliente típico. Nem todo armazenamento de mensagens inclui pastas de exibição; somente armazenamentos de mensagens que estão configurados para funcionar como o armazenamento de mensagens padrão para a sessão devem inclui-los.  
  
MAPI suporta duas pastas de exibição:
  
- Comum — A pasta de exibição comuns contém modos de exibição que são padrão para o armazenamento de mensagens e podem ser usados por qualquer usuário de um cliente que acessa o armazenamento de mensagens. O identificador de entrada para a pasta de exibição comuns é armazenado na propriedade de **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) da loja.
    
- Pessoal — A pasta de exibição pessoal contém modos de exibição que são definidos por um usuário específico. MAPI define a propriedade **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) para reter o identificador de entrada da pasta de exibição pessoal. Usando as exibições pessoais, por exemplo, um usuário pode examinar um grupo de mensagens, classificados por remetente, listando apenas a mensagem assunto e recebimento data; outro usuário pode examinar o mesmo grupo classificado por data, listando o assunto, o remetente e o tamanho da mensagem.
    
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

