---
title: Hierarquia de herança de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345834"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Hierarquia de herança de objetos MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todas as interfaces implementadas por objetos MAPI herdam, em última análise, [de IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), a interface OLE que permite que os objetos se comuniquem. A maioria das interfaces herda diretamente de **IUnknown**, mas algumas herdam de uma de duas outras interfaces base: [IMAPIProp : IUnknown](imapipropiunknown.md) ou [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). A ilustração a seguir mostra a hierarquia de herança completa em MAPI.
  
**MAPI inheritance hierarchy**
  
![Hierarquia de herança MAPI da](media/amapi_06.gif "hierarquia de herança MAPI")
  
## <a name="see-also"></a>Confira também

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Visão geral de objetos e interface MAPI](mapi-object-and-interface-overview.md)

