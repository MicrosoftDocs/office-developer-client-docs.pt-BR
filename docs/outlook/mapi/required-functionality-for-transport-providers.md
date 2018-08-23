---
title: Funcionalidade exigida para provedores de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580492"
---
# <a name="required-functionality-for-transport-providers"></a>Funcionalidade exigida para provedores de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada provedor de transporte MAPI deve:
  
- Siga as diretrizes gerais para trabalhar com os outros provedores de serviços e MAPI. Para obter mais informações, consulte [O desenvolvimento de aplicativos MAPI](mapi-application-development.md) e [Provedores de serviços de MAPI](mapi-service-providers.md).
    
- Ter sua função de inicialização de [XPProviderInit](xpproviderinit.md) de seu provedor de transporte são expostos DLL para MAPI. 
    
- Expor para MAPI sua implementação do [IXPProvider: IUnknown](ixpprovideriunknown.md) e [IXPLogon: IUnknown](ixplogoniunknown.md) interfaces. 
    
- Expor para aplicativos cliente e MAPI sua implementação do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface. Para obter mais informações sobre como implementar **IMAPIStatus**, consulte o [Status de implementação de objeto](status-object-implementation.md). 
    
- Implemente uma caixa de diálogo de folha de propriedade para a configuração. Para obter mais informações sobre como implementar folhas de propriedades, consulte [Implementação da folha de propriedade](property-sheet-implementation.md).
    

