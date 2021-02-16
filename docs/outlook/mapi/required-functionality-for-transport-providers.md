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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404439"
---
# <a name="required-functionality-for-transport-providers"></a>Funcionalidade necessária para provedores de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada provedor de transporte MAPI deve:
  
- Siga as diretrizes gerais para trabalhar com MAPI e outros provedores de serviços. Para obter mais informações, consulte [MapI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).
    
- Ter seu provedor de transporte DLL expor ao MAPI sua [função de inicialização XPProviderInit.](xpproviderinit.md) 
    
- Exponha ao MAPI sua implementação do [IXPProvider : IUnknown](ixpprovideriunknown.md) e [IXPLogon : interfaces IUnknown.](ixplogoniunknown.md) 
    
- Exponha a MAPI e aplicativos cliente sua implementação do [IMAPIStatus : interface IMAPIProp.](imapistatusimapiprop.md) Para obter mais informações sobre a implementação **de IMAPIStatus,** consulte [Implementação de objeto de status.](status-object-implementation.md) 
    
- Implemente uma caixa de diálogo de folha de propriedades para configuração. Para obter mais informações sobre a implementação de folhas de propriedades, consulte [Implementação da Folha de Propriedades.](property-sheet-implementation.md)
    

