---
title: Visão geral do XML para um item do feed de atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Um feed de atividades consiste em uma ou mais atividades que ocorrem em uma rede social. Cada feed de atividades é representado por um elemento activityFeed e é caracterizado por essas três informações:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439944"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Visão geral do XML para um item do feed de atividades

Um feed de atividades consiste em uma ou mais atividades que ocorrem em uma rede social. Cada feed de atividades é representado por **um elemento activityFeed** e é caracterizado por essas três informações: 
  
- **rede**— nome da rede social da qual as atividades se originaram.
    
- **atividades**— Contêiner para atividades que ocorrem na conta do usuário conectado nessa rede social.
    
- **modelos contêiner** para modelos que são usados para exibir o item de atividade correspondente em **atividades**.
    
Para criar um item de feed de atividades, você deve estar em conformidade com o esquema XML de extensibilidade do provedor do Outlook Social Connector (OSC). A Figura 1 mostra a estrutura XML do feed de atividades.
  
**Figura 1. Activity feed XML structure**

![Activity XML structure](media/odc_ol14_ta_OSC_Fig06.gif)
  
Para cada item de feed de atividades, as duas partes mais importantes desse esquema são **activityDetails** e **elementos activityTemplateContainer:** 
  
- O **elemento activityDetails** armazena informações específicas para cada item do feed de atividades, como o nome do proprietário da atividade ou a URL das imagens carregadas. 
    
- O **elemento activityTemplateContainer** armazena o formato ou o layout de cada item do feed de atividades. Ele consiste em modelos, representados por elementos **activityTemplate** individuais, que podem ser reutilizáveis para vários itens de feed. 
    
Para um item de feed de atividades individual, o **elemento activityTemplate** especifica as quatro informações a seguir: 
  
- **icon**— Especifica a URL do ícone para exibir o item do feed de atividades.
    
- **title**— Descreve o item de feed de atividades.
    
- **type**— Especifica o tipo de atividade, como um status, uma foto ou uma atualização de documento.
    
- **data**— Especifica informações extras exibidas com o item de feed de atividades.
    
> [!TIP]
> O ícone exibido no feed de atividades é sempre o mesmo que o ícone do provedor retornado pela propriedade **ISocialProvider::SocialNetworkIcon.** 
  
Consulte os tópicos a seguir para obter mais informações sobre o elemento **activityDetails,** o elemento **activityTemplateContainer,** tokens de modelo e variáveis de modelo: 
  
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variáveis do modelo](template-variables.md)
    
- [Diretrizes para a exibição adequada das atividades](guidelines-for-properly-displaying-activities.md)
    
Para um exemplo de XML do feed de atividades, consulte [Exemplo XML do feed de atividades.](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Confira também

- [XML para atividades](xml-for-activities.md) 
- [Esquema XML do provedor Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Como desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

