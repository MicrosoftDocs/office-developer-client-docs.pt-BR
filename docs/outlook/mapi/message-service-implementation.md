---
title: Implementação do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768127"
---
# <a name="message-service-implementation"></a><span data-ttu-id="386f6-103">Implementação do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="386f6-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="386f6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="386f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="386f6-105">Um serviço de mensagem é um ou mais provedores de serviço relacionado agrupados para fins de simplifica a instalação e configuração.</span><span class="sxs-lookup"><span data-stu-id="386f6-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="386f6-106">Todos os provedores de serviço devem ser incluídos em um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="386f6-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="386f6-107">Para implementar um serviço de mensagem com um ou mais provedores, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="386f6-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="386f6-108">Projete o serviço de mensagem, determinando o número e tipo de provedores de serviço a serem incluídas.</span><span class="sxs-lookup"><span data-stu-id="386f6-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="386f6-109">Para obter mais informações sobre como projetar um serviço de mensagem, consulte [Criando um serviço de mensagem](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="386f6-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="386f6-110">Crie um programa de instalação para instalar os provedores de serviço no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="386f6-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="386f6-111">Para obter mais informações sobre como escrever um programa de instalação do serviço de mensagem, consulte [Instalação do serviço de mensagem com suporte](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="386f6-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="386f6-112">Crie uma função de ponto de entrada para executar a configuração.</span><span class="sxs-lookup"><span data-stu-id="386f6-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="386f6-113">Para obter mais informações sobre como escrever uma entrada de serviço de mensagem ponto função, consulte [Configuração do serviço de mensagem com suporte](supporting-message-service-configuration.md) e [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="386f6-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="386f6-114">Crie um arquivo de cabeçalho público que contém as marcas de propriedade e descrições dos valores válidos para quaisquer propriedades personalizadas que suporta o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="386f6-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="386f6-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="386f6-115">See also</span></span>



[<span data-ttu-id="386f6-116">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="386f6-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

