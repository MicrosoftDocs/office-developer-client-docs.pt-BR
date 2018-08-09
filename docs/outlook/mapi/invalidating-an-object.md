---
title: Invalidar um objeto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9c0ba8f1f0bf31bb892f380df310cd9fa7a8a24f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767585"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="6180f-103">Invalidar um objeto</span><span class="sxs-lookup"><span data-stu-id="6180f-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="6180f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6180f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6180f-105">Como parte do processo de encerramento do seu provedor, talvez você queira invalidar um objeto.</span><span class="sxs-lookup"><span data-stu-id="6180f-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="6180f-106">A invalidação de um objeto envolve a substituição seu vtable com uma vtable que contém implementações para os três métodos **IUnknown** : **QueryInterface**, **AddRef**e **Release**.</span><span class="sxs-lookup"><span data-stu-id="6180f-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="6180f-107">Invalide um objeto chamando [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), um método que está incluído no objeto de suporte de cada um dos três tipos de provedor comuns.</span><span class="sxs-lookup"><span data-stu-id="6180f-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="6180f-108">Provedores geralmente fazer essa chamada na implementação do método de **Logoff** do objeto seus logon.</span><span class="sxs-lookup"><span data-stu-id="6180f-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="6180f-109">A invalidação de um objeto dá MAPI a responsabilidade ultimate para liberar a memória associada ao objeto.</span><span class="sxs-lookup"><span data-stu-id="6180f-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="6180f-110">Você pode liberar todos os recursos conectados com um objeto e em seguida, chame **MakeInvalid** para invalidar todos os métodos em seus interfaces herdadas.</span><span class="sxs-lookup"><span data-stu-id="6180f-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="6180f-111">Chamadas para qualquer um desses métodos retornará MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="6180f-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="6180f-112">O uso de **MakeInvalid** é uma opção que muitos provedores de serviço optar por ignorar.</span><span class="sxs-lookup"><span data-stu-id="6180f-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6180f-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="6180f-113">See also</span></span>



[<span data-ttu-id="6180f-114">Desligar a um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="6180f-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

