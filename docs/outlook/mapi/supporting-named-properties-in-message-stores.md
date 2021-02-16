---
title: Suporte a propriedades nomeadas em armazenamentos de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7e33c49d1ed211abf70e04a8bd3c06ca62e88572
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434918"
---
# <a name="supporting-named-properties-in-message-stores"></a>Suporte a propriedades nomeadas em armazenamentos de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Objetos message podem ter propriedades neles que não estão no conjunto de propriedades definido por MAPI. Essas propriedades podem ser nomeadas ou não. Propriedades não nomeadas devem residir em um intervalo de identificadores de propriedade definidos por MAPI. Propriedades personalizadas nomeadas residem em um intervalo diferente de identificadores de propriedade definidos por MAPI. Eles geralmente são usados por tipos de mensagem personalizados. Seu provedor de armazenamento de mensagens deve dar suporte a propriedades nomeadas se ela for usada como o armazenamento de mensagens padrão. O suporte a propriedades nomeadas significa implementar os métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e implementar uma ou mais assinaturas de mapeamento que identificam quais nomes vão com quais identificadores de propriedade. Para obter mais informações, consulte [Definindo novas propriedades MAPI](defining-new-mapi-properties.md) e [dando suporte a propriedades nomeadas.](supporting-named-properties.md)
  
A maioria dos provedores de armazenamento de mensagens que suportam propriedades nomeadas usa uma única assinatura de mapeamento para todos os objetos no armazenamento de mensagens. Isso tem dois benefícios. Primeiro, é mais simples implementar assinaturas de mapeamento se houver apenas uma para acompanhar. Segundo, se todos os objetos no armazenamento de mensagens usarem a mesma assinatura de mapeamento, os aplicativos cliente têm certeza de que todos os identificadores de propriedade em mensagens no armazenamento de mensagens realmente se referem à mesma propriedade nomeada. Isso permite que aplicativos cliente exibem colunas para propriedades nomeadas em sua interface de exibição de pasta.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

