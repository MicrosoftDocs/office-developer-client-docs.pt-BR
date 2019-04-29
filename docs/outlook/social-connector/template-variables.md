---
title: Variáveis do modelo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instâncias de variáveis de modelo (representadas por um elemento templateVariable) especificam os dados de um item de feed de atividade em um modelo de atividade.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404369"
---
# <a name="template-variables"></a><span data-ttu-id="12dc3-103">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="12dc3-103">Template variables</span></span>

<span data-ttu-id="12dc3-104">Instâncias de variáveis de modelo (representadas por um elemento **templateVariable** ) especificam os dados de um item de feed de atividade em um modelo de atividade.</span><span class="sxs-lookup"><span data-stu-id="12dc3-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="12dc3-105">Para obter um exemplo de XML de feed de atividades, consulte [exemplo de XML de feed de atividades](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="12dc3-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="12dc3-106">A tabela a seguir mostra os tipos de variáveis de modelo suportadas, cada uma representada pelo valor de enumeração XML correspondente.</span><span class="sxs-lookup"><span data-stu-id="12dc3-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="12dc3-107">**Tipo de variável de modelo**</span><span class="sxs-lookup"><span data-stu-id="12dc3-107">**Type of template variable**</span></span>|<span data-ttu-id="12dc3-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12dc3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12dc3-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="12dc3-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="12dc3-110">Uma pessoa, grupo ou item.</span><span class="sxs-lookup"><span data-stu-id="12dc3-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="12dc3-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="12dc3-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="12dc3-112">Um link.</span><span class="sxs-lookup"><span data-stu-id="12dc3-112">A link.</span></span>  <br/> |
|<span data-ttu-id="12dc3-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="12dc3-113">**listVariable**</span></span> <br/> |<span data-ttu-id="12dc3-114">Um grupo de objetos.</span><span class="sxs-lookup"><span data-stu-id="12dc3-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="12dc3-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="12dc3-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="12dc3-116">Uma imagem.</span><span class="sxs-lookup"><span data-stu-id="12dc3-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="12dc3-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="12dc3-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="12dc3-118">O fornecedor do item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="12dc3-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="12dc3-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="12dc3-119">**textVariable**</span></span> <br/> |<span data-ttu-id="12dc3-120">Um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="12dc3-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="12dc3-121">Cada tipo de variável de modelo tem elementos obrigatórios para especificar os dados da variável.</span><span class="sxs-lookup"><span data-stu-id="12dc3-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="12dc3-122">As variáveis de modelo são especificadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="12dc3-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="12dc3-123">Variável de modelo de lista</span><span class="sxs-lookup"><span data-stu-id="12dc3-123">List template variable</span></span>

<span data-ttu-id="12dc3-124">Você pode especificar variáveis de modelo que estão contidas em uma lista (delimitada pelos elementos **listVariable** e **ListItems** ) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="12dc3-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="12dc3-125">Uma variável de modelo do tipo **listVariable** é um contêiner para objetos.</span><span class="sxs-lookup"><span data-stu-id="12dc3-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="12dc3-126">Ele pode conter itens delimitados por vírgulas (do tipo **linkVariable** ou textVariable) ou imagens (do tipo **pictureVariable** ). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="12dc3-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="12dc3-127">As listas podem conter até cinco itens de link, cinco itens de texto ou cinco imagens.</span><span class="sxs-lookup"><span data-stu-id="12dc3-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="12dc3-128">O Outlook Social Connector (OSC) localiza itens de link ou de lista de texto de acordo com a localidade de sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="12dc3-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="12dc3-129">Para analisar e exibir corretamente as imagens em um item de feed de atividades, você deve incluir imagens em uma lista.</span><span class="sxs-lookup"><span data-stu-id="12dc3-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="12dc3-130">Todas as imagens são redimensionadas para serem 52 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="12dc3-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="12dc3-131">A largura da imagem não é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="12dc3-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="12dc3-132">Elementos de variável de modelo</span><span class="sxs-lookup"><span data-stu-id="12dc3-132">Template variable elements</span></span>

<span data-ttu-id="12dc3-133">Esta seção aborda os elementos obrigatórios e opcionais com suporte para cada tipo de variável de modelo.</span><span class="sxs-lookup"><span data-stu-id="12dc3-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="12dc3-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="12dc3-134">entityVariable</span></span>

|<span data-ttu-id="12dc3-135">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="12dc3-135">**Element**</span></span>|<span data-ttu-id="12dc3-136">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12dc3-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12dc3-137">**name**</span><span class="sxs-lookup"><span data-stu-id="12dc3-137">**name**</span></span> <br/> |<span data-ttu-id="12dc3-138">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="12dc3-138">The name of the variable.</span></span> <span data-ttu-id="12dc3-139">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-139">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-140">**id**</span><span class="sxs-lookup"><span data-stu-id="12dc3-140">**id**</span></span> <br/> |<span data-ttu-id="12dc3-141">A identificação exclusiva do usuário.</span><span class="sxs-lookup"><span data-stu-id="12dc3-141">The unique ID of the user.</span></span> <span data-ttu-id="12dc3-142">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-142">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="12dc3-143">**nameHint**</span></span> <br/> |<span data-ttu-id="12dc3-144">O nome a ser exibido no item de feed.</span><span class="sxs-lookup"><span data-stu-id="12dc3-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="12dc3-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="12dc3-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="12dc3-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="12dc3-147">A URL do perfil da pessoa que será usada como o hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente.</span><span class="sxs-lookup"><span data-stu-id="12dc3-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="12dc3-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="12dc3-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="12dc3-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="12dc3-150">O endereço de email usado para atualizar as informações de contato desta pessoa no Outlook.</span><span class="sxs-lookup"><span data-stu-id="12dc3-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="12dc3-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="12dc3-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="12dc3-152">linkVariable</span></span>

|<span data-ttu-id="12dc3-153">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="12dc3-153">**Element**</span></span>|<span data-ttu-id="12dc3-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12dc3-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12dc3-155">**name**</span><span class="sxs-lookup"><span data-stu-id="12dc3-155">**name**</span></span> <br/> |<span data-ttu-id="12dc3-156">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="12dc3-156">The name of the variable.</span></span> <span data-ttu-id="12dc3-157">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-157">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-158">**value**</span><span class="sxs-lookup"><span data-stu-id="12dc3-158">**value**</span></span> <br/> |<span data-ttu-id="12dc3-159">A URL para este link.</span><span class="sxs-lookup"><span data-stu-id="12dc3-159">The URL for this link.</span></span> <span data-ttu-id="12dc3-160">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-160">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-161">**text**</span><span class="sxs-lookup"><span data-stu-id="12dc3-161">**text**</span></span> <br/> |<span data-ttu-id="12dc3-162">O texto do link a ser exibido em vez da própria URL.</span><span class="sxs-lookup"><span data-stu-id="12dc3-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="12dc3-163">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="12dc3-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="12dc3-164">listVariable</span></span>

|<span data-ttu-id="12dc3-165">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="12dc3-165">**Element**</span></span>|<span data-ttu-id="12dc3-166">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12dc3-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12dc3-167">**name**</span><span class="sxs-lookup"><span data-stu-id="12dc3-167">**name**</span></span> <br/> |<span data-ttu-id="12dc3-168">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="12dc3-168">The name of the variable.</span></span> <span data-ttu-id="12dc3-169">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-169">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="12dc3-170">**listItems**</span></span> <br/> |<span data-ttu-id="12dc3-171">Um contêiner para itens na lista.</span><span class="sxs-lookup"><span data-stu-id="12dc3-171">A container for items in the list.</span></span> <span data-ttu-id="12dc3-172">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="12dc3-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="12dc3-173">pictureVariable</span></span>

|<span data-ttu-id="12dc3-174">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="12dc3-174">**Element**</span></span>|<span data-ttu-id="12dc3-175">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12dc3-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12dc3-176">**name**</span><span class="sxs-lookup"><span data-stu-id="12dc3-176">**name**</span></span> <br/> |<span data-ttu-id="12dc3-177">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="12dc3-177">The name of the variable.</span></span> <span data-ttu-id="12dc3-178">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-178">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-179">**value**</span><span class="sxs-lookup"><span data-stu-id="12dc3-179">**value**</span></span> <br/> |<span data-ttu-id="12dc3-180">A URL da imagem.</span><span class="sxs-lookup"><span data-stu-id="12dc3-180">The URL for the picture.</span></span> <span data-ttu-id="12dc3-181">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-181">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="12dc3-182">**altText**</span></span> <br/> |<span data-ttu-id="12dc3-183">O texto alternativo a ser exibido para acessibilidade e quando o usuário move o ponteiro do mouse sobre a imagem.</span><span class="sxs-lookup"><span data-stu-id="12dc3-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="12dc3-184">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="12dc3-185">**href**</span><span class="sxs-lookup"><span data-stu-id="12dc3-185">**href**</span></span> <br/> |<span data-ttu-id="12dc3-186">O hiperlink a ser usado quando o usuário clica na imagem, se o destino desejado não for a URL da imagem especificada pelo elemento **Value** .</span><span class="sxs-lookup"><span data-stu-id="12dc3-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="12dc3-187">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="12dc3-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="12dc3-188">publisherVariable</span></span>

|<span data-ttu-id="12dc3-189">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="12dc3-189">**Element**</span></span>|<span data-ttu-id="12dc3-190">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12dc3-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12dc3-191">**name**</span><span class="sxs-lookup"><span data-stu-id="12dc3-191">**name**</span></span> <br/> |<span data-ttu-id="12dc3-192">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="12dc3-192">The name of the variable.</span></span> <span data-ttu-id="12dc3-193">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-193">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-194">**id**</span><span class="sxs-lookup"><span data-stu-id="12dc3-194">**id**</span></span> <br/> |<span data-ttu-id="12dc3-195">A identificação exclusiva do usuário.</span><span class="sxs-lookup"><span data-stu-id="12dc3-195">The unique ID of the user.</span></span> <span data-ttu-id="12dc3-196">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-196">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="12dc3-197">**nameHint**</span></span> <br/> |<span data-ttu-id="12dc3-198">O nome a ser exibido no item de feed.</span><span class="sxs-lookup"><span data-stu-id="12dc3-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="12dc3-199">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="12dc3-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="12dc3-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="12dc3-201">A URL do perfil da pessoa que será usada como o hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente.</span><span class="sxs-lookup"><span data-stu-id="12dc3-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="12dc3-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="12dc3-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="12dc3-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="12dc3-204">O endereço de email usado para atualizar as informações de contato desta pessoa no Outlook.</span><span class="sxs-lookup"><span data-stu-id="12dc3-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="12dc3-205">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="12dc3-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="12dc3-206">textVariable</span></span>

|<span data-ttu-id="12dc3-207">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="12dc3-207">**Element**</span></span>|<span data-ttu-id="12dc3-208">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12dc3-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12dc3-209">**name**</span><span class="sxs-lookup"><span data-stu-id="12dc3-209">**name**</span></span> <br/> |<span data-ttu-id="12dc3-210">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="12dc3-210">The name of the variable.</span></span> <span data-ttu-id="12dc3-211">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12dc3-211">Required.</span></span>  <br/> |
|<span data-ttu-id="12dc3-212">**value**</span><span class="sxs-lookup"><span data-stu-id="12dc3-212">**value**</span></span> <br/> |<span data-ttu-id="12dc3-213">O texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="12dc3-213">The text to display.</span></span> <span data-ttu-id="12dc3-214">Opcional.</span><span class="sxs-lookup"><span data-stu-id="12dc3-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12dc3-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="12dc3-215">See also</span></span>

- [<span data-ttu-id="12dc3-216">Visão geral do XML para um item do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="12dc3-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="12dc3-217">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="12dc3-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="12dc3-218">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="12dc3-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="12dc3-219">Diretrizes para exibir atividades de modo adequado</span><span class="sxs-lookup"><span data-stu-id="12dc3-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="12dc3-220">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="12dc3-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="12dc3-221">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="12dc3-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="12dc3-222">Desenvolvimento de um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="12dc3-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

