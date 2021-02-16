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

Instâncias de variáveis de modelo (representadas por um **elemento templateVariable)** especificam os dados de um item de feed de atividade em um modelo de atividade. 
  
Para um exemplo de XML do feed de atividades, consulte [Exemplo XML do feed de atividades.](activity-feed-xml-example.md)

A tabela a seguir mostra os tipos de variáveis de modelo com suporte, cada uma representada pelo valor de enumeração XML correspondente.
  
|**Tipo de variável de modelo**|**Descrição**|
|:-----|:-----|
|**entityVariable** <br/> |Uma pessoa, grupo ou coisa.  <br/> |
|**linkVariable** <br/> |Um link.  <br/> |
|**listVariable** <br/> |Um grupo de objetos.  <br/> |
|**pictureVariable** <br/> |Uma imagem.  <br/> |
|**publisherVariable** <br/> |O editor do item de feed de atividades.  <br/> |
|**textVariable** <br/> |Um bloco de texto.  <br/> |
   
Cada tipo de variável de modelo exigiu elementos para especificar os dados sobre essa variável. As variáveis de modelo são especificadas da seguinte forma:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variável de modelo de lista

Você pode especificar variáveis de modelo que estão contidas em uma lista (delimitada pelos elementos **listVariable** e **listItems)** da seguinte forma: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Uma variável de modelo do **tipo listVariable** é um contêiner para objetos. Ele pode conter itens delimitados por vírgula (do tipo **linkVariable** ou **textVariable)** ou imagens (do tipo **pictureVariable).** As listas podem conter até cinco itens de link, cinco itens de texto ou cinco imagens. 
  
O Outlook Social Connector (OSC) localiza os itens de lista de texto ou link de acordo com a localidade do sistema Windows.
  
Para analisar e exibir imagens corretamente em um item do feed de atividades, você deve incluir imagens em uma lista. Todas as imagens são reorganizadas para ter 52 pixels de altura. A largura da imagem não é re tamanhoada.
  
## <a name="template-variable-elements"></a>Modelos de elementos variáveis

Esta seção aborda os elementos obrigatórios e opcionais com suporte para cada tipo de variável de modelo.
  
### <a name="entityvariable"></a>entityVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**id** <br/> |A ID exclusiva do usuário. Obrigatório.  <br/> |
|**nameHint** <br/> |O nome a ser exibido no item de feed. Opcional.  <br/> |
|**profileUrl** <br/> |A URL do perfil da pessoa que será usada como hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente. Opcional.  <br/> |
|**emailAddress** <br/> |O endereço de email usado para atualizar as informações de contato dessa pessoa no Outlook. Opcional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**value** <br/> |A URL para este link. Obrigatório.  <br/> |
|**text** <br/> |O texto do link a ser exibido em vez da PRÓPRIA URL. Opcional.  <br/> |
   
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
|**href** <br/> |O hiperlink a ser usado quando o usuário clica na imagem, se o destino desejado não for a URL da imagem especificada pelo **elemento de** valor. Opcional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**id** <br/> |A ID exclusiva do usuário. Obrigatório.  <br/> |
|**nameHint** <br/> |O nome a ser exibido no item de feed. Opcional.  <br/> |
|**profileUrl** <br/> |A URL do perfil da pessoa que será usada como hiperlink para o nome da pessoa no item de feed, se o nome da pessoa estiver presente. Opcional.  <br/> |
|**emailAddress** <br/> |O endereço de email usado para atualizar as informações de contato dessa pessoa no Outlook. Opcional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Elemento**|**Descrição**|
|:-----|:-----|
|**name** <br/> |O nome da variável. Obrigatório.  <br/> |
|**value** <br/> |O texto a ser exibido. Opcional.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Visão geral do XML para um item do feed de atividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Diretrizes para a exibição adequada das atividades](guidelines-for-properly-displaying-activities.md)  
- [XML para atividades](xml-for-activities.md)  
- [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Como desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

