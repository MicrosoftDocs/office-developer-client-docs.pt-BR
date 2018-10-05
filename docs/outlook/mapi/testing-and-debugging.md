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
ms.openlocfilehash: 8e1f15ae354894aede4e8418e6428d0524ccb70d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383657"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="b6b37-103">Teste e depuração</span><span class="sxs-lookup"><span data-stu-id="b6b37-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="b6b37-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6b37-105">Estratégias de teste diferem, dependendo se você estiver desenvolvendo um provedor de cliente ou serviço.</span><span class="sxs-lookup"><span data-stu-id="b6b37-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="b6b37-106">Como um aplicativo cliente requer um ou mais provedores de serviço operar, os clientes devem ser testados em um ambiente com diferentes conjuntos de provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="b6b37-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="b6b37-107">Provedores de serviço, no entanto, devem ser testadas isoladamente antes sendo integrado com outros provedores.</span><span class="sxs-lookup"><span data-stu-id="b6b37-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="b6b37-108">MAPI fornece ferramentas que servem para testar os recursos de um provedor de serviço de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="b6b37-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="b6b37-109">O aplicativo de exemplo [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) mostra como testar os recursos de um provedor de catálogo de endereços e o provedor de armazenamento funciona com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b6b37-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6b37-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6b37-110">See also</span></span>



[<span data-ttu-id="b6b37-111">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b37-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="b6b37-112">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b6b37-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

