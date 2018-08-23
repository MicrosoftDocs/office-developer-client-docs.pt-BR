---
title: Teste e depuração
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ae9b49717fd7981d653e9852ed02d50bef7c7846
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590684"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="3fdcf-103">Teste e depuração</span><span class="sxs-lookup"><span data-stu-id="3fdcf-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="3fdcf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fdcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fdcf-105">Estratégias de teste diferem, dependendo se você estiver desenvolvendo um provedor de cliente ou serviço.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="3fdcf-106">Como um aplicativo cliente requer um ou mais provedores de serviço operar, os clientes devem ser testados em um ambiente com diferentes conjuntos de provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="3fdcf-107">Provedores de serviço, no entanto, devem ser testadas isoladamente antes sendo integrado com outros provedores.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="3fdcf-108">MAPI fornece ferramentas que servem para testar os recursos de um provedor de serviço de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="3fdcf-109">O aplicativo de exemplo [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) mostra como testar os recursos de um provedor de catálogo de endereços e o provedor de armazenamento funciona com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-109">The [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3fdcf-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fdcf-110">See also</span></span>



[<span data-ttu-id="3fdcf-111">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="3fdcf-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="3fdcf-112">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="3fdcf-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

