---
title: activityDetails elemento
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: O elemento activityDetails armazena os dados brutos para um item de feed de atividade único. Cada item de feed de atividade deve ter seu próprio elemento activityDetails. Dados no elemento activityDetails referenciados nos modelos de atividade usando nomes de elementos.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770825"
---
# <a name="activitydetails-element"></a>activityDetails elemento

O elemento **activityDetails** armazena os dados brutos para um item de feed de atividade único. Cada item de feed de atividade deve ter seu próprio elemento **activityDetails** . Dados no elemento **activityDetails** referenciados nos modelos de atividade usando **nomes** de elementos. Cada parte dos dados no elemento **activityDetails** deve ter um elemento **name** . 
  
A tabela a seguir descreve os elementos de seis que requer o elemento **activityDetails** . 
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**ownerID** <br/> |A ID do usuário na rede social que gerou essa atividade feed item.  <br/> |
|**objectID** <br/> |Uma cadeia de caracteres exclusiva da atividade de alimentação item para detectar itens de feed de duplicata.  <br/> |
|**ApplicationId** <br/> |Uma das duas identificações exclusivas que são usadas para corresponder a atividade feed item com seu modelo. Se você tiver vários aplicativos ou outros agrupamentos, isso pode ser usado como um organizador de modelo de primeiro nível.  <br/> |
|**templateId** <br/> |A segunda identificação exclusiva que será usada para corresponder a atividade feed item com seu modelo. Isso pode ser usado como um organizador de modelo de segundo nível.  <br/> |
|**publishDate** <br/> |A data e hora em que o item de feed de atividade foi publicado.  <br/> |
|**templateVariables** <br/> |Os dados a serem usados em tokens para o modelo de itens de feed de atividade.  <br/> |
   
Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Confira também

- [Visão geral de XML para uma atividade Feed Item](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer elemento](activitytemplatecontainer-element.md)  
- [Variáveis do modelo](template-variables.md) 
- [Diretrizes para exibir adequadamente atividades](guidelines-for-properly-displaying-activities.md)  
- [XML para atividades](xml-for-activities.md)  
- [Esquema XML do Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

