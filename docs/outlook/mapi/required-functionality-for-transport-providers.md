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
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="1f747-103">Funcionalidade necessária para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="1f747-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="1f747-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f747-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f747-105">Cada provedor de transporte MAPI deve:</span><span class="sxs-lookup"><span data-stu-id="1f747-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="1f747-106">Siga as diretrizes gerais para trabalhar com MAPI e outros provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="1f747-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="1f747-107">Para obter mais informações, consulte [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="1f747-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="1f747-108">Ter sua DLL do provedor de transporte expõe para MAPI sua função de inicialização [XPProviderInit](xpproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="1f747-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="1f747-109">Expor a MAPI sua implementação das interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) e [IXPLogon: IUnknown](ixplogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="1f747-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="1f747-110">Expor a MAPI e aplicativos cliente sua implementação da interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="1f747-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="1f747-111">Para obter mais informações sobre a implementação de **IMAPIStatus**, consulte [status Object Implementation](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1f747-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="1f747-112">Implementar uma caixa de diálogo de folha de propriedades para configuração.</span><span class="sxs-lookup"><span data-stu-id="1f747-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="1f747-113">Para obter mais informações sobre a implementação de folhas de propriedades, consulte [implementação da folha de propriedades](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1f747-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

