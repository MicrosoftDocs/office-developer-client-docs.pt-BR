---
title: Implementar uma interface de configuração para provedores de repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332974"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="04d7f-103">Implementar uma interface de configuração para provedores de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="04d7f-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="04d7f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04d7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04d7f-105">Os provedores de repositórios de mensagens são necessários para implementar uma interface que permite que o usuário configure o provedor de repositório de mensagens para ser executado no computador desse usuário.</span><span class="sxs-lookup"><span data-stu-id="04d7f-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="04d7f-106">Normalmente, o provedor do repositório de mensagens é configurado quando o provedor do repositório de mensagens é adicionado ao perfil de um usuário.</span><span class="sxs-lookup"><span data-stu-id="04d7f-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="04d7f-107">A interface de configuração do provedor de repositório de mensagens geralmente trata de tarefas como configurar nomes de usuário e senhas para repositórios de mensagens protegidos, escolher caminhos para arquivos necessários e criar o mecanismo de armazenamento subjacente que ele usará, se necessário.</span><span class="sxs-lookup"><span data-stu-id="04d7f-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="04d7f-108">A interface de configuração implementada é acessada por pontos de entrada adicionais na DLL do provedor de serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04d7f-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="04d7f-109">Para obter mais informações, consulte [Configuring a Message Service](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="04d7f-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="04d7f-110">A interface de configuração do provedor de repositório de mensagens é a única interface de usuário que um provedor de armazenamento de mensagens deve implementar.</span><span class="sxs-lookup"><span data-stu-id="04d7f-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04d7f-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="04d7f-111">See also</span></span>



[<span data-ttu-id="04d7f-112">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="04d7f-112">Message Store Features</span></span>](message-store-features.md)

