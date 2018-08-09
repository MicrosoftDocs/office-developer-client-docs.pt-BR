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
# <a name="template-variables"></a>Variáveis do modelo

Instâncias de variáveis de modelo de (representadas por um elemento **templateVariable** ) especificam os dados de um item de feed em um modelo de atividade de atividade. 
  
Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md).

A tabela a seguir mostra os tipos de variáveis de modelo com suporte, que cada um representado pelo valor de enumeração XML correspondente.
  
|**Tipo de variável do modelo**|**Descrição**|
|:-----|:-----|
|**entityVariable** <br/> |Uma pessoa, grupo ou coisa.  <br/> |
|**linkVariable** <br/> |Um vínculo.  <br/> |
|**listVariable** <br/> |Um grupo de objetos.  <br/> |
|**pictureVariable** <br/> |Uma imagem.  <br/> |
|**publisherVariable** <br/> |O publisher da atividade de alimentação item.  <br/> |
|**textVariable** <br/> |Um bloco de texto.  <br/> |
   
Cada tipo de variável do modelo é obrigatório elementos para especificar os dados sobre essa variável. Variáveis de modelo são especificadas da seguinte maneira:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variável de modelo de lista

Você pode especificar variáveis de modelo que estão contidas dentro de uma lista (delimitada pelos elementos **listVariable** e **listItems** ) da seguinte maneira: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Uma variável de modelo do tipo **listVariable** é um contêiner para objetos. Ele pode conter itens delimitado por vírgula (do tipo **linkVariable** ou **textVariable** ) ou imagens (do tipo **pictureVariable** ). Listas podem conter até cinco vincular itens, cinco itens de texto ou imagens de cinco. 
  
Outlook Social Connector (OSC) localiza o texto ou vincular itens de lista de acordo com a localidade do sistema Windows.
  
Para corretamente, analisar e exibir imagens em uma item de feed de atividade, você deve incluir as imagens em uma lista. Todas as imagens são redimensionadas para ser 52 pixels de altura. A largura da imagem não é redimensionada.
  
## <a name="template-variable-elements"></a>Elementos de variáveis de modelo

Esta seção aborda os elementos obrigatórios e opcionais com suporte para cada tipo de variável do modelo.
  
### <a name="entityvariable"></a>entityVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**id** <br/> |A ID exclusiva do usuário. Obrigatório.  <br/> |
|**nameHint** <br/> |O nome a ser exibido no item de feed. Opcional.  <br/> |
|**profileUrl** <br/> |A URL do perfil da pessoa que será usado como o hiperlink para o nome da pessoa no item feed, se o nome da pessoa estiver presente. Opcional.  <br/> |
|**emailAddress** <br/> |O endereço de email que será usado para atualizar as informações de contato dessa pessoa no Outlook. Opcional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**value** <br/> |A URL para este link. Obrigatório.  <br/> |
|**text** <br/> |O texto do link para exibir, em vez da própria URL. Opcional.  <br/> |
   
### <a name="listvariable"></a>listVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**listItems** <br/> |Um contêiner para itens na lista. Obrigatório.  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**value** <br/> |A URL da imagem. Obrigatório.  <br/> |
|**altText** <br/> |O texto alternativo para exibir a acessibilidade e quando o usuário move o ponteiro do mouse sobre a imagem. Opcional.  <br/> |
|**href** <br/> |O hiperlink a ser usado quando o usuário clica a imagem, se o destino desejado não é a URL da imagem especificada pelo **valor de** elemento. Opcional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**id** <br/> |A ID exclusiva do usuário. Obrigatório.  <br/> |
|**nameHint** <br/> |O nome a ser exibido no item de feed. Opcional.  <br/> |
|**profileUrl** <br/> |A URL do perfil da pessoa que será usado como o hiperlink para o nome da pessoa no item feed, se o nome da pessoa estiver presente. Opcional.  <br/> |
|**emailAddress** <br/> |O endereço de email que será usado para atualizar as informações de contato dessa pessoa no Outlook. Opcional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**value** <br/> |O texto a ser exibido. Opcional.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Visão geral de XML para uma atividade Feed Item](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails elemento](activitydetails-element.md)  
- [activityTemplateContainer elemento](activitytemplatecontainer-element.md)  
- [Diretrizes para exibir adequadamente atividades](guidelines-for-properly-displaying-activities.md)  
- [XML para atividades](xml-for-activities.md)  
- [Esquema XML do Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

