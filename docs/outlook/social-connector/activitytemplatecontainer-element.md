---
title: activityTemplateContainer elemento
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Um elemento activityTemplateContainer é um modelo que permite que você formatar itens do seu feed de atividade e reutilizar XML que especifica um layout.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770828"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="693cb-103">activityTemplateContainer elemento</span><span class="sxs-lookup"><span data-stu-id="693cb-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="693cb-104">Um elemento **activityTemplateContainer** é um modelo que permite que você formatar itens do seu feed de atividade e reutilizar XML que especifica um layout.</span><span class="sxs-lookup"><span data-stu-id="693cb-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="693cb-105">Use os IDs (**applicationID** e **templateID**) para corresponder a um item de feed (**activityDetails**) a um modelo (**activityTemplateContainer**).</span><span class="sxs-lookup"><span data-stu-id="693cb-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="693cb-106">Armazene os dados de layout como parte do elemento **activityTemplate** .</span><span class="sxs-lookup"><span data-stu-id="693cb-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="693cb-107">Para fazer referência a dados retirados da item de feed de atividade individual, use as variáveis de modelo como espaços reservados para informações como pessoas, links e texto.</span><span class="sxs-lookup"><span data-stu-id="693cb-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="693cb-108">A tabela a seguir descreve os três elementos que requer o elemento **activityTemplateContainer** .</span><span class="sxs-lookup"><span data-stu-id="693cb-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="693cb-109">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="693cb-109">**Element**</span></span>|<span data-ttu-id="693cb-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="693cb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="693cb-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="693cb-111">**applicationID**</span></span> <br/> |<span data-ttu-id="693cb-112">Uma das duas identificações exclusivas que são usadas para corresponder os itens de feed com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="693cb-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="693cb-113">Se você tiver vários aplicativos ou outros agrupamentos, isso pode ser usado como um organizador de modelo de primeiro nível.</span><span class="sxs-lookup"><span data-stu-id="693cb-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="693cb-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="693cb-114">**templateID**</span></span> <br/> |<span data-ttu-id="693cb-115">A segunda identificação exclusiva que será usada para corresponder os itens de feed com seu modelo.</span><span class="sxs-lookup"><span data-stu-id="693cb-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="693cb-116">Isso pode ser usado como um organizador de modelo de segundo nível.</span><span class="sxs-lookup"><span data-stu-id="693cb-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="693cb-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="693cb-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="693cb-118">O layout do modelo de (**ícone**, **título**e **dados** elementos) e o tipo de atividade (**tipo de** elemento).</span><span class="sxs-lookup"><span data-stu-id="693cb-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="693cb-119">A tabela a seguir descreve os elementos filho de **activityTemplate**, que descrevem o layout e o tipo de um modelo.</span><span class="sxs-lookup"><span data-stu-id="693cb-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="693cb-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="693cb-120">**Element**</span></span>|<span data-ttu-id="693cb-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="693cb-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="693cb-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="693cb-122">**icon**</span></span> <br/> |<span data-ttu-id="693cb-123">Um token de link, que faz referência a URL para o ícone para esse item de feed.</span><span class="sxs-lookup"><span data-stu-id="693cb-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="693cb-124">**title**</span><span class="sxs-lookup"><span data-stu-id="693cb-124">**title**</span></span> <br/> |<span data-ttu-id="693cb-125">As informações necessárias para o item de feed.</span><span class="sxs-lookup"><span data-stu-id="693cb-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="693cb-126">**tipo**</span><span class="sxs-lookup"><span data-stu-id="693cb-126">**type**</span></span> <br/> |<span data-ttu-id="693cb-127">O tipo de atividade, como uma atualização de status, foto ou documento.</span><span class="sxs-lookup"><span data-stu-id="693cb-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="693cb-128">**data**</span><span class="sxs-lookup"><span data-stu-id="693cb-128">**data**</span></span> <br/> |<span data-ttu-id="693cb-129">Informações adicionais para o item de feed, como imagens, texto ou links.</span><span class="sxs-lookup"><span data-stu-id="693cb-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="693cb-130">Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="693cb-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="693cb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="693cb-131">See also</span></span>

- [<span data-ttu-id="693cb-132">Visão geral de XML para uma atividade Feed Item</span><span class="sxs-lookup"><span data-stu-id="693cb-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="693cb-133">activityDetails elemento</span><span class="sxs-lookup"><span data-stu-id="693cb-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="693cb-134">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="693cb-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="693cb-135">Diretrizes para exibir adequadamente atividades</span><span class="sxs-lookup"><span data-stu-id="693cb-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="693cb-136">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="693cb-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="693cb-137">Esquema XML do Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="693cb-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="693cb-138">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="693cb-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

