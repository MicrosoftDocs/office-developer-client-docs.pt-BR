---
title: Suporte a vários acessos de cliente a mensagens em armazenamentos de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439860"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>Suporte a vários acessos de cliente a mensagens em armazenamentos de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
É possível que vários aplicativos clientes abram uma determinada mensagem simultaneamente. Os provedores de armazenamento de mensagens não têm que seguir nenhuma regra específica para reger esse acesso. No entanto, se os aplicativos cliente modificarem a mensagem e salvarem suas alterações, o provedor da loja deverá estar em conformidade com as seguintes regras:
  
- Permita que a primeira chamada para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) prossiga como se fosse o único cliente que tenha a mensagem aberta. 
    
- Nas chamadas **saveChanges subsequentes** de outros clientes, o provedor de armazenamento de mensagens deve ignorar as alterações e retornar MAPI_E_OBJECT_CHANGED. 
    
- Permita que os aplicativos clientes respondam a MAPI_E_OBJECT_CHANGED código de retorno chamando **SaveChanges** novamente com o sinalizador FORCE_SAVE código. Se um aplicativo cliente fizer isso, o provedor de armazenamento de mensagens deverá substituir as alterações anteriores por novas. 
    
Como alternativa, o provedor de armazenamento de mensagens pode detectar o conflito e apresentar uma interface que permite ao usuário escolher se deve manter a mensagem original, substituir a mensagem original com as novas alterações ou salvar as novas alterações em outro local.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

