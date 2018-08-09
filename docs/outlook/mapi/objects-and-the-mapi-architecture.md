---
title: Objetos e a arquitetura do MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0e89c2ad37b700a977962e5e0ff0ca30b9d910e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768180"
---
# <a name="objects-and-the-mapi-architecture"></a>Objetos e a arquitetura do MAPI

**Aplica-se a**: Outlook 
  
Todos os objetos que MAPI define se encaixam em uma ou mais camadas da arquitetura de MAPI. A camada da interface de cliente contém todos os objetos que um aplicativo cliente, o Visualizador do formulário ou o servidor de formulário pode implementar. A camada de interface do provedor de serviço contém os objetos que pode ser implementar um provedor de serviços de qualquer tipo. Essa camada inclui objetos implementados por catálogos de endereços, repositórios de mensagem, provedores de transporte e bibliotecas de formulários. A camada que representa o subsistema de MAPI está posicionada entre as camadas de interface de provedor de cliente e de serviço. A camada MAPI contém todos os objetos que implementa o MAPI para clientes ou provedores de serviço para usar. 
  
A ilustração a seguir mostra onde cada um dos objetos MAPI se encaixa a arquitetura MAPI. Os objetos são representados com os nomes de suas interfaces derivadas. Por exemplo, um objeto de coletor de eventos advise é mostrado como [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), a interface que derive da [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) e que cada objeto de coletor de eventos advise implementa. As interfaces que ponte camadas são usadas ou implementadas por vários componentes. Embora a camada MAPI aparece para separar as camadas de cliente e o provedor, indicando que todas as comunicações devem fluir por MAPI, isso não é o caso. Os clientes possam e se comunicar diretamente com objetos do provedor de serviço. 
  
**Object layers in MAPI**
  
![Camadas de objeto no MAPI] (media/amapi_38.gif "Camadas de objeto no MAPI")
  
## <a name="see-also"></a>Confira também

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

