---
title: Objetos e a arquitetura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279782"
---
# <a name="objects-and-the-mapi-architecture"></a>Objetos e a arquitetura MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os objetos que o MAPI define se enquadram em uma ou mais camadas na arquitetura MAPI. A camada de interface de cliente contém todos os objetos que um aplicativo cliente, visualizador de formulários ou servidor de formulário pode implementar. A camada de interface do provedor de serviços contém os objetos que um provedor de serviços de qualquer tipo pode implementar. Esta camada inclui objetos implementados por catálogos de endereços, repositórios de mensagens, provedores de transporte e bibliotecas de formulários. A camada que representa o subsistema MAPI está posicionada entre as camadas de interface de cliente e de provedor de serviço. A camada MAPI contém todos os objetos que o MAPI implementa para clientes ou provedores de serviço a serem usados. 
  
A ilustração a seguir mostra onde cada um dos objetos MAPI se ajusta à arquitetura MAPI. Os objetos são representados com os nomes de suas interfaces derivadas. Por exemplo, um objeto de coletor de aviso é mostrado como [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), a interface derivada de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) e que cada objeto de coletor de aviso é implementado. As interfaces que as camadas de ponte são usadas ou implementadas por vários componentes. Embora a camada MAPI pareça separar as camadas de cliente e provedor, indicando que toda a comunicação deve fluir por MAPI, esse não é o caso. Os clientes podem e se comunicam diretamente com os objetos do provedor de serviços. 
  
**Object layers in MAPI**
  
![Camadas de objeto no MAPI] (media/amapi_38.gif "Camadas de objeto no MAPI")
  
## <a name="see-also"></a>Confira também

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

