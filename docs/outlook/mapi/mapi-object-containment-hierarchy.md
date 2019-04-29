---
title: Hierarquia de confinamento de objeto MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f5faf3a3d4971b01509d0ff0cfa59451015ba205
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426923"
---
# <a name="mapi-object-containment-hierarchy"></a>Hierarquia de confinamento de objeto MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A relação de confinamento entre objetos especifica as dependências que alguns objetos têm em outros objetos para o Access. Para um aplicativo cliente, o acesso a determinados objetos permite o acesso a outras pessoas. Em alguns casos, a relação de confinamento entre objetos implementados por um provedor de serviços segue uma hierarquia lógica. Em outros casos, é arbitrária. 
  
Um cliente deve obter acesso a um objeto de sessão MAPI antes de poder usar muitos outros objetos (por exemplo, provedores de serviço e o catálogo de endereços MAPI).
  
O contêiner de armazenamento de mensagens baseia-se na relação hierárquica entre os objetos no repositório de mensagens: o próprio objeto de repositório de mensagens, pastas, mensagens e anexos. Logicamente, os anexos estão contidos em mensagens, mensagens em pastas e pastas no repositório de mensagens. O relacionamento de confinamento corresponde a essa hierarquia lógica. Para obter acesso a uma mensagem, por exemplo, um cliente deve primeiro acessar a pasta na qual a mensagem está contida. Perfis e objetos de status são exemplos de uma relação de confinamento mais arbitrária. Esses dois objetos estão disponíveis através da sessão. 
  
Com alguns objetos, os contêineres fornecem o único acesso. Anexos e destinatários são exemplos de objetos totalmente dependentes de seus contêineres. O único acesso a um anexo ou destinatário é através da mensagem à qual ele pertence. Outros objetos têm caminhos de acesso alternativos. Esses objetos são atribuídos a identificadores binários, conhecidos como identificadores de entrada, pelos provedores de serviços que os criam. Os identificadores de entrada podem ser usados para acessar seus objetos diretamente, permitindo que os clientes ignorem a árvore de confinamento. 
  
A ilustração a seguir mostra a hierarquia de confinamento MAPI. A sessão está na parte superior da árvore porque é por meio da sessão que um cliente obtém acesso a todos os outros objetos. O próximo nível inclui a tabela de repositório de mensagens, um objeto Table que lista as propriedades de todos os provedores de repositórios de mensagens na sessão atual e o catálogo de endereços para fornecer acesso a todos os provedores de catálogo de endereços. A tabela de repositório de mensagens e o catálogo de endereços são usados para acessar os objetos implementados por provedores de serviços específicos, mostrados a seguir, em ordem de confinamento.
  
**MAPI containment hierarchy**
  
![Hierarquia] de conFinamento MAPI (media/amapi_41.gif "Hierarquia") de conFinamento MAPI
  
## <a name="see-also"></a>Confira também

- [Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

