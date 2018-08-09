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
# <a name="activity-feed-xml-example"></a>Exemplo de XML de Feed de atividade

O exemplo de XML deste tópico é uma cadeia de caracteres XML retornada para o Outlook Social Connector (OSC) depois de chamar o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para uma rede social de feed de atividade. 
  
O exemplo mostra o **feed de atividades** XML que contém as seguintes atividades de quatro, cada delimitados por elemento **activityDetails** e correspondência de um modelo para fins de exibição: 
  
- Atualizar uma imagem de perfil Melissa Macbeth, cujo **ownerID** na rede social é 4667647. Esta atividade especifica três variáveis do modelo de tipo **publisherVariable**, **listVariable**e **pictureVariable** (que está contido em **listVariable**). Especificam a pessoa que publicado a informações de imagem para serem atualizadas (usando os elementos de filho **href** , **valor**, **altText**e **nome**de **pictureVariable**) e item de feed de atividade.
    
- Atualizar uma imagem de perfil Michael Affronti cujo **ownerID** na rede social é 5015012. Semelhante à última atividade, essa atividade especifica três variáveis do modelo de tipo **publisherVariable**, **listVariable**e **pictureVariable**. Especificam a pessoa que publicado a informações da imagem a ser atualizado e o item de feed de atividade.
    
- Uma atualização de status por Michael Affronti, mostrando o mesmo **ownerID** de 5015012 como a última atividade. Esta atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **textVariable**. **publisherVariable** Especifica a pessoa que publicado a item de feed de atividade e **textVariable** inclui um **valor** de linha de status`is hiking on Mount Rainier this weekend!`
    
- Uma postagem de blog por Michael Affronti, mostrando o mesmo **ownerID** de 5015012 como as duas últimas atividades. Esta atividade especifica duas variáveis de modelo do tipo **publisherVariable** e **linkVariable**. **publisherVariable** Especifica a pessoa que publicou a atividade de item de feed e **linkVariable** inclui ainda mais informações (especificadas pelos elementos filho de **nome**, o **texto**e o **valor** de **linkVariable**) sobre a postagem do blog.
    
Cada uma das quatro atividades Especifica um valor de **templateID** , que corresponde a um dos três modelos especificados pelo elemento **modelos** . Cada modelo está em seu próprio elemento **activityTemplateContainer** , identificado por um valor **templateID** que também é usado para exibir uma atividade que tem o mesmo valor de **templateID** . 
  
Para obter uma descrição detalhada dos elementos XML usados no exemplo, consulte os tópicos a seguir: 
  
- [Visão geral de XML para uma atividade Feed Item](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails elemento](activitydetails-element.md)
    
- [activityTemplateContainer elemento](activitytemplatecontainer-element.md)
    
- [Variáveis do modelo](template-variables.md)
    
## <a name="xml-example"></a>Exemplo XML

O exemplo a seguir mostra o **feed de atividades** XML de quatro atividades: dois perfis atualizações de imagem, uma atualização de status e uma postagem de blog. O XML também especifica os três modelos de exibição de atividades para exibir as atividades correspondentes. 
  
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

## <a name="see-also"></a>Confira também

- [Exemplos XML de provedor do OSC](osc-provider-xml-examples.md)  
- [XML para atividades](xml-for-activities.md) 
- [Exemplo de XML de recursos](capabilities-xml-example.md)  
- [Exemplo de XML de amigos](friends-xml-example.md)
- [Esquema XML do Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md)

