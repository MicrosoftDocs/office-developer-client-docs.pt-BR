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
ms.openlocfilehash: eb5d70c31f28df16593fb020f13124ea217476ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770265"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="72afb-103">Funcionalidade exigida para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="72afb-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="72afb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72afb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72afb-105">Cada provedor de transporte MAPI deve:</span><span class="sxs-lookup"><span data-stu-id="72afb-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="72afb-106">Siga as diretrizes gerais para trabalhar com os outros provedores de serviços e MAPI.</span><span class="sxs-lookup"><span data-stu-id="72afb-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="72afb-107">Para obter mais informações, consulte [O desenvolvimento de aplicativos MAPI](mapi-application-development.md) e [Provedores de serviços de MAPI](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="72afb-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="72afb-108">Ter sua função de inicialização de [XPProviderInit](xpproviderinit.md) de seu provedor de transporte são expostos DLL para MAPI.</span><span class="sxs-lookup"><span data-stu-id="72afb-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="72afb-109">Expor para MAPI sua implementação do [IXPProvider: IUnknown](ixpprovideriunknown.md) e [IXPLogon: IUnknown](ixplogoniunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="72afb-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="72afb-110">Expor para aplicativos cliente e MAPI sua implementação do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="72afb-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="72afb-111">Para obter mais informações sobre como implementar **IMAPIStatus**, consulte o [Status de implementação de objeto](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="72afb-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="72afb-112">Implemente uma caixa de diálogo de folha de propriedade para a configuração.</span><span class="sxs-lookup"><span data-stu-id="72afb-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="72afb-113">Para obter mais informações sobre como implementar folhas de propriedades, consulte [Implementação da folha de propriedade](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="72afb-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

