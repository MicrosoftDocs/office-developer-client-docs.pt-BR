---
title: Implementar uma Interface de configuração para provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 15833768fbd148ae4e689b5a80ed3479823864cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592924"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="e9f68-103">Implementar uma Interface de configuração para provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="e9f68-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="e9f68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9f68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9f68-105">Provedores de armazenamento de mensagem são necessários para implementar uma interface que permite ao usuário configurar o provedor de armazenamento de mensagens para ser executado no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="e9f68-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="e9f68-106">Normalmente, o provedor de armazenamento de mensagens é configurado quando o provedor de armazenamento de mensagem é adicionado a um perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="e9f68-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="e9f68-107">Interface de configuração do provedor de repositório a mensagem geralmente trata de tarefas, como a definição de nomes de usuário e senhas para repositórios de mensagem protegida, escolhendo caminhos para os arquivos necessários, e criando o mecanismo de armazenamento subjacente ele usará, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e9f68-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="e9f68-108">Você implementar a interface de configuração é acessada através de pontos de entrada adicionais na DLL do provedor de serviço sua mensagem.</span><span class="sxs-lookup"><span data-stu-id="e9f68-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="e9f68-109">Para obter mais informações, consulte [Configurando um serviço de mensagem](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="e9f68-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="e9f68-110">Interface de configuração do provedor de repositório a mensagem é a única interface de usuário que um provedor de armazenamento de mensagem deve implementar.</span><span class="sxs-lookup"><span data-stu-id="e9f68-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9f68-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9f68-111">See also</span></span>



[<span data-ttu-id="e9f68-112">Recursos de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="e9f68-112">Message Store Features</span></span>](message-store-features.md)

