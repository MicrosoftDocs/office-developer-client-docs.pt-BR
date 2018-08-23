---
title: Implementar a segurança
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c2926e7c94178d5a3135f34e2ab3b3ae11d145dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568480"
---
# <a name="implementing-security"></a><span data-ttu-id="d5ccd-103">Implementar a segurança</span><span class="sxs-lookup"><span data-stu-id="d5ccd-103">Implementing Security</span></span>

  
  
<span data-ttu-id="d5ccd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5ccd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5ccd-105">Se o sistema de mensagens exigir, o provedor de transporte é responsável por implementar um nível apropriado de segurança de acesso ao sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="d5ccd-106">Cada mensagem de entrada ou saída enviada através de um provedor de transporte pelo spooler MAPI é manipulada no contexto de uma sessão de logon do provedor.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="d5ccd-107">O provedor de transporte pode exibir uma caixa de diálogo de logon para o usuário que solicita credenciais do usuário antes de estabelecer uma conexão tal.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="d5ccd-108">Como alternativa, o provedor de transporte pode armazenar as credenciais do usuário inseridos anteriormente no intervalo propriedade segura dentro de uma seção de perfil e usá-los para o access sem avisar.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="d5ccd-109">Ao implementar a segurança do seu provedor de transporte, considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d5ccd-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="d5ccd-110">Com vários provedores de serviço instalado, pode haver uma infinidade de nomes e senhas associadas a um usuário.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="d5ccd-111">MAPI permite várias sessões com várias identidades.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="d5ccd-112">Provedores são incentivados a oferecer suporte a várias sessões, mas não são necessários para fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="d5ccd-113">Cada sessão com um provedor de transporte está associada por MAPI uma seção discreta no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="d5ccd-114">O provedor de transporte pode usar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para acessar os nesta seção, que pode ser usada para armazenar informações associadas a essa sessão, inclusive as credenciais.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="d5ccd-115">Com vários provedores de transporte instalados, não é necessariamente verdadeiro se o usuário tem somente um único endereço de email.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="d5ccd-116">Um usuário pode ter um endereço de email separados para cada provedor de transporte instalados ou pode ter um endereço diferente para cada sessão em um único provedor.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="d5ccd-117">Para obter mais informações sobre como armazenar credenciais nas seções de perfil, consulte [Serviços de mensagem e perfis](message-services-and-profiles.md) e [IProfSect: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="d5ccd-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

