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
  
Quando uma nova pasta ou mensagem é criada em um armazenamento de mensagens, o provedor de armazenamento de mensagens precisa atribuir a esse objeto um identificador de entrada para que os aplicativos clientes possam se referir a ele. Os provedores de armazenamento de mensagens podem reutilizar os identificadores de entrada de longo prazo dos objetos excluídos ou criar novos identificadores. Não há requisitos de uma maneira ou de outra para provedores de armazenamento de mensagens; No entanto, se for viável, um provedor de armazenamento de mensagens deve sempre gerar novos identificadores de entrada de longo prazo para novos objetos em vez de reutilizar os antigos. Não há problema em reutilizar identificadores de entrada de curto prazo quando os objetos a que se referem são excluídos.
  
O motivo para essa exclusão é que os clientes podem armazenar em cache identificadores de entrada, às vezes por longos períodos de tempo. Se isso acontecer e o provedor do armazenamento de mensagens reutilizar identificadores de entrada, é possível que o identificador de entrada se refira a um objeto diferente quando o cliente abre o identificador de entrada do que quando obteve pela primeira vez o identificador de entrada. Se o provedor do armazenamento de mensagens não reutilizar identificadores de entrada — ou pelo menos usar um esquema de geração de identificador de entrada que não se repete há muito tempo — esse problema não pode ocorrer.
  
Da mesma forma, os provedores de armazenamento de mensagens devem tentar preservar identificadores de entrada para pastas e mensagens quando eles são movidos no armazenamento de mensagens. Se o provedor de armazenamento de mensagens puder fazer isso, as referências a objetos no armazenamento não se tornarão inválidas quando o objeto for movido para um local diferente no armazenamento.
  
## <a name="see-also"></a>Confira também

- [Recursos do Armazenamento de Mensagens](message-store-features.md)

