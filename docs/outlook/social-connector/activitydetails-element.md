---
title: Elemento activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: O elemento activityDetails armazena os dados brutos de um único item de feed de atividade. Cada item de feed de atividades deve ter seu próprio elemento activityDetails. Os dados no elemento activityDetails são referenciados em modelos de atividade usando elementos Name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434869"
---
# <a name="activitydetails-element"></a><span data-ttu-id="a24da-105">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="a24da-105">activityDetails Element</span></span>

<span data-ttu-id="a24da-106">O elemento **activityDetails** armazena os dados brutos de um único item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="a24da-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="a24da-107">Cada item de feed de atividades deve ter seu próprio elemento **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="a24da-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="a24da-108">Os dados no elemento **activityDetails** são referenciados em modelos de atividade usando elementos **Name** .</span><span class="sxs-lookup"><span data-stu-id="a24da-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="a24da-109">Cada item de dados no elemento **activityDetails** deve ter um elemento **Name** .</span><span class="sxs-lookup"><span data-stu-id="a24da-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="a24da-110">A tabela a seguir descreve os seis elementos que o elemento **activityDetails** requer.</span><span class="sxs-lookup"><span data-stu-id="a24da-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="a24da-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a24da-111">**Element**</span></span>|<span data-ttu-id="a24da-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a24da-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a24da-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="a24da-113">**ownerID**</span></span> <br/> |<span data-ttu-id="a24da-114">A ID do usuário na rede social que gerou este item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="a24da-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="a24da-115">**IDs**</span><span class="sxs-lookup"><span data-stu-id="a24da-115">**objectID**</span></span> <br/> |<span data-ttu-id="a24da-116">Uma cadeia de caracteres exclusiva para o item de feed de atividade para detectar itens de feed duplicados.</span><span class="sxs-lookup"><span data-stu-id="a24da-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="a24da-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="a24da-117">**applicationId**</span></span> <br/> |<span data-ttu-id="a24da-118">Uma de duas IDs exclusivas que são usadas para corresponder ao item de feed de atividades com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="a24da-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="a24da-119">Se você tiver vários aplicativos ou outros agrupamentos, isso poderá ser usado como organizador de modelos de primeira camada.</span><span class="sxs-lookup"><span data-stu-id="a24da-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="a24da-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="a24da-120">**templateId**</span></span> <br/> |<span data-ttu-id="a24da-121">A segunda ID exclusiva usada para corresponder ao item de feed de atividades com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="a24da-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="a24da-122">Isso pode ser usado como organizador de modelos de segunda camada.</span><span class="sxs-lookup"><span data-stu-id="a24da-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="a24da-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="a24da-123">**publishDate**</span></span> <br/> |<span data-ttu-id="a24da-124">A data e a hora em que o item de feed de atividade foi publicado.</span><span class="sxs-lookup"><span data-stu-id="a24da-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="a24da-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="a24da-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="a24da-126">Os dados a serem usados nos tokens para o modelo de item do feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="a24da-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="a24da-127">Para obter um exemplo de XML de feed de atividades, consulte [exemplo de XML de feed de atividades](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="a24da-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a24da-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a24da-128">See also</span></span>

- [<span data-ttu-id="a24da-129">Visão geral do XML para um item do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="a24da-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="a24da-130">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="a24da-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="a24da-131">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="a24da-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="a24da-132">Diretrizes para exibir atividades de modo adequado</span><span class="sxs-lookup"><span data-stu-id="a24da-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="a24da-133">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="a24da-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="a24da-134">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="a24da-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="a24da-135">Desenvolvimento de um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="a24da-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

