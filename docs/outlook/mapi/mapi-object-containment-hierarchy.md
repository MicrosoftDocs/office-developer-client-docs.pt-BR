---
title: Hierarquia de contenção de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6350202eb22edc478f7738bebf6d7f0bc4684ee0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566240"
---
# <a name="mapi-object-containment-hierarchy"></a>Hierarquia de contenção de objetos MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O relacionamento entre objetos Especifica as dependências de alguns objetos em outros objetos do access. Para um aplicativo cliente, acesso aos objetos determinados habilita o acesso a outras pessoas. Em alguns casos, o relacionamento entre objetos implementada por um provedor de serviços segue uma hierarquia lógica. Em outros casos, é arbitrário. 
  
Um cliente deve obter acesso a um objeto de sessão MAPI para que ele possa usar muitos outros objetos (por exemplo, provedores de serviços e o catálogo de endereços MAPI).
  
Contenção de repositório de mensagem se baseia na relação hierárquica entre objetos no repositório de mensagem: o armazenamento de mensagens do objeto propriamente dito, pastas, mensagens e anexos. Logicamente, anexos estão contidos em mensagens, mensagens em pastas e pastas no repositório de mensagem. O relacionamento de contenção corresponde a essa hierarquia lógica. Para obter acesso a uma mensagem, por exemplo, um cliente deve primeiro acessar a pasta em que a mensagem está contida. Perfis e objetos de status são exemplos de uma relação de contenção mais arbitrário. Ambos desses objetos estão disponíveis através da sessão. 
  
Com alguns objetos, contêineres fornecem o acesso único. Destinatários e anexos são exemplos de objetos que são totalmente dependentes de seus contêineres. O único acesso a um anexo ou um destinatário é por meio da mensagem à qual ele pertence. Outros objetos têm caminhos de acesso alternativo. Esses objetos são atribuídos identificadores binários, conhecidos como identificadores de entrada, pelos provedores de serviço que criá-los. Identificadores de entrada podem ser usados para acessar seus objetos diretamente, permitindo que os clientes ignorar a árvore de contenção. 
  
A ilustração a seguir mostra a hierarquia de contenção de MAPI. A sessão está na parte superior da árvore porque ele é através da sessão que um cliente obtiver acesso a todos os outros objetos. O próximo nível inclui a tabela de repositório de mensagens, um objeto table que lista as propriedades de todos os provedores de repositório de mensagem na sessão atual e o catálogo de endereços para fornecer acesso a todos os provedores de catálogo de endereços. O catálogo de tabela e endereço de repositório de mensagem são usadas para acessar os objetos implementados por provedores de serviço específico, mostrados a seguir, na ordem de contenção.
  
**MAPI containment hierarchy**
  
![Hierarquia de contenção de MAPI] (media/amapi_41.gif "Hierarquia de contenção de MAPI")
  
## <a name="see-also"></a>Confira também

- [Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

