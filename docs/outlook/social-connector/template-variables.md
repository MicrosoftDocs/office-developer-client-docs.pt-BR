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
# <a name="template-variables"></a><span data-ttu-id="48550-103">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="48550-103">Template variables</span></span>

<span data-ttu-id="48550-104">Instâncias de variáveis de modelo (representadas por um **elemento templateVariable)** especificam os dados de um item de feed de atividade em um modelo de atividade.</span><span class="sxs-lookup"><span data-stu-id="48550-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="48550-105">Para um exemplo de XML do feed de atividades, consulte [Exemplo XML do feed de atividades.](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="48550-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="48550-106">A tabela a seguir mostra os tipos de variáveis de modelo com suporte, cada uma representada pelo valor de enumeração XML correspondente.</span><span class="sxs-lookup"><span data-stu-id="48550-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="48550-107">**Tipo de variável de modelo**</span><span class="sxs-lookup"><span data-stu-id="48550-107">**Type of template variable**</span></span>|<span data-ttu-id="48550-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48550-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48550-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="48550-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="48550-110">Uma pessoa, grupo ou coisa.</span><span class="sxs-lookup"><span data-stu-id="48550-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="48550-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="48550-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="48550-112">Um link.</span><span class="sxs-lookup"><span data-stu-id="48550-112">A link.</span></span>  <br/> |
|<span data-ttu-id="48550-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="48550-113">**listVariable**</span></span> <br/> |<span data-ttu-id="48550-114">Um grupo de objetos.</span><span class="sxs-lookup"><span data-stu-id="48550-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="48550-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="48550-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="48550-116">Uma imagem.</span><span class="sxs-lookup"><span data-stu-id="48550-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="48550-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="48550-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="48550-118">O editor do item de feed de atividades.</span><span class="sxs-lookup"><span data-stu-id="48550-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="48550-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="48550-119">**textVariable**</span></span> <br/> |<span data-ttu-id="48550-120">Um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="48550-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="48550-121">Cada tipo de variável de modelo exigiu elementos para especificar os dados sobre essa variável.</span><span class="sxs-lookup"><span data-stu-id="48550-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="48550-122">As variáveis de modelo são especificadas da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="48550-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="48550-123">Variável de modelo de lista</span><span class="sxs-lookup"><span data-stu-id="48550-123">List template variable</span></span>

<span data-ttu-id="48550-124">Você pode especificar variáveis de modelo que estão contidas em uma lista (delimitada pelos elementos **listVariable** e **listItems)** da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="48550-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="48550-125">Uma variável de modelo do **tipo listVariable** é um contêiner para objetos.</span><span class="sxs-lookup"><span data-stu-id="48550-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="48550-126">Ele pode conter itens delimitados por vírgula (do tipo **linkVariable** ou **textVariable)** ou imagens (do tipo **pictureVariable).**</span><span class="sxs-lookup"><span data-stu-id="48550-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="48550-127">As listas podem conter até cinco itens de link, cinco itens de texto ou cinco imagens.</span><span class="sxs-lookup"><span data-stu-id="48550-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="48550-128">O Outlook Social Connector (OSC) localiza os itens de lista de texto ou link de acordo com a localidade do sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="48550-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="48550-129">Para analisar e exibir imagens corretamente em um item do feed de atividades, você deve incluir imagens em uma lista.</span><span class="sxs-lookup"><span data-stu-id="48550-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="48550-130">Todas as imagens são reorganizadas para ter 52 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="48550-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="48550-131">A largura da imagem não é re tamanhoada.</span><span class="sxs-lookup"><span data-stu-id="48550-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="48550-132">Modelos de elementos variáveis</span><span class="sxs-lookup"><span data-stu-id="48550-132">Template variable elements</span></span>

<span data-ttu-id="48550-133">Esta seção aborda os elementos obrigatórios e opcionais com suporte para cada tipo de variável de modelo.</span><span class="sxs-lookup"><span data-stu-id="48550-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="48550-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="48550-134">entityVariable</span></span>

|<span data-ttu-id="48550-135">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48550-135">**Element**</span></span>|<span data-ttu-id="48550-136">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48550-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48550-137">**name**</span><span class="sxs-lookup"><span data-stu-id="48550-137">**name**</span></span> <br/> |<span data-ttu-id="48550-138">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="48550-138">The name of the variable.</span></span> <span data-ttu-id="48550-139">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-139">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-140">**id**</span><span class="sxs-lookup"><span data-stu-id="48550-140">**id**</span></span> <br/> |<span data-ttu-id="48550-141">A ID exclusiva do usuário.</span><span class="sxs-lookup"><span data-stu-id="48550-141">The unique ID of the user.</span></span> <span data-ttu-id="48550-142">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-142">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="48550-143">**nameHint**</span></span> <br/> |<span data-ttu-id="48550-144">O nome a ser exibido no item de feed.</span><span class="sxs-lookup"><span data-stu-id="48550-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="48550-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="48550-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="48550-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="48550-147">A URL do perfil da pessoa que será usada como hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente.</span><span class="sxs-lookup"><span data-stu-id="48550-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="48550-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="48550-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="48550-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="48550-150">O endereço de email usado para atualizar as informações de contato dessa pessoa no Outlook.</span><span class="sxs-lookup"><span data-stu-id="48550-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="48550-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="48550-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="48550-152">linkVariable</span></span>

|<span data-ttu-id="48550-153">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48550-153">**Element**</span></span>|<span data-ttu-id="48550-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48550-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48550-155">**name**</span><span class="sxs-lookup"><span data-stu-id="48550-155">**name**</span></span> <br/> |<span data-ttu-id="48550-156">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="48550-156">The name of the variable.</span></span> <span data-ttu-id="48550-157">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-157">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-158">**value**</span><span class="sxs-lookup"><span data-stu-id="48550-158">**value**</span></span> <br/> |<span data-ttu-id="48550-159">A URL para este link.</span><span class="sxs-lookup"><span data-stu-id="48550-159">The URL for this link.</span></span> <span data-ttu-id="48550-160">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-160">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-161">**text**</span><span class="sxs-lookup"><span data-stu-id="48550-161">**text**</span></span> <br/> |<span data-ttu-id="48550-162">O texto do link a ser exibido em vez da PRÓPRIA URL.</span><span class="sxs-lookup"><span data-stu-id="48550-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="48550-163">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="48550-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="48550-164">listVariable</span></span>

|<span data-ttu-id="48550-165">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48550-165">**Element**</span></span>|<span data-ttu-id="48550-166">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48550-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48550-167">**name**</span><span class="sxs-lookup"><span data-stu-id="48550-167">**name**</span></span> <br/> |<span data-ttu-id="48550-168">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="48550-168">The name of the variable.</span></span> <span data-ttu-id="48550-169">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-169">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="48550-170">**listItems**</span></span> <br/> |<span data-ttu-id="48550-171">Um contêiner para itens na lista.</span><span class="sxs-lookup"><span data-stu-id="48550-171">A container for items in the list.</span></span> <span data-ttu-id="48550-172">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="48550-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="48550-173">pictureVariable</span></span>

|<span data-ttu-id="48550-174">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48550-174">**Element**</span></span>|<span data-ttu-id="48550-175">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48550-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48550-176">**name**</span><span class="sxs-lookup"><span data-stu-id="48550-176">**name**</span></span> <br/> |<span data-ttu-id="48550-177">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="48550-177">The name of the variable.</span></span> <span data-ttu-id="48550-178">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-178">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-179">**value**</span><span class="sxs-lookup"><span data-stu-id="48550-179">**value**</span></span> <br/> |<span data-ttu-id="48550-180">A URL da imagem.</span><span class="sxs-lookup"><span data-stu-id="48550-180">The URL for the picture.</span></span> <span data-ttu-id="48550-181">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-181">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="48550-182">**altText**</span></span> <br/> |<span data-ttu-id="48550-183">O texto alternativo a ser exibido para acessibilidade e quando o usuário move o ponteiro do mouse sobre a imagem.</span><span class="sxs-lookup"><span data-stu-id="48550-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="48550-184">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="48550-185">**href**</span><span class="sxs-lookup"><span data-stu-id="48550-185">**href**</span></span> <br/> |<span data-ttu-id="48550-186">O hiperlink a ser usado quando o usuário clica na imagem, se o destino desejado não for a URL da imagem especificada pelo **elemento de** valor.</span><span class="sxs-lookup"><span data-stu-id="48550-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="48550-187">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="48550-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="48550-188">publisherVariable</span></span>

|<span data-ttu-id="48550-189">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48550-189">**Element**</span></span>|<span data-ttu-id="48550-190">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48550-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48550-191">**name**</span><span class="sxs-lookup"><span data-stu-id="48550-191">**name**</span></span> <br/> |<span data-ttu-id="48550-192">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="48550-192">The name of the variable.</span></span> <span data-ttu-id="48550-193">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-193">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-194">**id**</span><span class="sxs-lookup"><span data-stu-id="48550-194">**id**</span></span> <br/> |<span data-ttu-id="48550-195">A ID exclusiva do usuário.</span><span class="sxs-lookup"><span data-stu-id="48550-195">The unique ID of the user.</span></span> <span data-ttu-id="48550-196">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-196">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="48550-197">**nameHint**</span></span> <br/> |<span data-ttu-id="48550-198">O nome a ser exibido no item de feed.</span><span class="sxs-lookup"><span data-stu-id="48550-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="48550-199">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="48550-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="48550-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="48550-201">A URL do perfil da pessoa que será usada como hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente.</span><span class="sxs-lookup"><span data-stu-id="48550-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="48550-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="48550-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="48550-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="48550-204">O endereço de email usado para atualizar as informações de contato dessa pessoa no Outlook.</span><span class="sxs-lookup"><span data-stu-id="48550-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="48550-205">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="48550-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="48550-206">textVariable</span></span>

|<span data-ttu-id="48550-207">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48550-207">**Element**</span></span>|<span data-ttu-id="48550-208">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48550-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48550-209">**name**</span><span class="sxs-lookup"><span data-stu-id="48550-209">**name**</span></span> <br/> |<span data-ttu-id="48550-210">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="48550-210">The name of the variable.</span></span> <span data-ttu-id="48550-211">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48550-211">Required.</span></span>  <br/> |
|<span data-ttu-id="48550-212">**value**</span><span class="sxs-lookup"><span data-stu-id="48550-212">**value**</span></span> <br/> |<span data-ttu-id="48550-213">O texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="48550-213">The text to display.</span></span> <span data-ttu-id="48550-214">Opcional.</span><span class="sxs-lookup"><span data-stu-id="48550-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48550-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="48550-215">See also</span></span>

- [<span data-ttu-id="48550-216">Visão geral do XML para um item do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="48550-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="48550-217">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="48550-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="48550-218">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="48550-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="48550-219">Diretrizes para a exibição adequada das atividades</span><span class="sxs-lookup"><span data-stu-id="48550-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="48550-220">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="48550-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="48550-221">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="48550-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="48550-222">Como desenvolver um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="48550-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

