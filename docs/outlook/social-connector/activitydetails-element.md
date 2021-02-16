---
title: Elemento activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: O elemento activityDetails armazena os dados brutos para um único item de feed de atividade. Cada item do feed de atividades deve ter seu próprio elemento activityDetails. Os dados no elemento activityDetails são referenciados nos modelos de atividade usando elementos de nome.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434869"
---
# <a name="activitydetails-element"></a>Elemento activityDetails

O **elemento activityDetails** armazena os dados brutos para um único item de feed de atividade. Cada item do feed de atividades deve ter seu próprio **elemento activityDetails.** Os dados no **elemento activityDetails** são referenciados nos modelos de atividade usando elementos **de** nome. Cada dado no elemento **activityDetails** deve ter um **elemento name.** 
  
A tabela a seguir descreve os seis elementos que o **elemento activityDetails** requer. 
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**ownerID** <br/> |A ID do usuário na rede social que gerou esse item de feed de atividades.  <br/> |
|**objectID** <br/> |Uma cadeia de caracteres exclusiva para o item de feed de atividade detectar itens de feed duplicados.  <br/> |
|**applicationId** <br/> |Uma das duas IDs exclusivas que são usadas para corresponder o item de feed de atividades com seu modelo. Se você tiver vários aplicativos ou outros grupos, isso poderá ser usado como um organizador de modelos de primeira camada.  <br/> |
|**templateId** <br/> |A segunda ID exclusiva usada para corresponder o item do feed de atividades com seu modelo. Isso pode ser usado como um organizador de modelos de segunda camada.  <br/> |
|**publishDate** <br/> |A data e a hora em que o item do feed de atividades foi publicado.  <br/> |
|**templateVariables** <br/> |Os dados a serem usados nos tokens para o modelo de item do feed de atividades.  <br/> |
   
Para um exemplo de XML do feed de atividades, consulte [Exemplo XML do feed de atividades](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Confira também

- [Visão geral do XML para um item do feed de atividades](overview-of-xml-for-an-activity-feed-item.md)  
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)  
- [Variáveis do modelo](template-variables.md) 
- [Diretrizes para a exibição adequada das atividades](guidelines-for-properly-displaying-activities.md)  
- [XML para atividades](xml-for-activities.md)  
- [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Como desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

