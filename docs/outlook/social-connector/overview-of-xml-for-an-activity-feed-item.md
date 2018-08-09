---
title: Visão geral do XML para um item do feed de atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Um feed de atividade consiste em uma ou mais atividades que ocorrem em uma rede social. Cada feed de atividade é representada por um elemento de feed de atividades e é caracterizada por esses três partes de informações:'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770964"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="6e2a8-104">Visão geral do XML para um item do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="6e2a8-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="6e2a8-105">Um feed de atividade consiste em uma ou mais atividades que ocorrem em uma rede social.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="6e2a8-106">Cada feed de atividade é representada por um elemento de **feed de atividades** e é caracterizada por esses três partes de informações:</span><span class="sxs-lookup"><span data-stu-id="6e2a8-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="6e2a8-107">**rede**— nome da rede social que origem as atividades.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="6e2a8-108">**atividades**— contêiner para atividades acontecendo na conta do usuário conectado em rede social.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="6e2a8-109">**modelos**— contêiner para modelos que são usados para exibir o item de atividade correspondente em **atividades**.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="6e2a8-110">Para criar uma item de feed de atividade, você deve estar em conformidade com o esquema XML de extensibilidade de provedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="6e2a8-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="6e2a8-111">A Figura 1 mostra o que feed de atividade de estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="6e2a8-112">**Figura 1. Estrutura XML do feed de atividade**</span><span class="sxs-lookup"><span data-stu-id="6e2a8-112">**Figure 1. Activity feed XML structure**</span></span>

![Activity XML structure](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="6e2a8-114">Para cada item de feed de atividades, as duas partes mais importantes deste esquema são os elementos **activityDetails** e **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="6e2a8-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="6e2a8-115">O elemento **activityDetails** armazena informações específicas para cada item, como o nome do proprietário atividade ou a URL para as imagens carregados de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="6e2a8-116">O elemento **activityTemplateContainer** armazena o formato ou item de feed de layout para cada atividade.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="6e2a8-117">Ele consiste em modelos, representados por individuais **activityTemplate** elementos, que podem ser reutilizados para vários itens de feed.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="6e2a8-118">Para uma item de feed de atividade de individual, o elemento **activityTemplate** Especifica as quatro unidades de informações a seguintes:</span><span class="sxs-lookup"><span data-stu-id="6e2a8-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="6e2a8-119">**ícone**— Especifica o URL para o ícone para exibir a atividade feed item.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="6e2a8-120">**título**— descreve a item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="6e2a8-121">**tipo**— Especifica o tipo de atividade, como um status, foto ou atualização do documento.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="6e2a8-122">**dados**— Especifica qualquer informação extra exibida com um item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="6e2a8-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="6e2a8-123">O ícone exibido na feed de atividade sempre é o mesmo que o ícone do provedor retornado pela propriedade **ISocialProvider::SocialNetworkIcon** .</span><span class="sxs-lookup"><span data-stu-id="6e2a8-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="6e2a8-124">Consulte os tópicos a seguir para obter mais informações sobre o elemento **activityDetails** , o elemento **activityTemplateContainer** , tokens de modelo e variáveis de modelo:</span><span class="sxs-lookup"><span data-stu-id="6e2a8-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="6e2a8-125">activityDetails elemento</span><span class="sxs-lookup"><span data-stu-id="6e2a8-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="6e2a8-126">activityTemplateContainer elemento</span><span class="sxs-lookup"><span data-stu-id="6e2a8-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="6e2a8-127">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="6e2a8-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="6e2a8-128">Diretrizes para exibir adequadamente atividades</span><span class="sxs-lookup"><span data-stu-id="6e2a8-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="6e2a8-129">Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="6e2a8-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e2a8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e2a8-130">See also</span></span>

- [<span data-ttu-id="6e2a8-131">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="6e2a8-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="6e2a8-132">Esquema XML do Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="6e2a8-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="6e2a8-133">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="6e2a8-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

