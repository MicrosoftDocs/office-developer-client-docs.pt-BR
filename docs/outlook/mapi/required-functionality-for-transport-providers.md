---
title: Funcionalidade exigida para provedores de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580492"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="4eb5e-103">Funcionalidade exigida para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="4eb5e-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="4eb5e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4eb5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4eb5e-105">Cada provedor de transporte MAPI deve:</span><span class="sxs-lookup"><span data-stu-id="4eb5e-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="4eb5e-106">Siga as diretrizes gerais para trabalhar com os outros provedores de serviços e MAPI.</span><span class="sxs-lookup"><span data-stu-id="4eb5e-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="4eb5e-107">Para obter mais informações, consulte [O desenvolvimento de aplicativos MAPI](mapi-application-development.md) e [Provedores de serviços de MAPI](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="4eb5e-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="4eb5e-108">Ter sua função de inicialização de [XPProviderInit](xpproviderinit.md) de seu provedor de transporte são expostos DLL para MAPI.</span><span class="sxs-lookup"><span data-stu-id="4eb5e-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="4eb5e-109">Expor para MAPI sua implementação do [IXPProvider: IUnknown](ixpprovideriunknown.md) e [IXPLogon: IUnknown](ixplogoniunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="4eb5e-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="4eb5e-110">Expor para aplicativos cliente e MAPI sua implementação do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="4eb5e-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="4eb5e-111">Para obter mais informações sobre como implementar **IMAPIStatus**, consulte o [Status de implementação de objeto](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4eb5e-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="4eb5e-112">Implemente uma caixa de diálogo de folha de propriedade para a configuração.</span><span class="sxs-lookup"><span data-stu-id="4eb5e-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="4eb5e-113">Para obter mais informações sobre como implementar folhas de propriedades, consulte [Implementação da folha de propriedade](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4eb5e-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

