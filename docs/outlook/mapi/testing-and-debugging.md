---
title: Teste e depuração
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8e1f15ae354894aede4e8418e6428d0524ccb70d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316476"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="fdf72-103">Teste e depuração</span><span class="sxs-lookup"><span data-stu-id="fdf72-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="fdf72-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdf72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdf72-105">As estratégias de teste diferem dependendo se você está desenvolvendo um cliente ou provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="fdf72-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="fdf72-106">Como um aplicativo cliente exige que um ou mais provedores de serviço operem, os clientes devem ser testados em um ambiente com diferentes conjuntos de provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="fdf72-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="fdf72-107">No entanto, os provedores de serviços devem ser testados isoladamente antes de serem integrados a outros provedores.</span><span class="sxs-lookup"><span data-stu-id="fdf72-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="fdf72-108">O MAPI fornece ferramentas destinadas a testar os recursos de um provedor de serviços de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="fdf72-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="fdf72-109">O aplicativo de exemplo [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) mostra como testar os recursos de um provedor de catálogo de endereços e funciona com um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fdf72-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fdf72-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdf72-110">See also</span></span>



[<span data-ttu-id="fdf72-111">Visão geral da programação MAPI</span><span class="sxs-lookup"><span data-stu-id="fdf72-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="fdf72-112">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fdf72-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

