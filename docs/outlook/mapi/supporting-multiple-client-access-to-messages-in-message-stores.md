---
title: Suporte a vários acesso do cliente para mensagens em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b13fbb9f2807c9814fed5ba3bcca8fe73aaa7b01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564217"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>Suporte a vários acesso do cliente para mensagens em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
É possível para vários aplicativos de cliente abrir uma determinada mensagem simultaneamente. Provedores de armazenamento de mensagem não precisará Siga todas as regras específicas para administrando tal acesso. No entanto, se os aplicativos cliente modificar a mensagem e salvem suas alterações, o provedor de armazenamento deve ser compatíveis com as regras a seguir:
  
- Permitir que a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) continuar como se fosse o único cliente que tem a mensagem aberto. 
    
- Sobre as chamadas subsequentes **SaveChanges** por outros clientes, o provedor de armazenamento de mensagem deve ignorar as alterações e retornar MAPI_E_OBJECT_CHANGED. 
    
- Permitir aplicativos para responder a um código de retorno MAPI_E_OBJECT_CHANGED pela chamada **SaveChanges** novamente com o sinalizador FORCE_SAVE de cliente. Se um aplicativo cliente faz isso, o provedor de armazenamento de mensagem deve substituir as alterações anteriores com os novos. 
    
Como alternativa, o provedor de armazenamento de mensagens pode detectar o conflito e apresentar uma interface que permite que o usuário escolha se deseja manter a mensagem original, substituir a mensagem original com as alterações ou salvar as alterações de novas para outro local.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

