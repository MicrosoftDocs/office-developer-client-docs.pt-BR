---
title: Estrutura de provedores de armazenamento de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 58b6771c6bdae91ad0e496189258e4745de5bc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584286"
---
# <a name="structure-of-message-store-providers"></a>Estrutura de provedores de armazenamento de mensagem
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de armazenamento de mensagem, quando ele está em execução na memória, é um [IMSProvider: IUnknown](imsprovideriunknown.md) interface. A interface de **IMSProvider** permite que o cliente aplicativos e o spooler MAPI fazer logon e logoff de armazenamento de mensagens. As interfaces que aplicativos cliente e o MAPI spooler usam para acessar mensagens no armazenamento de mensagens e pastas são interfaces [IMSLogon](imslogoniunknown.md) e [IMsgStore](imsgstoreimapiprop.md) . Estas interfaces geralmente são criados quando o armazenamento de mensagens é primeiro fazer logon, embora o ponto de entrada da mensagem [MSProviderInit](msproviderinit.md) armazenar DLL também pode criá-los. 
  
Como as interfaces **IMSLogon** e **IMsgStore** compartilham alguns métodos, talvez seja mais fácil criar um objeto de classe que herda de duas interfaces. Você também pode implementar estas interfaces nos objetos separados e grave funções de auxiliar internas para sua DLL que implementam os métodos compartilhados que podem ser chamados depois dos métodos nas interfaces **IMSLogon** e **IMsgStore** . 
  
A ilustração a seguir mostra uma estrutura de tópicos de alto nível da hierarquia do objeto dentro de um armazenamento de mensagens em execução.
  
**Message store object hierarchy**
  
![Hierarquia de objetos de armazenamento de mensagens] (media/storeobj.gif "Hierarquia de objetos de armazenamento de mensagens")
  
## <a name="see-also"></a>Confira também

- [Desenvolver um provedor do repositório de mensagens MAPI](developing-a-mapi-message-store-provider.md)

