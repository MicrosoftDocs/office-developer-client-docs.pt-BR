---
title: Implementar a segurança
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417284"
---
# <a name="implementing-security"></a><span data-ttu-id="34a1c-103">Implementar a segurança</span><span class="sxs-lookup"><span data-stu-id="34a1c-103">Implementing Security</span></span>

  
  
<span data-ttu-id="34a1c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34a1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34a1c-105">Se o sistema de mensagens exigir, o provedor de transporte é responsável pela implementação de um nível apropriado de segurança para acessar o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="34a1c-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="34a1c-106">Cada mensagem de entrada ou saída enviada por meio de um provedor de transporte pelo spooler MAPI é manipulada no contexto de uma sessão de logon de provedor.</span><span class="sxs-lookup"><span data-stu-id="34a1c-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="34a1c-107">O provedor de transporte pode exibir uma caixa de diálogo de logon para o usuário que solicita as credenciais de um usuário antes de estabelecer tal conexão.</span><span class="sxs-lookup"><span data-stu-id="34a1c-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="34a1c-108">Como alternativa, o provedor de transporte pode armazenar as credenciais inseridas anteriormente do usuário no intervalo de propriedades seguras dentro de uma seção de perfil e usá-las para acesso sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="34a1c-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="34a1c-109">Ao implementar a segurança do provedor de transporte, considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="34a1c-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="34a1c-110">Com vários provedores de serviços instalados, pode haver uma infinidade de nomes e senhas associados a um usuário.</span><span class="sxs-lookup"><span data-stu-id="34a1c-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="34a1c-111">O MAPI permite várias sessões com múltiplas identidades.</span><span class="sxs-lookup"><span data-stu-id="34a1c-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="34a1c-112">Os provedores são incentivados a oferecer suporte a várias sessões, mas não são necessários para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="34a1c-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="34a1c-113">Cada sessão com um provedor de transporte é associada por MAPI com uma seção discreta no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="34a1c-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="34a1c-114">O provedor de transporte pode usar o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) para obter acesso a esta seção, que pode ser usada para armazenar qualquer informação associada a esta sessão, incluindo credenciais.</span><span class="sxs-lookup"><span data-stu-id="34a1c-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="34a1c-115">Com vários provedores de transporte instalados, não é necessariamente verdade de que o usuário tenha apenas um único endereço de email.</span><span class="sxs-lookup"><span data-stu-id="34a1c-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="34a1c-116">Um usuário pode ter um endereço de email separado para cada provedor de transporte instalado ou pode ter um endereço diferente para cada sessão em um único provedor.</span><span class="sxs-lookup"><span data-stu-id="34a1c-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="34a1c-117">Para obter mais informações sobre como armazenar credenciais em seções de perfil, consulte [Message Services and](message-services-and-profiles.md) Profiles e [IProfSect: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="34a1c-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

