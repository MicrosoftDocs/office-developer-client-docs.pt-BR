---
title: Exemplo de XML do feed de atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: O exemplo XML neste tópico é uma feed de atividades de cadeia XML retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialSession2::GetActivitiesEx para uma rede social.
ms.openlocfilehash: 6370b559c5160bfa48d32afa77715e9a7c126aab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281329"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="b7b7d-103">Exemplo de XML do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="b7b7d-103">Activity Feed XML Example</span></span>

<span data-ttu-id="b7b7d-104">O exemplo XML neste tópico é uma feed de atividades de cadeia XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="b7b7d-105">O exemplo mostra o**feed de atividades**XML que contém as seguintes quatro atividades, sendo cada uma delas  delimitadas pelo elemento**activityDetails**e correspondendo a um modelo para fins de exibição:</span><span class="sxs-lookup"><span data-stu-id="b7b7d-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="b7b7d-106">Uma imagem de perfil atualizada por Melissa Mello cujo **ownerID** na rede social é 4667647.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="b7b7d-107">Essa atividade especifica três variáveis de modelo do tipo **publisherVariable**, **listVariable**, e **pictureVariable** (delimitado no \*\* listVariable\*\*).</span><span class="sxs-lookup"><span data-stu-id="b7b7d-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="b7b7d-108">Essa variáveis especificam a pessoa que publicou o item e as informações para a imagem que será atualizada no feed de atividades (usando o **nome**, **valor**, **altText**e os elemento filhos**href** de **pictureVariable**).</span><span class="sxs-lookup"><span data-stu-id="b7b7d-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="b7b7d-109">Uma imagem de perfil é atualizada por Mateus Vaz cujo**ownerID** na rede social é 5015012.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="b7b7d-110">Assim como a última atividade, essa atividade especifica três variáveis de modelo do tipo **publisherVariable**, **listVariable**, e **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="b7b7d-111">Essa variáveis especificam a pessoa que publicou o item e as informações para a imagem que será atualizada no feed de atividades.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="b7b7d-112">Uma atualização de status Mateus Vaz mostrando o mesmo **ownerID** de 5015012, como na última atividade.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="b7b7d-113">Essa atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="b7b7d-114">**publisherVariable** Especifica a pessoa que publicou o item, feed de atividades e **textVariable** inclui um **valor** da linha de status  `is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="b7b7d-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="b7b7d-115">Uma postagem no blog por Mateus Vaz mostrando o mesmo **ownerID** 5015012 como nas duas últimas atividades.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="b7b7d-116">Essa atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **linkVariable**.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="b7b7d-117">**publisherVariable** Especifica a pessoa que publicou o item no feed de atividades e **linkVariable** inclui mais informações (especificado, o **nome**, **texto**, e **valor** dos elementos filhos de **linkVariable**) sobre a postagem do blog.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="b7b7d-118">Cada uma das quatro atividades especifica um valor **TemplateId do**que corresponde a um dos três modelos especificados no elemento **modelos**.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="b7b7d-119">Cada modelo está no seu próprio elemento**activityTemplateContainer**identificado por um  valor**TemplateId**que também é usado para exibir uma atividade com o mesmo valor**TemplateId**.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="b7b7d-120">Para obter uma descrição detalhada dos elementos XML usados no exemplo, confira os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="b7b7d-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="b7b7d-121">Visão geral do XML para um item do feed de atividades</span><span class="sxs-lookup"><span data-stu-id="b7b7d-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="b7b7d-122">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="b7b7d-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="b7b7d-123">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="b7b7d-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="b7b7d-124">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="b7b7d-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="b7b7d-125">Exemplos de XML</span><span class="sxs-lookup"><span data-stu-id="b7b7d-125">XML example</span></span>

<span data-ttu-id="b7b7d-126">O exemplo a seguir mostra o XML**feed de atividades** de quatro atividades: duas atualizações de imagem de perfil, uma atualização de status e uma postagem de blog.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="b7b7d-127">O XML também especifica três modelos de exibição de atividade para exibir as atividades correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b7b7d-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>https://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="b7b7d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7b7d-128">See also</span></span>

- [<span data-ttu-id="b7b7d-129">Exemplos de XML de provedor OSC</span><span class="sxs-lookup"><span data-stu-id="b7b7d-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="b7b7d-130">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="b7b7d-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="b7b7d-131">Exemplo de XML de recursos</span><span class="sxs-lookup"><span data-stu-id="b7b7d-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="b7b7d-132">Exemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="b7b7d-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="b7b7d-133">Esquema XML do provedor Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b7b7d-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

