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
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538323"
---
# <a name="activity-feed-xml-example"></a>Exemplo de XML do feed de atividades

O exemplo XML neste tópico é uma feed de atividades de cadeia XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para uma rede social. 
  
O exemplo mostra o **feed de atividades** XML que contém as seguintes quatro atividades, sendo cada uma delas  delimitadas pelo elemento **activityDetails** e correspondendo a um modelo para fins de exibição: 
  
- Uma imagem de perfil atualizada por Melissa Mello cujo **ownerID** na rede social é 4667647. Essa atividade especifica três variáveis de modelo do tipo **publisherVariable**, **listVariable**, e **pictureVariable** (delimitado no **listVariable**). Essa variáveis especificam a pessoa que publicou o item e as informações para a imagem que será atualizada no feed de atividades (usando o **nome**, **valor**, **altText** e os elemento filhos **href** de **pictureVariable**).
    
- Uma imagem de perfil é atualizada por Mateus Vaz cujo **ownerID** na rede social é 5015012. Assim como a última atividade, essa atividade especifica três variáveis de modelo do tipo **publisherVariable**, **listVariable**, e **pictureVariable**. Essa variáveis especificam a pessoa que publicou o item e as informações para a imagem que será atualizada no feed de atividades.
    
- Uma atualização de status Mateus Vaz mostrando o mesmo **ownerID** de 5015012, como na última atividade. Essa atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **textVariable**. **publisherVariable** Especifica a pessoa que publicou o item, feed de atividades e **textVariable** inclui um **valor** da linha de status  `is hiking on Mount Rainier this weekend!`
    
- Uma postagem no blog por Mateus Vaz mostrando o mesmo **ownerID** 5015012 como nas duas últimas atividades. Essa atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **linkVariable**. **publisherVariable** Especifica a pessoa que publicou o item no feed de atividades e **linkVariable** inclui mais informações (especificado, o **nome**, **texto**, e **valor** dos elementos filhos de **linkVariable**) sobre a postagem do blog.
    
Cada uma das quatro atividades especifica um valor **TemplateId do** que corresponde a um dos três modelos especificados no elemento **modelos**. Cada modelo está no seu próprio elemento **activityTemplateContainer** identificado por um  valor **TemplateId** que também é usado para exibir uma atividade com o mesmo valor **TemplateId**. 
  
Para obter uma descrição detalhada dos elementos XML usados no exemplo, confira os tópicos a seguir: 
  
- [Visão geral do XML para um item do feed de atividades](overview-of-xml-for-an-activity-feed-item.md)
    
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variáveis do modelo](template-variables.md)
    
## <a name="xml-example"></a>Exemplos de XML

O exemplo a seguir mostra o XML **feed de atividades** de quatro atividades: duas atualizações de imagem de perfil, uma atualização de status e uma postagem de blog. O XML também especifica três modelos de exibição de atividade para exibir as atividades correspondentes. 
  
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

## <a name="see-also"></a>Confira também

- [Exemplos de XML de provedor OSC](osc-provider-xml-examples.md)  
- [XML para atividades](xml-for-activities.md) 
- [Exemplo de XML de recursos](capabilities-xml-example.md)  
- [Exemplo de XML de amigos](friends-xml-example.md)
- [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

