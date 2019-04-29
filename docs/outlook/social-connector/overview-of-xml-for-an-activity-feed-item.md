---
title: Visão geral do XML para um item do feed de atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Um feed de atividades consiste em uma ou mais atividades que ocorrem em uma rede social. Cada feed de atividades é representado por um elemento Ofeed e é caracterizado por estas três informações:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439944"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="b149c-104">Visão geral do XML para um item do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="b149c-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="b149c-105">Um feed de atividades consiste em uma ou mais atividades que ocorrem em uma rede social.</span><span class="sxs-lookup"><span data-stu-id="b149c-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="b149c-106">Cada feed de atividades é representado por um elemento **ofeed** e é caracterizado por estas três informações:</span><span class="sxs-lookup"><span data-stu-id="b149c-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="b149c-107">**rede**— nome da rede social da qual as atividades se originaram.</span><span class="sxs-lookup"><span data-stu-id="b149c-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="b149c-108">**atividades**— contêiner para atividades que ocorrem na conta do usuário conectado na rede social.</span><span class="sxs-lookup"><span data-stu-id="b149c-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="b149c-109">**modelos**— contêiner para modelos usados para exibir o item de atividade correspondente nas **atividades**.</span><span class="sxs-lookup"><span data-stu-id="b149c-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="b149c-110">Para criar um item de feed de atividades, você deve estar em conformidade com o esquema XML de extensibilidade do provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="b149c-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="b149c-111">A Figura 1 mostra a estrutura XML do feed de atividades.</span><span class="sxs-lookup"><span data-stu-id="b149c-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="b149c-112">**Figura 1. Estrutura XML do feed de atividades**</span><span class="sxs-lookup"><span data-stu-id="b149c-112">**Figure 1. Activity feed XML structure**</span></span>

![Activity XML structure](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="b149c-114">Para cada item de feed de atividades, as duas partes mais importantes desse esquema são os elementos **activityDetails** e **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="b149c-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="b149c-115">O elemento **activityDetails** armazena informações específicas de cada item de feed de atividades, como o nome do proprietário da atividade ou a URL para as imagens carregadas.</span><span class="sxs-lookup"><span data-stu-id="b149c-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="b149c-116">O elemento **activityTemplateContainer** armazena o formato ou layout de cada item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="b149c-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="b149c-117">Ele consiste em modelos, representados por \*\*\*\* elementos de activitytemplate individuais, que podem ser reutilizados para vários itens de feed.</span><span class="sxs-lookup"><span data-stu-id="b149c-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="b149c-118">Para um item de feed de atividade individual \*\*\*\* , o elemento activitytemplate especifica as quatro partes de informação a seguir:</span><span class="sxs-lookup"><span data-stu-id="b149c-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="b149c-119">**Icon**— especifica a URL do ícone para exibir o item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="b149c-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="b149c-120">**título**— descreve o item feed de atividades.</span><span class="sxs-lookup"><span data-stu-id="b149c-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="b149c-121">**tipo**— especifica o tipo de atividade, como um status, uma foto ou uma atualização de documento.</span><span class="sxs-lookup"><span data-stu-id="b149c-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="b149c-122">**dados**— Especifica qualquer informação extra exibida com o item feed de atividades.</span><span class="sxs-lookup"><span data-stu-id="b149c-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="b149c-123">O ícone exibido no feed de atividades é sempre o mesmo que o ícone de provedor retornado pela propriedade **ISocialProvider:: SocialNetworkIcon** .</span><span class="sxs-lookup"><span data-stu-id="b149c-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="b149c-124">Consulte os tópicos a seguir para obter mais informações sobre o elemento **activityDetails** , o elemento **activityTemplateContainer** , tokens de modelo e variáveis de modelo:</span><span class="sxs-lookup"><span data-stu-id="b149c-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="b149c-125">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="b149c-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="b149c-126">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="b149c-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="b149c-127">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="b149c-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="b149c-128">Diretrizes para exibir atividades de modo adequado</span><span class="sxs-lookup"><span data-stu-id="b149c-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="b149c-129">Para obter um exemplo de XML de feed de atividades, consulte [exemplo de XML de feed de atividades](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="b149c-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b149c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b149c-130">See also</span></span>

- [<span data-ttu-id="b149c-131">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="b149c-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="b149c-132">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b149c-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="b149c-133">Desenvolvimento de um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="b149c-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

