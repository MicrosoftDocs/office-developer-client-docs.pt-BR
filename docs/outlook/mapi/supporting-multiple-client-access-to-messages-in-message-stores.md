---
title: Suporte a várias mensagens de acesso para cliente em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350600"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>Suporte a várias mensagens de acesso para cliente em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
É possível que vários aplicativos cliente abram uma determinada mensagem simultaneamente. Os provedores de repositórios de mensagens não precisam seguir regras específicas para o controle desse acesso. No enTanto, se os aplicativos cliente modificarem a mensagem e salvar suas alterações, o provedor de repositório deverá estar em conformidade com as seguintes regras:
  
- Permita que a primeira chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) prossiga como se fosse o único cliente com a mensagem aberta. 
    
- Nas chamadas de **SaveChanges** subsequentes por outros clientes, o provedor de repositório de mensagens deve ignorar as alterações e retornar MAPI_E_OBJECT_CHANGED. 
    
- Permitir que os aplicativos cliente respondam a um código de retorno do MAPI_E_OBJECT_CHANGED chamando o **SaveChanges** novamente com o sinalizador FORCE_SAVE. Se um aplicativo cliente fizer isso, o provedor do repositório de mensagens deverá substituir as alterações anteriores pelas novas. 
    
Como alternativa, o provedor do repositório de mensagens pode detectar o conflito e apresentar uma interface que permite ao usuário escolher se deseja manter a mensagem original, sobrescrever a mensagem original com as novas alterações ou salvar as novas alterações em outro local.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

