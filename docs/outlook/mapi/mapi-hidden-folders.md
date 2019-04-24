---
title: Pastas ocultas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f9daa2169a087cf962d09a7c135e2829c7cd1ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346743"
---
# <a name="mapi-hidden-folders"></a>Pastas ocultas MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As pastas ocultas são pastas genéricas criadas pelos clientes na pasta raiz do repositório de mensagens, e não na pasta raiz de uma subárvore de mensagem interpessoal (IPM). Como essas pastas não são colocadas em uma sub-árvore IPM, elas geralmente ficam ocultas da exibição do usuário pelo provedor de armazenamento de mensagens. As pastas ocultas normalmente contêm informações relevantes para o repositório de mensagens, mas irrelevante para o usuário. Os clientes criam pastas ocultas para armazenar, por exemplo, informações adicionais a serem salvas com o restante da hierarquia de pastas.
  
O MAPI espera que todos os clientes possam exibir, criar, modificar e excluir pastas em uma sub-árvore IPM. O suporte para trabalhar com pastas em outras árvores é considerado opcional. No enTanto, todos os repositórios de mensagens que podem ser usados como o repositório padrão e que podem enviar e receber mensagens devem suportar totalmente as pastas ocultas.
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

