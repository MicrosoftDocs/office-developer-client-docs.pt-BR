---
title: Elemento activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Um elemento activityTemplateContainer é um modelo que permite formatar seus itens de feed de atividade e reutilizar XML que especifica um layout.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413714"
---
# <a name="activitytemplatecontainer-element"></a>Elemento activityTemplateContainer

Um **elemento activityTemplateContainer** é um modelo que permite formatar seus itens de feed de atividade e reutilizar XML que especifica um layout. Use IDs (**applicationID** e **templateID**) para corresponder um item de feed (**activityDetails**) a um modelo (**activityTemplateContainer**). Armazene os dados de layout como parte do **elemento activityTemplate.** Para fazer referência aos dados que são retirados do item de feed de atividades individuais, use variáveis de modelo como espaço reservado para informações como pessoas, links e texto. 
  
A tabela a seguir descreve os três elementos que o **elemento activityTemplateContainer** requer. 
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**applicationID** <br/> |Uma das duas IDs exclusivas que são usadas para corresponder o item de feed com seu modelo. Se você tiver vários aplicativos ou outros grupos, isso poderá ser usado como um organizador de modelos de primeira camada.  <br/> |
|**templateID** <br/> |A segunda ID exclusiva usada para corresponder o item de feed com seu modelo. Isso pode ser usado como um organizador de modelos de segunda camada.  <br/> |
|**activityTemplate** <br/> |O layout do modelo **(ícone,** **título** e **elementos** de dados) e o tipo de atividade **(elemento de** tipo).  <br/> |
   
A tabela a seguir descreve os elementos filho de **activityTemplate**, que descrevem o layout e o tipo de um modelo.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**icon** <br/> |Um token de link, que faz referência à URL do ícone para esse item de feed.  <br/> |
|**title** <br/> |As informações necessárias para o item de feed.  <br/> |
|**tipo** <br/> |O tipo de atividade, como uma atualização de status, foto ou documento.  <br/> |
|**data** <br/> |Qualquer informação adicional para o item de feed, como imagens, texto ou links.  <br/> |
   
Para um exemplo de XML do feed de atividades, consulte [Exemplo XML do feed de atividades](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Confira também

- [Visão geral do XML para um item do feed de atividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityDetails](activitydetails-element.md)  
- [Variáveis do modelo](template-variables.md)  
- [Diretrizes para a exibição adequada das atividades](guidelines-for-properly-displaying-activities.md)  
- [XML para atividades](xml-for-activities.md)  
- [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Como desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

