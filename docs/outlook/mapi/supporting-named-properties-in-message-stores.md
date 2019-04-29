---
title: Suporte a propriedades nomeadas em repositórios de mensagens
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
# <a name="supporting-named-properties-in-message-stores"></a>Suporte a propriedades nomeadas em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos Message podem ter propriedades no conjunto de propriedades definidas por MAPI. Essas propriedades podem ser não nomeadas ou nomeadas. As propriedades sem nome devem residir em um intervalo de identificadores de propriedade definido por MAPI. As propriedades personalizadas nomeadas residem em um intervalo diferente de identificadores de propriedade definidos por MAPI. Normalmente, eles são usados por tipos de mensagem personalizados. Seu provedor de repositório de mensagens deve oferecer suporte a propriedades nomeadas se for usado como o repositório de mensagens padrão. O suporte a propriedades nomeadas significa implementar os métodos [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) e implementar uma ou mais assinaturas de mapeamento que identifiquem quais nomes são usados em quais identificadores de propriedade. Para obter mais informações, consulte [definindo novas propriedades MAPI](defining-new-mapi-properties.md) e [propriedades nomeadas de suporte](supporting-named-properties.md).
  
A maioria dos provedores de repositórios de mensagens que oferecem suporte a propriedades nomeadas usam uma única assinatura de mapeamento para todos os objetos no repositório de mensagens. Isso tem dois benefícios. Primeiro, é mais simples implementar assinaturas de mapeamento se houver apenas uma para acompanhar. Em segundo lugar, se todos os objetos no repositório de mensagens usarem a mesma assinatura de mapeamento, os aplicativos cliente serão garantidos que todos os identificadores de propriedade nas mensagens no repositório de mensagens realmente se referem à mesma propriedade nomeada. Isso permite que os aplicativos cliente exibam colunas para propriedades nomeadas na interface de exibição de pastas.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

