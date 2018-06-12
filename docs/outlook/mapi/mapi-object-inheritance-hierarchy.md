---
title: Hierarquia de herança de objeto MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a03b994a613bbb1f17db3e3220b7e053989c278a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767890"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Hierarquia de herança de objeto MAPI

**Aplica-se a**: Outlook 
  
Todas as interfaces implementadas por objetos MAPI basicamente herdem [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), a interface OLE que permite a comunicação entre objetos. A maioria das interfaces herde diretamente **IUnknown**, mas algumas herdarem de uma das duas interfaces de base: [IMAPIProp: IUnknown](imapipropiunknown.md) ou [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). A ilustração a seguir mostra a hierarquia de herança completa em MAPI.
  
**Hierarquia de herança de MAPI**
  
![Hierarquia de herança de MAPI] (media/amapi_06.gif "Hierarquia de herança de MAPI")
  
## <a name="see-also"></a>Confira também

- [IMAPIProp: IUnknown](imapipropiunknown.md) 
- [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)
- [Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

