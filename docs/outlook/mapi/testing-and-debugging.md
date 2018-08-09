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
ms.openlocfilehash: 96bc2e58482ba259b14e820f3380978f80c542c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770582"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="e2314-103">Teste e depuração</span><span class="sxs-lookup"><span data-stu-id="e2314-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="e2314-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2314-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2314-105">Estratégias de teste diferem, dependendo se você estiver desenvolvendo um provedor de cliente ou serviço.</span><span class="sxs-lookup"><span data-stu-id="e2314-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="e2314-106">Como um aplicativo cliente requer um ou mais provedores de serviço operar, os clientes devem ser testados em um ambiente com diferentes conjuntos de provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="e2314-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="e2314-107">Provedores de serviço, no entanto, devem ser testadas isoladamente antes sendo integrado com outros provedores.</span><span class="sxs-lookup"><span data-stu-id="e2314-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="e2314-108">MAPI fornece ferramentas que servem para testar os recursos de um provedor de serviço de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="e2314-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="e2314-109">O aplicativo de exemplo [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) mostra como testar os recursos de um provedor de catálogo de endereços e o provedor de armazenamento funciona com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e2314-109">The [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2314-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2314-110">See also</span></span>



[<span data-ttu-id="e2314-111">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="e2314-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="e2314-112">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e2314-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

