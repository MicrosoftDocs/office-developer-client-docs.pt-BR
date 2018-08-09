---
title: activityTemplateContainer elemento
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Um elemento activityTemplateContainer é um modelo que permite que você formatar itens do seu feed de atividade e reutilizar XML que especifica um layout.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770828"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer elemento

Um elemento **activityTemplateContainer** é um modelo que permite que você formatar itens do seu feed de atividade e reutilizar XML que especifica um layout. Use os IDs (**applicationID** e **templateID**) para corresponder a um item de feed (**activityDetails**) a um modelo (**activityTemplateContainer**). Armazene os dados de layout como parte do elemento **activityTemplate** . Para fazer referência a dados retirados da item de feed de atividade individual, use as variáveis de modelo como espaços reservados para informações como pessoas, links e texto. 
  
A tabela a seguir descreve os três elementos que requer o elemento **activityTemplateContainer** . 
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**applicationID** <br/> |Uma das duas identificações exclusivas que são usadas para corresponder os itens de feed com seu modelo. Se você tiver vários aplicativos ou outros agrupamentos, isso pode ser usado como um organizador de modelo de primeiro nível.  <br/> |
|**templateID** <br/> |A segunda identificação exclusiva que será usada para corresponder os itens de feed com seu modelo. Isso pode ser usado como um organizador de modelo de segundo nível.  <br/> |
|**activityTemplate** <br/> |O layout do modelo de (**ícone**, **título**e **dados** elementos) e o tipo de atividade (**tipo de** elemento).  <br/> |
   
A tabela a seguir descreve os elementos filho de **activityTemplate**, que descrevem o layout e o tipo de um modelo.
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**icon** <br/> |Um token de link, que faz referência a URL para o ícone para esse item de feed.  <br/> |
|**title** <br/> |As informações necessárias para o item de feed.  <br/> |
|**type** <br/> |O tipo de atividade, como uma atualização de status, foto ou documento.  <br/> |
|**data** <br/> |Informações adicionais para o item de feed, como imagens, texto ou links.  <br/> |
   
Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Confira também

- [Visão geral de XML para uma atividade Feed Item](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails elemento](activitydetails-element.md)  
- [Variáveis do modelo](template-variables.md)  
- [Diretrizes para exibir adequadamente atividades](guidelines-for-properly-displaying-activities.md)  
- [XML para atividades](xml-for-activities.md)  
- [Esquema XML do Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

