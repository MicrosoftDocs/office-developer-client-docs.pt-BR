---
title: Implementação do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356914"
---
# <a name="message-service-implementation"></a><span data-ttu-id="36114-103">Implementação do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="36114-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="36114-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36114-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36114-105">Um serviço de mensagens é um ou mais provedores de serviços relacionados, agrupados para o propósito de simplificar a instalação e a configuração.</span><span class="sxs-lookup"><span data-stu-id="36114-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="36114-106">Todos os provedores de serviços devem ser incluídos em um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="36114-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="36114-107">Para implementar um serviço de mensagens com um ou mais provedores, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="36114-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="36114-108">Projete o serviço de mensagens, determinando o número e o tipo de provedores de serviços a serem incluídos.</span><span class="sxs-lookup"><span data-stu-id="36114-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="36114-109">Para obter mais informações sobre como criar um serviço de mensagens, consulte [Designing a Message Service](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="36114-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="36114-110">Crie um programa de instalação para instalar os provedores de serviços no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="36114-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="36114-111">Para obter mais informações sobre como escrever um programa de instalação do serviço de mensagens, consulte [supportIng Message Service Installation](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="36114-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="36114-112">Crie uma função de ponto de entrada para executar a configuração.</span><span class="sxs-lookup"><span data-stu-id="36114-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="36114-113">Para obter mais informações sobre a gravação de uma função de ponto de entrada do serviço de mensagens, consulte [supportIng Message Service Configuration](supporting-message-service-configuration.md) e [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="36114-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="36114-114">Crie um arquivo de cabeçalho público que contenha as marcas de propriedade e as descrições de valores válidos para qualquer propriedade personalizada à qual o serviço de mensagens ofereça suporte.</span><span class="sxs-lookup"><span data-stu-id="36114-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="36114-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="36114-115">See also</span></span>



[<span data-ttu-id="36114-116">Provedores de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="36114-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

