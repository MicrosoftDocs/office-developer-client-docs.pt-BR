---
title: Invalidando um objeto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407673"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="3214e-103">Invalidando um objeto</span><span class="sxs-lookup"><span data-stu-id="3214e-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="3214e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3214e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3214e-105">Como parte do processo de desligamento do provedor, talvez você queira invalidar um objeto.</span><span class="sxs-lookup"><span data-stu-id="3214e-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="3214e-106">A invalidação de um objeto envolve a substituição de uma vtable com uma vtable que contém implementações para os três métodos **IUnknown** : **AddRef**, **Release**e **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="3214e-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="3214e-107">Invalidar um objeto chamando [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md), um método que está incluído no objeto support de cada um dos três tipos de provedor comuns.</span><span class="sxs-lookup"><span data-stu-id="3214e-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="3214e-108">Geralmente, os provedores fazem essa chamada na implementação do método **logoff** do objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="3214e-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="3214e-109">A invalidação de um objeto dá ao MAPI a responsabilidade final de liberar a memória associada a um objeto.</span><span class="sxs-lookup"><span data-stu-id="3214e-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="3214e-110">Você pode liberar todos os recursos conectados a um objeto e, em seguida, chamar **MakeInvalid** para invalidar todos os métodos em suas interfaces herdadas.</span><span class="sxs-lookup"><span data-stu-id="3214e-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="3214e-111">As chamadas para qualquer um desses métodos retornarão MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="3214e-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="3214e-112">O uso do **MakeInvalid** é uma opção que muitos provedores de serviço optam por ignorar.</span><span class="sxs-lookup"><span data-stu-id="3214e-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3214e-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="3214e-113">See also</span></span>



[<span data-ttu-id="3214e-114">Desligar um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="3214e-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

