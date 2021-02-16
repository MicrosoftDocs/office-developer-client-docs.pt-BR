---
title: Implementando uma interface de configuração para provedores de armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415884"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="dccce-103">Implementando uma interface de configuração para provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="dccce-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="dccce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dccce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dccce-105">Provedores de armazenamento de mensagens são necessários para implementar uma interface que permite ao usuário configurar o provedor de armazenamento de mensagens para executar no computador desse usuário.</span><span class="sxs-lookup"><span data-stu-id="dccce-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="dccce-106">Normalmente, o provedor de armazenamento de mensagens é configurado quando o provedor de armazenamento de mensagens é adicionado ao perfil de um usuário.</span><span class="sxs-lookup"><span data-stu-id="dccce-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="dccce-107">A interface de configuração do provedor de armazenamento de mensagens geralmente lida com tarefas como definir nomes de usuário e senhas para armazenamentos de mensagens protegidos, escolher caminhos para os arquivos necessários e criar o mecanismo de armazenamento subjacente que ele usará, se necessário.</span><span class="sxs-lookup"><span data-stu-id="dccce-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="dccce-108">A interface de configuração implementada é acessada por meio de pontos de entrada adicionais na DLL do provedor de serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dccce-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="dccce-109">Para obter mais informações, [consulte Configurando um serviço de mensagens.](configuring-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="dccce-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="dccce-110">A interface de configuração do provedor de armazenamento de mensagens é a única interface do usuário que um provedor de armazenamento de mensagens deve implementar.</span><span class="sxs-lookup"><span data-stu-id="dccce-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dccce-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="dccce-111">See also</span></span>



[<span data-ttu-id="dccce-112">Recursos do Armazenamento de Mensagens</span><span class="sxs-lookup"><span data-stu-id="dccce-112">Message Store Features</span></span>](message-store-features.md)

