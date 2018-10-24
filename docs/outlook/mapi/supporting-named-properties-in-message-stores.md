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
ms.openlocfilehash: 235683d8565732034f868dd71e4f2047ffe76f09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569838"
---
# <a name="supporting-named-properties-in-message-stores"></a>Suporte a propriedades nomeadas em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Objetos de mensagem podem ter propriedades neles que não estão no conjunto de propriedades definidas pelo MAPI. Tais propriedades podem ser não nomeadas ou nomeadas. Propriedades sem nome devem residir em um intervalo de identificadores de propriedade definida pelo MAPI. Propriedades personalizadas nomeadas residirem em um intervalo diferente dos identificadores de propriedade definida pelo MAPI. Eles geralmente são usados por tipos de mensagem personalizada. Seu provedor de armazenamento de mensagem deve oferecer suporte a propriedades nomeadas caso deva ser usado como o armazenamento de mensagens padrão. Suporte a propriedades nomeadas significa Implementando os métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e a implementação de uma ou mais assinaturas de mapeamento que identificam quais nomes vá com quais identificadores de propriedade. Para obter mais informações, consulte [Definindo novas propriedades MAPI](defining-new-mapi-properties.md) e [Suporte a propriedades chamado](supporting-named-properties.md).
  
A maioria das mensagens armazenar provedores que suportam chamados de assinatura de um único mapeamento de uso de propriedades para todos os objetos no repositório de mensagem. Isso tem duas vantagens. Primeiro, é mais simples implementar assinaturas de mapeamento, se houver apenas um para acompanhar. Em segundo lugar, se todos os objetos no repositório de mensagem usam a mesma assinatura de mapeamento, aplicativos de cliente são certeza de que todos os identificadores de propriedade em mensagens no repositório de mensagem realmente se referem a mesma propriedade nomeada. Isso permite que aplicativos de cliente exibir colunas para propriedades nomeadas em sua interface de visualização de pasta.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

