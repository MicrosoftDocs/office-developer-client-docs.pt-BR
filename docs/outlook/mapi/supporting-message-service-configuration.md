---
title: Configuração do serviço de mensagens de suporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e1782f3c20c1741e0e4b1859f1b29d835444009c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770522"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="1e0a7-103">Configuração do serviço de mensagens de suporte</span><span class="sxs-lookup"><span data-stu-id="1e0a7-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="1e0a7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e0a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e0a7-105">Para suportar a configuração do serviço de mensagens, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="1e0a7-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="1e0a7-106">Implemente uma função de ponto de entrada que está em conformidade com o protótipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="1e0a7-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="1e0a7-107">Funções de ponto de entrada de serviço de mensagem gerenciam o acesso aos dados de configuração e são chamadas nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="1e0a7-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="1e0a7-108">Quando um cliente fizer logon em recuperar informações para configurar seu serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="1e0a7-109">Quando um cliente deseja exibir ou alterar uma propriedade de configuração.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="1e0a7-110">Embora a maioria dos serviços de mensagem fornecerá funções de ponto de entrada, como deveriam, essas funções não são estritamente necessárias.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="1e0a7-111">Serviços de mensagens podem fornecer acesso aos dados de configuração de outras formas.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="1e0a7-112">No entanto, usando uma função de ponto de entrada padroniza e simplifica o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="1e0a7-113">MAPI espera que todas as mensagens serviço entrada ponto funções para ser capaz de armazenar e recuperar as propriedades de seções perfil associados ao seu serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="1e0a7-114">Você pode oferecer suporte a essa funcionalidade interativamente, programaticamente, ou ambos interativamente e programaticamente.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="1e0a7-115">Para oferecer suporte à configuração interativa, fornecer uma folha de propriedades que exibe as propriedades envolvidas na configuração do seu serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="1e0a7-116">Como opção, também é possível oferecer folhas de propriedades para cada provedor configurável.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="1e0a7-117">Alguns serviços de mensagem restringem os usuários a um modo de exibição somente leitura das propriedades de configuração; outros serviços de mensagem permitem que os usuários façam alterações.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="1e0a7-118">Para oferecer suporte à configuração de programação, sua função de ponto de entrada de serviço de mensagem deve ser capaz de trabalhar sem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="1e0a7-119">Se o seu serviço de mensagem pode ser chamado pelo Assistente de perfil, você deve suportar configuração programática.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="1e0a7-120">Se o seu serviço de mensagem não permitir que a própria a ser configurado usando o Assistente de perfil, você poderá escolher se deseja ou não oferecer suporte a configurações de programação.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="1e0a7-121">Para obter mais informações sobre como suportar a configuração em uma entrada de serviço de mensagem ponto função, consulte [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="1e0a7-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="1e0a7-122">Publica o nome da sua função de ponto de entrada de serviço de mensagem no arquivo de configuração Mapisvc, incluindo a seguinte entrada na seção serviço de mensagem:</span><span class="sxs-lookup"><span data-stu-id="1e0a7-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="1e0a7-123">Crie um ou mais propriedade folha caixas de diálogo para exibir os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="1e0a7-124">Se você quiser permitir que o Assistente de perfil configurar seu serviço de mensagem, execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="1e0a7-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="1e0a7-125">Implemente uma função de ponto de entrada que está em conformidade com o protótipo [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="1e0a7-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="1e0a7-126">Implemente um procedimento de caixa de diálogo Windows padrão que está em conformidade com o protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="1e0a7-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="1e0a7-127">Melhore sua função do ponto de entrada do serviço de mensagem para responder a eventos adicionais.</span><span class="sxs-lookup"><span data-stu-id="1e0a7-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e0a7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e0a7-128">See also</span></span>

- [<span data-ttu-id="1e0a7-129">Implementação do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="1e0a7-129">Message Service Implementation</span></span>](message-service-implementation.md)

