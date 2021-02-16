---
title: Estrutura de provedores do armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426419"
---
# <a name="structure-of-message-store-providers"></a>Estrutura de provedores do armazenamento de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de armazenamento de mensagens, quando está sendo executado na memória, é um [IMSProvider : interface IUnknown.](imsprovideriunknown.md) A interface **IMSProvider** permite que aplicativos cliente e o spooler MAPI faça logoff de e para o armazenamento de mensagens. As interfaces que os aplicativos cliente e o spooler MAPI usam para acessar pastas e mensagens no repositório de mensagens são interfaces [IMSLogon](imslogoniunknown.md) e [IMsgStore.](imsgstoreimapiprop.md) Normalmente, essas interfaces são criadas quando o armazenamento de mensagens é conectado pela primeira vez, embora o ponto de entrada [MSProviderInit](msproviderinit.md) da DLL do armazenamento de mensagens também possa criar. 
  
Como as interfaces **IMSLogon** e **IMsgStore** compartilham alguns métodos, pode ser mais fácil criar um objeto de classe que herda de ambas as interfaces. Você também pode implementar essas interfaces em objetos separados e gravar funções auxiliares internas à sua DLL que implementam os métodos compartilhados que podem ser chamados a partir dos métodos nas interfaces **IMSLogon** e **IMsgStore.** 
  
A ilustração a seguir mostra uma delineada de alto nível da hierarquia de objetos em um armazenamento de mensagens em execução.
  
**Message store object hierarchy**
  
![Hierarquia de objetos do armazenamento de mensagens]Hierarquia de objetos do armazenamento de(media/storeobj.gif "mensagens")
  
## <a name="see-also"></a>Confira também

- [Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

