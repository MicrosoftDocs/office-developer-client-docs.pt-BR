---
title: Funcionalidade necessária para provedores de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328683"
---
# <a name="required-functionality-for-transport-providers"></a>Funcionalidade necessária para provedores de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada provedor de transporte MAPI deve:
  
- Siga as diretrizes gerais para trabalhar com MAPI e outros provedores de serviços. Para obter mais informações, consulte [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).
    
- Ter sua DLL do provedor de transporte expõe para MAPI sua função de inicialização [XPProviderInit](xpproviderinit.md) . 
    
- Expor a MAPI sua implementação das interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) e [IXPLogon: IUnknown](ixplogoniunknown.md) . 
    
- Expor a MAPI e aplicativos cliente sua implementação da interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . Para obter mais informações sobre a implementação de **IMAPIStatus**, consulte [status Object Implementation](status-object-implementation.md). 
    
- Implementar uma caixa de diálogo de folha de propriedades para configuração. Para obter mais informações sobre a implementação de folhas de propriedades, consulte [implementação da folha de propriedades](property-sheet-implementation.md).
    

