---
title: Suporte à configuração do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350607"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="af95b-103">Suporte à configuração do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="af95b-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="af95b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af95b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af95b-105">Para oferecer suporte à configuração do serviço de mensagens, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="af95b-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="af95b-106">Implementar uma função de ponto de entrada que está de acordo com o protótipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="af95b-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="af95b-107">As funções de ponto de entrada de serviço de mensagens gerenciam o acesso a dados de configuração e são chamadas nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="af95b-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="af95b-108">Quando um cliente faz logon para recuperar informações para configurar o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="af95b-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="af95b-109">Quando um cliente deseja exibir ou alterar uma propriedade de configuração.</span><span class="sxs-lookup"><span data-stu-id="af95b-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="af95b-110">Embora a maioria dos serviços de mensagens forneça funções de ponto de entrada, como deveriam, essas funções não são estritamente necessárias.</span><span class="sxs-lookup"><span data-stu-id="af95b-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="af95b-111">Os serviços de mensagens podem fornecer acesso a dados de configuração de outras maneiras.</span><span class="sxs-lookup"><span data-stu-id="af95b-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="af95b-112">No enTanto, o uso de uma função de ponto de entrada padroniza e simplifica o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="af95b-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="af95b-113">O MAPI espera que todas as funções de ponto de entrada do serviço de mensagens possam armazenar e recuperar as propriedades das seções de perfil associadas ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="af95b-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="af95b-114">Você pode oferecer suporte a essa funcionalidade interativamente, programaticamente ou de forma interativa e proativa.</span><span class="sxs-lookup"><span data-stu-id="af95b-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="af95b-115">Para oferecer suporte à configuração interativa, forneça uma folha de propriedades que exibe as propriedades envolvidas na configuração do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="af95b-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="af95b-116">Como opção, você também pode fornecer folhas de propriedades para cada provedor configurável.</span><span class="sxs-lookup"><span data-stu-id="af95b-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="af95b-117">Alguns serviços de mensagens restringem os usuários a um modo de exibição somente leitura das propriedades de configuração; outros serviços de mensagens permitem que os usuários façam alterações.</span><span class="sxs-lookup"><span data-stu-id="af95b-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="af95b-118">Para oferecer suporte à configuração programática, a função de ponto de entrada do serviço de mensagens deve ser capaz de funcionar sem a intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="af95b-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="af95b-119">Se o seu serviço de mensagens puder ser chamado pelo assistente de perfil, você deverá oferecer suporte à configuração programática.</span><span class="sxs-lookup"><span data-stu-id="af95b-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="af95b-120">Se o serviço de mensagens não permitir que ele próprio seja configurado usando o assistente de perfil, você poderá escolher se a configuração programática será ou não compatível.</span><span class="sxs-lookup"><span data-stu-id="af95b-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="af95b-121">Para obter mais informações sobre como oferecer suporte à configuração em uma função de ponto de entrada do serviço de mensagens, consulte [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="af95b-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="af95b-122">Publique o nome da função de ponto de entrada do serviço de mensagens no arquivo de configuração MAPISVC. inf, incluindo a seguinte entrada na seção serviço de mensagens:</span><span class="sxs-lookup"><span data-stu-id="af95b-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="af95b-123">Crie uma ou mais caixas de diálogo de folha de propriedades para exibir dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="af95b-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="af95b-124">Execute as seguintes tarefas se quiser permitir que o assistente de perfil configure o serviço de mensagens:</span><span class="sxs-lookup"><span data-stu-id="af95b-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="af95b-125">Implementar uma função de ponto de entrada que está de acordo com o protótipo [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="af95b-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="af95b-126">Implemente um procedimento de caixa de diálogo padrão do Windows que esteja em conformidade com o protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="af95b-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="af95b-127">Aprimore sua função de ponto de entrada do serviço de mensagens para responder a eventos adicionais.</span><span class="sxs-lookup"><span data-stu-id="af95b-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af95b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="af95b-128">See also</span></span>

- [<span data-ttu-id="af95b-129">Implementação do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="af95b-129">Message Service Implementation</span></span>](message-service-implementation.md)

