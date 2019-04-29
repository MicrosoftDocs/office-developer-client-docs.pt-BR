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
# <a name="template-variables"></a>Variáveis do modelo

Instâncias de variáveis de modelo (representadas por um elemento **templateVariable** ) especificam os dados de um item de feed de atividade em um modelo de atividade. 
  
Para obter um exemplo de XML de feed de atividades, consulte [exemplo de XML de feed de atividades](activity-feed-xml-example.md).

A tabela a seguir mostra os tipos de variáveis de modelo suportadas, cada uma representada pelo valor de enumeração XML correspondente.
  
|**Tipo de variável de modelo**|**Descrição**|
|:-----|:-----|
|**entityVariable** <br/> |Uma pessoa, grupo ou item.  <br/> |
|**linkVariable** <br/> |Um link.  <br/> |
|**listVariable** <br/> |Um grupo de objetos.  <br/> |
|**pictureVariable** <br/> |Uma imagem.  <br/> |
|**publisherVariable** <br/> |O fornecedor do item de feed de atividade.  <br/> |
|**textVariable** <br/> |Um bloco de texto.  <br/> |
   
Cada tipo de variável de modelo tem elementos obrigatórios para especificar os dados da variável. As variáveis de modelo são especificadas da seguinte maneira:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variável de modelo de lista

Você pode especificar variáveis de modelo que estão contidas em uma lista (delimitada pelos elementos **listVariable** e **ListItems** ) da seguinte maneira: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Uma variável de modelo do tipo **listVariable** é um contêiner para objetos. Ele pode conter itens delimitados por vírgulas (do tipo **linkVariable** ou textVariable) ou imagens (do tipo **pictureVariable** ). **** As listas podem conter até cinco itens de link, cinco itens de texto ou cinco imagens. 
  
O Outlook Social Connector (OSC) localiza itens de link ou de lista de texto de acordo com a localidade de sistema do Windows.
  
Para analisar e exibir corretamente as imagens em um item de feed de atividades, você deve incluir imagens em uma lista. Todas as imagens são redimensionadas para serem 52 pixels de altura. A largura da imagem não é redimensionada.
  
## <a name="template-variable-elements"></a>Elementos de variável de modelo

Esta seção aborda os elementos obrigatórios e opcionais com suporte para cada tipo de variável de modelo.
  
### <a name="entityvariable"></a>entityVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**id** <br/> |A identificação exclusiva do usuário. Obrigatório.  <br/> |
|**nameHint** <br/> |O nome a ser exibido no item de feed. Opcional.  <br/> |
|**profileUrl** <br/> |A URL do perfil da pessoa que será usada como o hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente. Opcional.  <br/> |
|**emailAddress** <br/> |O endereço de email usado para atualizar as informações de contato desta pessoa no Outlook. Opcional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**value** <br/> |A URL para este link. Obrigatório.  <br/> |
|**text** <br/> |O texto do link a ser exibido em vez da própria URL. Opcional.  <br/> |
   
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
|**altText** <br/> |O texto alternativo a ser exibido para acessibilidade e quando o usuário move o ponteiro do mouse sobre a imagem. Opcional.  <br/> |
|**href** <br/> |O hiperlink a ser usado quando o usuário clica na imagem, se o destino desejado não for a URL da imagem especificada pelo elemento **Value** . Opcional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**id** <br/> |A identificação exclusiva do usuário. Obrigatório.  <br/> |
|**nameHint** <br/> |O nome a ser exibido no item de feed. Opcional.  <br/> |
|**profileUrl** <br/> |A URL do perfil da pessoa que será usada como o hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente. Opcional.  <br/> |
|**emailAddress** <br/> |O endereço de email usado para atualizar as informações de contato desta pessoa no Outlook. Opcional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**value** <br/> |O texto a ser exibido. Opcional.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Visão geral do XML para um item do feed de atividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Diretrizes para exibir atividades de modo adequado](guidelines-for-properly-displaying-activities.md)  
- [XML para atividades](xml-for-activities.md)  
- [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Desenvolvimento de um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

