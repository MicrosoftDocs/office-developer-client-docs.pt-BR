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
  
Um provedor de armazenamento de mensagens, quando está em execução na memória, é uma interface [IMSProvider: IUnknown](imsprovideriunknown.md) . A interface **IMSProvider** permite que os aplicativos cliente e o spooler MAPI façam logon e logoff no repositório de mensagens. As interfaces que os aplicativos clientes e o spooler MAPI usam para acessar pastas e mensagens no repositório de mensagens são interfaces [IMSLogon](imslogoniunknown.md) e [IMsgStore](imsgstoreimapiprop.md) . Essas interfaces normalmente são criadas quando o repositório de mensagens é conectado pela primeira vez, embora o ponto de entrada [MSProviderInit](msproviderinit.md) da dll do repositório de mensagens também possa criá-las. 
  
Como as interfaces **IMSLogon** e **IMsgStore** compartilham alguns métodos, pode ser mais fácil criar um objeto Class que herda de ambas as interfaces. Você também pode implementar essas interfaces em objetos separados e escrever funções auxiliares internas à sua DLL que implementam os métodos compartilhados que podem ser chamados dos métodos nas interfaces **IMSLogon** e **IMsgStore** . 
  
A ilustração a seguir mostra uma estrutura de tópicos de alto nível da hierarquia de objetos em um repositório de mensagens em execução.
  
**Message store object hierarchy**
  
![Hierarquia do objeto do repositório de mensagens] (media/storeobj.gif "Hierarquia do objeto do repositório de mensagens")
  
## <a name="see-also"></a>Confira também

- [Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

