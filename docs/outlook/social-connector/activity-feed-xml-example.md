---
title: Exemplo de XML de Feed de atividade
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: O exemplo de XML neste tópico é a que cadeia de caracteres XML retornada para o Outlook Social Connector (OSC) depois de chamar o método ISocialSession2::GetActivitiesEx para uma rede social de feed de uma atividade.
ms.openlocfilehash: ab27ddfad5044994a19bb32759994a0e98c39ae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770816"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="d9fff-103">Exemplo de XML de Feed de atividade</span><span class="sxs-lookup"><span data-stu-id="d9fff-103">Activity Feed XML Example</span></span>

<span data-ttu-id="d9fff-104">O exemplo de XML deste tópico é uma cadeia de caracteres XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para uma rede social de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="d9fff-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="d9fff-105">O exemplo mostra o **feed de atividades** XML que contém as seguintes atividades de quatro, cada delimitados por elemento **activityDetails** e correspondência de um modelo para fins de exibição:</span><span class="sxs-lookup"><span data-stu-id="d9fff-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="d9fff-106">Atualizar uma imagem de perfil Melissa Macbeth, cujo **ownerID** na rede social é 4667647.</span><span class="sxs-lookup"><span data-stu-id="d9fff-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="d9fff-107">Esta atividade especifica três variáveis do modelo de tipo **publisherVariable**, **listVariable**e **pictureVariable** (que está contido em **listVariable**).</span><span class="sxs-lookup"><span data-stu-id="d9fff-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="d9fff-108">Especificam a pessoa que publicado a informações de imagem para serem atualizadas (usando os elementos de filho **href** , **valor**, **altText**e **nome**de **pictureVariable**) e item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="d9fff-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="d9fff-109">Atualizar uma imagem de perfil Michael Affronti cujo **ownerID** na rede social é 5015012.</span><span class="sxs-lookup"><span data-stu-id="d9fff-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="d9fff-110">Semelhante à última atividade, essa atividade especifica três variáveis do modelo de tipo **publisherVariable**, **listVariable**e **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="d9fff-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="d9fff-111">Especificam a pessoa que publicado a informações da imagem a ser atualizado e o item de feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="d9fff-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="d9fff-112">Uma atualização de status por Michael Affronti, mostrando o mesmo **ownerID** de 5015012 como a última atividade.</span><span class="sxs-lookup"><span data-stu-id="d9fff-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="d9fff-113">Esta atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="d9fff-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="d9fff-114">**publisherVariable** Especifica a pessoa que publicado a item de feed de atividade e **textVariable** inclui um **valor** de linha de status`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="d9fff-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="d9fff-115">Uma postagem de blog por Michael Affronti, mostrando o mesmo **ownerID** de 5015012 como as duas últimas atividades.</span><span class="sxs-lookup"><span data-stu-id="d9fff-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="d9fff-116">Esta atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **linkVariable**.</span><span class="sxs-lookup"><span data-stu-id="d9fff-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="d9fff-117">**publisherVariable** Especifica a pessoa que publicou a atividade de item de feed e **linkVariable** inclui ainda mais informações (especificadas pelos elementos filho de **nome**, o **texto**e o **valor** de **linkVariable**) sobre a postagem do blog.</span><span class="sxs-lookup"><span data-stu-id="d9fff-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="d9fff-118">Cada uma das quatro atividades Especifica um valor de **templateID** , que corresponde a um dos três modelos especificados pelo elemento **modelos** .</span><span class="sxs-lookup"><span data-stu-id="d9fff-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="d9fff-119">Cada modelo está em seu próprio elemento **activityTemplateContainer** , identificado por um valor **templateID** que também é usado para exibir uma atividade que tem o mesmo valor de **templateID** .</span><span class="sxs-lookup"><span data-stu-id="d9fff-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="d9fff-120">Para obter uma descrição detalhada dos elementos XML usados no exemplo, consulte os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="d9fff-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="d9fff-121">Visão geral de XML para uma atividade Feed Item</span><span class="sxs-lookup"><span data-stu-id="d9fff-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="d9fff-122">activityDetails elemento</span><span class="sxs-lookup"><span data-stu-id="d9fff-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="d9fff-123">activityTemplateContainer elemento</span><span class="sxs-lookup"><span data-stu-id="d9fff-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="d9fff-124">Variáveis do modelo</span><span class="sxs-lookup"><span data-stu-id="d9fff-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="d9fff-125">Exemplo XML</span><span class="sxs-lookup"><span data-stu-id="d9fff-125">XML example</span></span>

<span data-ttu-id="d9fff-126">O exemplo a seguir mostra o **feed de atividades** XML de quatro atividades: dois perfis atualizações de imagem, uma atualização de status e uma postagem de blog.</span><span class="sxs-lookup"><span data-stu-id="d9fff-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="d9fff-127">O XML também especifica os três modelos de exibição de atividades para exibir as atividades correspondentes.</span><span class="sxs-lookup"><span data-stu-id="d9fff-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
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
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
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
          <profileUrl>http://www.contoso.com</profileUrl>
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
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>http://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
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
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="d9fff-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9fff-128">See also</span></span>

- [<span data-ttu-id="d9fff-129">Exemplos XML de provedor do OSC</span><span class="sxs-lookup"><span data-stu-id="d9fff-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="d9fff-130">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="d9fff-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="d9fff-131">Exemplo de XML de recursos</span><span class="sxs-lookup"><span data-stu-id="d9fff-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="d9fff-132">Exemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="d9fff-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="d9fff-133">Esquema XML do Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="d9fff-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

