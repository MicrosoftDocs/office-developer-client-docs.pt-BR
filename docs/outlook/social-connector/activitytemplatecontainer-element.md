---
title: Elemento activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Um elemento activityTemplateContainer é um modelo que permite formatar seus itens de feed de atividade e reutilizar XML que especifica um layout.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413714"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="9663f-103">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="9663f-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="9663f-104">Um **elemento activityTemplateContainer** é um modelo que permite formatar seus itens de feed de atividade e reutilizar XML que especifica um layout.</span><span class="sxs-lookup"><span data-stu-id="9663f-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="9663f-105">Use IDs (**applicationID** e **templateID**) para corresponder um item de feed (**activityDetails**) a um modelo (**activityTemplateContainer**).</span><span class="sxs-lookup"><span data-stu-id="9663f-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="9663f-106">Armazene os dados de layout como parte do **elemento activityTemplate.**</span><span class="sxs-lookup"><span data-stu-id="9663f-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="9663f-107">Para fazer referência aos dados que são retirados do item de feed de atividades individuais, use variáveis de modelo como espaço reservado para informações como pessoas, links e texto.</span><span class="sxs-lookup"><span data-stu-id="9663f-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="9663f-108">A tabela a seguir descreve os três elementos que o **elemento activityTemplateContainer** requer.</span><span class="sxs-lookup"><span data-stu-id="9663f-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="9663f-109">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9663f-109">**Element**</span></span>|<span data-ttu-id="9663f-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9663f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9663f-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="9663f-111">**applicationID**</span></span> <br/> |<span data-ttu-id="9663f-112">Uma das duas IDs exclusivas que são usadas para corresponder o item de feed com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="9663f-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="9663f-113">Se você tiver vários aplicativos ou outros grupos, isso poderá ser usado como um organizador de modelos de primeira camada.</span><span class="sxs-lookup"><span data-stu-id="9663f-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="9663f-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="9663f-114">**templateID**</span></span> <br/> |<span data-ttu-id="9663f-115">A segunda ID exclusiva usada para corresponder o item de feed com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="9663f-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="9663f-116">Isso pode ser usado como um organizador de modelos de segunda camada.</span><span class="sxs-lookup"><span data-stu-id="9663f-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="9663f-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="9663f-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="9663f-118">O layout do modelo **(ícone,** **título** e **elementos** de dados) e o tipo de atividade **(elemento de** tipo).</span><span class="sxs-lookup"><span data-stu-id="9663f-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="9663f-119">A tabela a seguir descreve os elementos filho de **activityTemplate**, que descrevem o layout e o tipo de um modelo.</span><span class="sxs-lookup"><span data-stu-id="9663f-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="9663f-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9663f-120">**Element**</span></span>|<span data-ttu-id="9663f-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9663f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9663f-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="9663f-122">**icon**</span></span> <br/> |<span data-ttu-id="9663f-123">Um token de link, que faz referência à URL do ícone para esse item de feed.</span><span class="sxs-lookup"><span data-stu-id="9663f-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="9663f-124">**title**</span><span class="sxs-lookup"><span data-stu-id="9663f-124">**title**</span></span> <br/> |<span data-ttu-id="9663f-125">As informações necessárias para o item de feed.</span><span class="sxs-lookup"><span data-stu-id="9663f-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="9663f-126">**tipo**</span><span class="sxs-lookup"><span data-stu-id="9663f-126">**type**</span></span> <br/> |<span data-ttu-id="9663f-127">O tipo de atividade, como uma atualização de status, foto ou documento.</span><span class="sxs-lookup"><span data-stu-id="9663f-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="9663f-128">**data**</span><span class="sxs-lookup"><span data-stu-id="9663f-128">**data**</span></span> <br/> |<span data-ttu-id="9663f-129">Qualquer informação adicional para o item de feed, como imagens, texto ou links.</span><span class="sxs-lookup"><span data-stu-id="9663f-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="9663f-130">Para um exemplo de XML do feed de atividades, consulte [Exemplo XML do feed de atividades](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="9663f-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9663f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9663f-131">See also</span></span>

- [<span data-ttu-id="9663f-132">Visão geral do XML para um item do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="9663f-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="9663f-133">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="9663f-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="9663f-134">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="9663f-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="9663f-135">Diretrizes para a exibição adequada das atividades</span><span class="sxs-lookup"><span data-stu-id="9663f-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="9663f-136">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="9663f-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="9663f-137">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="9663f-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="9663f-138">Como desenvolver um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="9663f-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

