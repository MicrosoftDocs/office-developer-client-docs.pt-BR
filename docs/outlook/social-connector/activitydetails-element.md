---
title: activityDetails elemento
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: O elemento activityDetails armazena os dados brutos para um item de feed de atividade único. Cada item de feed de atividade deve ter seu próprio elemento activityDetails. Dados no elemento activityDetails referenciados nos modelos de atividade usando nomes de elementos.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770825"
---
# <a name="activitydetails-element"></a><span data-ttu-id="ca55d-105">activityDetails elemento</span><span class="sxs-lookup"><span data-stu-id="ca55d-105">activityDetails Element</span></span>

<span data-ttu-id="ca55d-106">O elemento **activityDetails** armazena os dados brutos para um item de feed de atividade único.</span><span class="sxs-lookup"><span data-stu-id="ca55d-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="ca55d-107">Cada item de feed de atividade deve ter seu próprio elemento **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="ca55d-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="ca55d-108">Dados no elemento **activityDetails** referenciados nos modelos de atividade usando **nomes** de elementos.</span><span class="sxs-lookup"><span data-stu-id="ca55d-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="ca55d-109">Cada parte dos dados no elemento **activityDetails** deve ter um elemento **name** .</span><span class="sxs-lookup"><span data-stu-id="ca55d-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="ca55d-110">A tabela a seguir descreve os elementos de seis que requer o elemento **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="ca55d-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="ca55d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ca55d-111">**Element**</span></span>|<span data-ttu-id="ca55d-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ca55d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca55d-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="ca55d-113">**ownerID**</span></span> <br/> |<span data-ttu-id="ca55d-114">A ID do usuário na rede social que gerou essa atividade feed item.</span><span class="sxs-lookup"><span data-stu-id="ca55d-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="ca55d-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="ca55d-115">**objectID**</span></span> <br/> |<span data-ttu-id="ca55d-116">Uma cadeia de caracteres exclusiva da atividade de alimentação item para detectar itens de feed de duplicata.</span><span class="sxs-lookup"><span data-stu-id="ca55d-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="ca55d-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="ca55d-117">**applicationId**</span></span> <br/> |<span data-ttu-id="ca55d-118">Uma das duas identificações exclusivas que são usadas para corresponder a atividade feed item com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="ca55d-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="ca55d-119">Se você tiver vários aplicativos ou outros agrupamentos, isso pode ser usado como um organizador de modelo de primeiro nível.</span><span class="sxs-lookup"><span data-stu-id="ca55d-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="ca55d-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="ca55d-120">**templateId**</span></span> <br/> |<span data-ttu-id="ca55d-121">A segunda identificação exclusiva que será usada para corresponder a atividade feed item com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="ca55d-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="ca55d-122">Isso pode ser usado como um organizador de modelo de segundo nível.</span><span class="sxs-lookup"><span data-stu-id="ca55d-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="ca55d-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="ca55d-123">**publishDate**</span></span> <br/> |<span data-ttu-id="ca55d-124">A data e hora em que o item de feed de atividade foi publicado.</span><span class="sxs-lookup"><span data-stu-id="ca55d-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="ca55d-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="ca55d-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="ca55d-126">Os dados a serem usados em tokens para o modelo de itens de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="ca55d-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="ca55d-127">Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="ca55d-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca55d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca55d-128">See also</span></span>

- [<span data-ttu-id="ca55d-129">Visão geral de XML para uma atividade Feed Item</span><span class="sxs-lookup"><span data-stu-id="ca55d-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="ca55d-130">activityTemplateContainer elemento</span><span class="sxs-lookup"><span data-stu-id="ca55d-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="ca55d-131">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="ca55d-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="ca55d-132">Diretrizes para exibir adequadamente atividades</span><span class="sxs-lookup"><span data-stu-id="ca55d-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="ca55d-133">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="ca55d-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="ca55d-134">Esquema XML do Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="ca55d-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="ca55d-135">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="ca55d-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

