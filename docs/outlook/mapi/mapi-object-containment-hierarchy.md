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
ms.openlocfilehash: f5faf3a3d4971b01509d0ff0cfa59451015ba205
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426923"
---
# <a name="mapi-object-containment-hierarchy"></a>Hierarquia de contenção de objetos MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A relação de contenção entre objetos especifica as dependências que alguns objetos têm em outros objetos para acesso. Para um aplicativo cliente, o acesso a objetos específicos permite o acesso a outras pessoas. Em alguns casos, a relação de contenção entre objetos implementados por um provedor de serviços segue uma hierarquia lógica. Em outros casos, é arbitrário. 
  
Um cliente deve obter acesso a um objeto de sessão MAPI antes de poder usar muitos outros objetos (por exemplo, provedores de serviços e o livro de endereços MAPI).
  
A contenção do armazenamento de mensagens baseia-se na relação hierárquica entre objetos no armazenamento de mensagens: o próprio objeto do armazenamento de mensagens, pastas, mensagens e anexos. Logicamente, os anexos estão contidos em mensagens, mensagens em pastas e pastas no armazenamento de mensagens. A relação de contenção corresponde a essa hierarquia lógica. Para obter acesso a uma mensagem, por exemplo, um cliente deve primeiro acessar a pasta na qual a mensagem está contida. Perfis e objetos de status são exemplos de uma relação de contenção mais arbitrária. Esses dois objetos estão disponíveis durante a sessão. 
  
Com alguns objetos, os contêineres fornecem o único acesso. Anexos e destinatários são exemplos de objetos totalmente dependentes de seus contêineres. O único acesso a um anexo ou destinatário é por meio da mensagem à qual ele pertence. Outros objetos têm caminhos de acesso alternativos. Esses objetos são atribuídos a identificadores binários, conhecidos como identificadores de entrada, pelos provedores de serviços que os criam. Os identificadores de entrada podem ser usados para acessar seus objetos diretamente, permitindo que os clientes ignorem a árvore de contenção. 
  
A ilustração a seguir mostra a hierarquia de contenção MAPI. A sessão está na parte superior da árvore porque é por meio da sessão que um cliente obtém acesso a todos os outros objetos. O próximo nível inclui a tabela de armazenamento de mensagens, um objeto de tabela que lista as propriedades de todos os provedores de armazenamento de mensagens na sessão atual e o livro de endereços para fornecer acesso a todos os provedores de agendas. A tabela de armazenamento de mensagens e o livro de endereços são usados para acessar os objetos implementados por provedores de serviços específicos, mostrados a seguir, em ordem de contenção.
  
**MAPI containment hierarchy**
  
![Hierarquia de contenção]MAPI da hierarquia de(media/amapi_41.gif "contenção MAPI")
  
## <a name="see-also"></a>Confira também

- [Visão geral de objetos e interface MAPI](mapi-object-and-interface-overview.md)

