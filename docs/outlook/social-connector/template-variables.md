---
title: Variáveis do modelo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instâncias de variáveis de modelo de (representadas por um elemento templateVariable) especificam os dados de um item de feed em um modelo de atividade de atividade.
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770975"
---
# <a name="template-variables"></a><span data-ttu-id="59b77-103">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="59b77-103">Template variables</span></span>

<span data-ttu-id="59b77-104">Instâncias de variáveis de modelo de (representadas por um elemento **templateVariable** ) especificam os dados de um item de feed em um modelo de atividade de atividade.</span><span class="sxs-lookup"><span data-stu-id="59b77-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="59b77-105">Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="59b77-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="59b77-106">A tabela a seguir mostra os tipos de variáveis de modelo com suporte, que cada um representado pelo valor de enumeração XML correspondente.</span><span class="sxs-lookup"><span data-stu-id="59b77-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="59b77-107">**Tipo de variável do modelo**</span><span class="sxs-lookup"><span data-stu-id="59b77-107">**Type of template variable**</span></span>|<span data-ttu-id="59b77-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="59b77-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59b77-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="59b77-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="59b77-110">Uma pessoa, grupo ou coisa.</span><span class="sxs-lookup"><span data-stu-id="59b77-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="59b77-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="59b77-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="59b77-112">Um vínculo.</span><span class="sxs-lookup"><span data-stu-id="59b77-112">A link.</span></span>  <br/> |
|<span data-ttu-id="59b77-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="59b77-113">**listVariable**</span></span> <br/> |<span data-ttu-id="59b77-114">Um grupo de objetos.</span><span class="sxs-lookup"><span data-stu-id="59b77-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="59b77-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="59b77-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="59b77-116">Uma imagem.</span><span class="sxs-lookup"><span data-stu-id="59b77-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="59b77-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="59b77-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="59b77-118">O publisher da atividade de alimentação item.</span><span class="sxs-lookup"><span data-stu-id="59b77-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="59b77-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="59b77-119">**textVariable**</span></span> <br/> |<span data-ttu-id="59b77-120">Um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="59b77-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="59b77-121">Cada tipo de variável do modelo é obrigatório elementos para especificar os dados sobre essa variável.</span><span class="sxs-lookup"><span data-stu-id="59b77-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="59b77-122">Variáveis de modelo são especificadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="59b77-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="59b77-123">Variável de modelo de lista</span><span class="sxs-lookup"><span data-stu-id="59b77-123">List template variable</span></span>

<span data-ttu-id="59b77-124">Você pode especificar variáveis de modelo que estão contidas dentro de uma lista (delimitada pelos elementos **listVariable** e **listItems** ) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="59b77-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="59b77-125">Uma variável de modelo do tipo **listVariable** é um contêiner para objetos.</span><span class="sxs-lookup"><span data-stu-id="59b77-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="59b77-126">Ele pode conter itens delimitado por vírgula (do tipo **linkVariable** ou **textVariable** ) ou imagens (do tipo **pictureVariable** ).</span><span class="sxs-lookup"><span data-stu-id="59b77-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="59b77-127">Listas podem conter até cinco vincular itens, cinco itens de texto ou imagens de cinco.</span><span class="sxs-lookup"><span data-stu-id="59b77-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="59b77-128">Outlook Social Connector (OSC) localiza o texto ou vincular itens de lista de acordo com a localidade do sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="59b77-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="59b77-129">Para corretamente, analisar e exibir imagens em uma item de feed de atividade, você deve incluir as imagens em uma lista.</span><span class="sxs-lookup"><span data-stu-id="59b77-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="59b77-130">Todas as imagens são redimensionadas para ser 52 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="59b77-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="59b77-131">A largura da imagem não é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="59b77-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="59b77-132">Elementos de variáveis de modelo</span><span class="sxs-lookup"><span data-stu-id="59b77-132">Template variable elements</span></span>

<span data-ttu-id="59b77-133">Esta seção aborda os elementos obrigatórios e opcionais com suporte para cada tipo de variável do modelo.</span><span class="sxs-lookup"><span data-stu-id="59b77-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="59b77-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="59b77-134">entityVariable</span></span>

|<span data-ttu-id="59b77-135">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59b77-135">**Element**</span></span>|<span data-ttu-id="59b77-136">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="59b77-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59b77-137">**name**</span><span class="sxs-lookup"><span data-stu-id="59b77-137">**name**</span></span> <br/> |<span data-ttu-id="59b77-138">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="59b77-138">The name of the variable.</span></span> <span data-ttu-id="59b77-139">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-139">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-140">**id**</span><span class="sxs-lookup"><span data-stu-id="59b77-140">**id**</span></span> <br/> |<span data-ttu-id="59b77-141">A ID exclusiva do usuário.</span><span class="sxs-lookup"><span data-stu-id="59b77-141">The unique ID of the user.</span></span> <span data-ttu-id="59b77-142">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-142">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="59b77-143">**nameHint**</span></span> <br/> |<span data-ttu-id="59b77-144">O nome a ser exibido no item de feed.</span><span class="sxs-lookup"><span data-stu-id="59b77-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="59b77-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="59b77-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="59b77-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="59b77-147">A URL do perfil da pessoa que será usado como o hiperlink para o nome da pessoa no item feed, se o nome da pessoa estiver presente.</span><span class="sxs-lookup"><span data-stu-id="59b77-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="59b77-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="59b77-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="59b77-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="59b77-150">O endereço de email que será usado para atualizar as informações de contato dessa pessoa no Outlook.</span><span class="sxs-lookup"><span data-stu-id="59b77-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="59b77-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="59b77-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="59b77-152">linkVariable</span></span>

|<span data-ttu-id="59b77-153">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59b77-153">**Element**</span></span>|<span data-ttu-id="59b77-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="59b77-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59b77-155">**name**</span><span class="sxs-lookup"><span data-stu-id="59b77-155">**name**</span></span> <br/> |<span data-ttu-id="59b77-156">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="59b77-156">The name of the variable.</span></span> <span data-ttu-id="59b77-157">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-157">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-158">**value**</span><span class="sxs-lookup"><span data-stu-id="59b77-158">**value**</span></span> <br/> |<span data-ttu-id="59b77-159">A URL para este link.</span><span class="sxs-lookup"><span data-stu-id="59b77-159">The URL for this link.</span></span> <span data-ttu-id="59b77-160">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-160">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-161">**text**</span><span class="sxs-lookup"><span data-stu-id="59b77-161">**text**</span></span> <br/> |<span data-ttu-id="59b77-162">O texto do link para exibir, em vez da própria URL.</span><span class="sxs-lookup"><span data-stu-id="59b77-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="59b77-163">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="59b77-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="59b77-164">listVariable</span></span>

|<span data-ttu-id="59b77-165">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59b77-165">**Element**</span></span>|<span data-ttu-id="59b77-166">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="59b77-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59b77-167">**name**</span><span class="sxs-lookup"><span data-stu-id="59b77-167">**name**</span></span> <br/> |<span data-ttu-id="59b77-168">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="59b77-168">The name of the variable.</span></span> <span data-ttu-id="59b77-169">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-169">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="59b77-170">**listItems**</span></span> <br/> |<span data-ttu-id="59b77-171">Um contêiner para itens na lista.</span><span class="sxs-lookup"><span data-stu-id="59b77-171">A container for items in the list.</span></span> <span data-ttu-id="59b77-172">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="59b77-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="59b77-173">pictureVariable</span></span>

|<span data-ttu-id="59b77-174">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59b77-174">**Element**</span></span>|<span data-ttu-id="59b77-175">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="59b77-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59b77-176">**name**</span><span class="sxs-lookup"><span data-stu-id="59b77-176">**name**</span></span> <br/> |<span data-ttu-id="59b77-177">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="59b77-177">The name of the variable.</span></span> <span data-ttu-id="59b77-178">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-178">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-179">**value**</span><span class="sxs-lookup"><span data-stu-id="59b77-179">**value**</span></span> <br/> |<span data-ttu-id="59b77-180">A URL da imagem.</span><span class="sxs-lookup"><span data-stu-id="59b77-180">The URL for the picture.</span></span> <span data-ttu-id="59b77-181">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-181">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="59b77-182">**altText**</span></span> <br/> |<span data-ttu-id="59b77-183">O texto alternativo para exibir a acessibilidade e quando o usuário move o ponteiro do mouse sobre a imagem.</span><span class="sxs-lookup"><span data-stu-id="59b77-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="59b77-184">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="59b77-185">**href**</span><span class="sxs-lookup"><span data-stu-id="59b77-185">**href**</span></span> <br/> |<span data-ttu-id="59b77-186">O hiperlink a ser usado quando o usuário clica a imagem, se o destino desejado não é a URL da imagem especificada pelo **valor de** elemento.</span><span class="sxs-lookup"><span data-stu-id="59b77-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="59b77-187">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="59b77-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="59b77-188">publisherVariable</span></span>

|<span data-ttu-id="59b77-189">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59b77-189">**Element**</span></span>|<span data-ttu-id="59b77-190">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="59b77-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59b77-191">**name**</span><span class="sxs-lookup"><span data-stu-id="59b77-191">**name**</span></span> <br/> |<span data-ttu-id="59b77-192">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="59b77-192">The name of the variable.</span></span> <span data-ttu-id="59b77-193">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-193">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-194">**id**</span><span class="sxs-lookup"><span data-stu-id="59b77-194">**id**</span></span> <br/> |<span data-ttu-id="59b77-195">A ID exclusiva do usuário.</span><span class="sxs-lookup"><span data-stu-id="59b77-195">The unique ID of the user.</span></span> <span data-ttu-id="59b77-196">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-196">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="59b77-197">**nameHint**</span></span> <br/> |<span data-ttu-id="59b77-198">O nome a ser exibido no item de feed.</span><span class="sxs-lookup"><span data-stu-id="59b77-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="59b77-199">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="59b77-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="59b77-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="59b77-201">A URL do perfil da pessoa que será usado como o hiperlink para o nome da pessoa no item feed, se o nome da pessoa estiver presente.</span><span class="sxs-lookup"><span data-stu-id="59b77-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="59b77-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="59b77-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="59b77-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="59b77-204">O endereço de email que será usado para atualizar as informações de contato dessa pessoa no Outlook.</span><span class="sxs-lookup"><span data-stu-id="59b77-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="59b77-205">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="59b77-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="59b77-206">textVariable</span></span>

|<span data-ttu-id="59b77-207">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59b77-207">**Element**</span></span>|<span data-ttu-id="59b77-208">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="59b77-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59b77-209">**name**</span><span class="sxs-lookup"><span data-stu-id="59b77-209">**name**</span></span> <br/> |<span data-ttu-id="59b77-210">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="59b77-210">The name of the variable.</span></span> <span data-ttu-id="59b77-211">Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="59b77-211">Required.</span></span>  <br/> |
|<span data-ttu-id="59b77-212">**value**</span><span class="sxs-lookup"><span data-stu-id="59b77-212">**value**</span></span> <br/> |<span data-ttu-id="59b77-213">O texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="59b77-213">The text to display.</span></span> <span data-ttu-id="59b77-214">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59b77-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59b77-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="59b77-215">See also</span></span>

- [<span data-ttu-id="59b77-216">Visão geral de XML para uma atividade Feed Item</span><span class="sxs-lookup"><span data-stu-id="59b77-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="59b77-217">activityDetails elemento</span><span class="sxs-lookup"><span data-stu-id="59b77-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="59b77-218">activityTemplateContainer elemento</span><span class="sxs-lookup"><span data-stu-id="59b77-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="59b77-219">Diretrizes para exibir adequadamente atividades</span><span class="sxs-lookup"><span data-stu-id="59b77-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="59b77-220">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="59b77-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="59b77-221">Esquema XML do Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="59b77-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="59b77-222">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="59b77-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

