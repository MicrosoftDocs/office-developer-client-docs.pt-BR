---
title: Gerar e usar identificadores de entradas em provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437676"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Gerar e usar identificadores de entradas em provedores do repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando uma nova pasta ou mensagem é criada em um repositório de mensagens, o provedor de armazenamento de mensagens precisa atribuir a esse objeto um identificador de entrada para que os aplicativos clientes possam consultá-lo. Os provedores de repositórios de mensagens podem reutilizar os identificadores de entrada de longo prazo dos objetos excluídos ou criar novos identificadores. Não há um requisito de uma maneira ou o outro para provedores de repositórios de mensagens; no entanto, se for viável, um provedor de repositório de mensagens sempre deverá gerar novos identificadores de entrada de longo prazo para novos objetos, em vez de usar os antigos. É preciso reutilizar identificadores de entrada de curto prazo quando os objetos aos quais eles se referem são excluídos.
  
O motivo dessa exclusão é que os clientes podem armazenar em cache identificadores de entrada, às vezes por longos períodos de tempo. Se isso acontecer e o provedor do repositório de mensagens reutilizar identificadores de entrada, é possível que o identificador de entrada faça referência a um objeto diferente quando o cliente abre o identificador de entrada do que quando obteve o identificador de entrada pela primeira vez. Se o provedor do repositório de mensagens não reutilizar identificadores de entrada — ou pelo menos usa um esquema de geração de identificador de entrada que não se repete por um tempo muito longo — esse problema não pode ocorrer.
  
Da mesma forma, os provedores de repositórios de mensagens devem tentar preservar identificadores de entrada para pastas e mensagens quando forem movidos no repositório de mensagens. Se o provedor de repositório de mensagens puder fazer isso, as referências a objetos no repositório não se tornarão inválidas quando o objeto for movido para um local diferente no repositório.
  
## <a name="see-also"></a>Confira também

- [Recursos do repositório de mensagens](message-store-features.md)

