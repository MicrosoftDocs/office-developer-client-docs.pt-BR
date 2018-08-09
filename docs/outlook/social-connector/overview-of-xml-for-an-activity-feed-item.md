---
title: Visão geral do XML para um item do feed de atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Um feed de atividade consiste em uma ou mais atividades que ocorrem em uma rede social. Cada feed de atividade é representada por um elemento de feed de atividades e é caracterizada por esses três partes de informações:'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770964"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Visão geral do XML para um item do feed de atividades

Um feed de atividade consiste em uma ou mais atividades que ocorrem em uma rede social. Cada feed de atividade é representada por um elemento de **feed de atividades** e é caracterizada por esses três partes de informações: 
  
- **rede**— nome da rede social que origem as atividades.
    
- **atividades**— contêiner para atividades acontecendo na conta do usuário conectado em rede social.
    
- **modelos**— contêiner para modelos que são usados para exibir o item de atividade correspondente em **atividades**.
    
Para criar uma item de feed de atividade, você deve estar em conformidade com o esquema XML de extensibilidade de provedor de Outlook Social Connector (OSC). A Figura 1 mostra o que feed de atividade de estrutura XML.
  
**Figura 1. Estrutura XML do feed de atividade**

![Activity XML structure](media/odc_ol14_ta_OSC_Fig06.gif)
  
Para cada item de feed de atividades, as duas partes mais importantes deste esquema são os elementos **activityDetails** e **activityTemplateContainer** : 
  
- O elemento **activityDetails** armazena informações específicas para cada item, como o nome do proprietário atividade ou a URL para as imagens carregados de feed de atividade. 
    
- O elemento **activityTemplateContainer** armazena o formato ou item de feed de layout para cada atividade. Ele consiste em modelos, representados por individuais **activityTemplate** elementos, que podem ser reutilizados para vários itens de feed. 
    
Para uma item de feed de atividade de individual, o elemento **activityTemplate** Especifica as quatro unidades de informações a seguintes: 
  
- **ícone**— Especifica o URL para o ícone para exibir a atividade feed item.
    
- **título**— descreve a item de feed de atividade.
    
- **tipo**— Especifica o tipo de atividade, como um status, foto ou atualização do documento.
    
- **dados**— Especifica qualquer informação extra exibida com um item de feed de atividade.
    
> [!TIP]
> O ícone exibido na feed de atividade sempre é o mesmo que o ícone do provedor retornado pela propriedade **ISocialProvider::SocialNetworkIcon** . 
  
Consulte os tópicos a seguir para obter mais informações sobre o elemento **activityDetails** , o elemento **activityTemplateContainer** , tokens de modelo e variáveis de modelo: 
  
- [activityDetails elemento](activitydetails-element.md)
    
- [activityTemplateContainer elemento](activitytemplatecontainer-element.md)
    
- [Variáveis do modelo](template-variables.md)
    
- [Diretrizes para exibir adequadamente atividades](guidelines-for-properly-displaying-activities.md)
    
Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Confira também

- [XML para atividades](xml-for-activities.md) 
- [Esquema XML do Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

