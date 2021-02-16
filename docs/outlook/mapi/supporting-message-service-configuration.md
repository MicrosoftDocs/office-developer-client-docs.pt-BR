---
title: Suporte à configuração do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418992"
---
# <a name="supporting-message-service-configuration"></a>Suporte à configuração do serviço de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para dar suporte à configuração do serviço de mensagens, use o seguinte procedimento:
  
1. Implemente uma função de ponto de entrada que esteja em conformidade com o [protótipo MSGSERVICEENTRY.](msgserviceentry.md) As funções de ponto de entrada do serviço de mensagens gerenciam o acesso aos dados de configuração e são chamadas nas seguintes circunstâncias: 
    
   - Quando um cliente faz o login para recuperar informações para configurar o serviço de mensagens.
    
   - Quando um cliente deseja exibir ou alterar uma propriedade de configuração. 
    
   Embora a maioria dos serviços de mensagens forneça funções de ponto de entrada, como deveriam, essas funções não são estritamente necessárias. Os serviços de mensagens podem fornecer acesso aos dados de configuração de outras maneiras. No entanto, o uso de uma função de ponto de entrada padroniza e simplifica o processo de configuração.
    
   MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service. Você pode dar suporte a essa funcionalidade de forma interativa, programática ou interativa e programática.
    
   Para dar suporte à configuração interativa, forneça uma folha de propriedades que exibe as propriedades envolvidas na configuração do serviço de mensagens. Como opção, você também pode fornecer folhas de propriedades para cada provedor configurável. Alguns serviços de mensagens restringem os usuários a uma exibição somente leitura das propriedades de configuração; outros serviços de mensagens permitem que os usuários façam alterações.
    
   Para dar suporte à configuração programática, sua função de ponto de entrada do serviço de mensagens deve ser capaz de funcionar sem intervenção do usuário. Se o serviço de mensagens puder ser chamado pelo Assistente de Perfil, você deverá dar suporte à configuração programática. Se o serviço de mensagens não se permitir ser configurado usando o Assistente de Perfil, você poderá optar por dar suporte ou não à configuração programática.
    
   Para obter mais informações sobre como dar suporte à configuração em uma função de ponto de entrada do serviço de mensagens, consulte [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publique o nome da função de ponto de entrada do serviço de mensagens no arquivo de configuração Mapisvc.inf incluindo a seguinte entrada na seção do serviço de mensagens:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Crie uma ou mais caixas de diálogo de folha de propriedades para exibir dados de configuração.
    
4. Execute as seguintes tarefas se quiser permitir que o Assistente de Perfil configure seu serviço de mensagem:
    
   - Implemente uma função de ponto de entrada que esteja em conformidade com o [protótipo WIZARDENTRY.](wizardentry.md) 
    
   - Implemente um procedimento de caixa de diálogo padrão do Windows que esteja em conformidade com o [protótipo SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md) 
    
   - Aprimora a função de ponto de entrada do serviço de mensagens para responder a eventos adicionais.
    
## <a name="see-also"></a>Confira também

- [Implementação do serviço de mensagens](message-service-implementation.md)

