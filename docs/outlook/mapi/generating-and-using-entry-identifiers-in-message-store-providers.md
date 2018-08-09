---
title: Gerando e uso de identificadores de entrada na mensagem de provedores de armazenamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3bfda4a1dbe464c744917c2e9b3ca66eaf88fd20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766661"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Gerando e uso de identificadores de entrada na mensagem de provedores de armazenamento

**Aplica-se a**: Outlook 
  
Quando uma nova pasta ou mensagem é criada em um armazenamento de mensagens, o provedor de armazenamento de mensagem deve atribuir esse objeto em um identificador de entrada para que os aplicativos clientes podem se referir a ele. Provedores de armazenamento de mensagens podem reutilizar os identificadores de entrada de longo prazo expirado dos objetos excluídos ou criar novos identificadores. Não há nenhum requisito de uma forma ou outro para provedores de armazenamento de mensagem; No entanto, se ele for viável, um provedor de armazenamento de mensagem sempre deve gerar novos identificadores de entrada de longo prazo para novos objetos, em vez da reutilizando as antigas. Há problemas reutilizar os identificadores de entrada de curto prazo quando os objetos que se referem ao são excluídos.
  
O motivo para essa exclusão é que os clientes podem armazenar em cache identificadores de entrada, às vezes por longos períodos de tempo. Se isso ocorrer e o provedor de armazenamento de mensagem reutilizar os identificadores de entrada, é possível para o identificador de entrada para se referir a um objeto diferente, quando o cliente abre o identificador de entrada que quando obteve seu primeiro o identificador de entrada. Se o provedor de armazenamento de mensagem não reutilizar os identificadores de entrada — ou pelo menos usa um esquema de geração de identificador de entrada que não se repete por um tempo muito longo — esse problema não é possível ocorrer.
  
Da mesma forma, os provedores de armazenamento de mensagem devem tentar preservar os identificadores de entrada para pastas e mensagens quando forem movidos no repositório de mensagem. Se o provedor de armazenamento de mensagens pode fazer isso, referências a objetos no repositório não tornarão inválidas quando o objeto é movido para um local diferente no repositório.
  
## <a name="see-also"></a>Confira também

- [Recursos do repositório de mensagens](message-store-features.md)

