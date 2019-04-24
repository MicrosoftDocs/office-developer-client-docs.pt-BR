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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350607"
---
# <a name="supporting-message-service-configuration"></a>Suporte à configuração do serviço de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para oferecer suporte à configuração do serviço de mensagens, use o seguinte procedimento:
  
1. Implementar uma função de ponto de entrada que está de acordo com o protótipo [MSGSERVICEENTRY](msgserviceentry.md) . As funções de ponto de entrada de serviço de mensagens gerenciam o acesso a dados de configuração e são chamadas nas seguintes circunstâncias: 
    
   - Quando um cliente faz logon para recuperar informações para configurar o serviço de mensagens.
    
   - Quando um cliente deseja exibir ou alterar uma propriedade de configuração. 
    
   Embora a maioria dos serviços de mensagens forneça funções de ponto de entrada, como deveriam, essas funções não são estritamente necessárias. Os serviços de mensagens podem fornecer acesso a dados de configuração de outras maneiras. No enTanto, o uso de uma função de ponto de entrada padroniza e simplifica o processo de configuração.
    
   O MAPI espera que todas as funções de ponto de entrada do serviço de mensagens possam armazenar e recuperar as propriedades das seções de perfil associadas ao serviço de mensagens. Você pode oferecer suporte a essa funcionalidade interativamente, programaticamente ou de forma interativa e proativa.
    
   Para oferecer suporte à configuração interativa, forneça uma folha de propriedades que exibe as propriedades envolvidas na configuração do serviço de mensagens. Como opção, você também pode fornecer folhas de propriedades para cada provedor configurável. Alguns serviços de mensagens restringem os usuários a um modo de exibição somente leitura das propriedades de configuração; outros serviços de mensagens permitem que os usuários façam alterações.
    
   Para oferecer suporte à configuração programática, a função de ponto de entrada do serviço de mensagens deve ser capaz de funcionar sem a intervenção do usuário. Se o seu serviço de mensagens puder ser chamado pelo assistente de perfil, você deverá oferecer suporte à configuração programática. Se o serviço de mensagens não permitir que ele próprio seja configurado usando o assistente de perfil, você poderá escolher se a configuração programática será ou não compatível.
    
   Para obter mais informações sobre como oferecer suporte à configuração em uma função de ponto de entrada do serviço de mensagens, consulte [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publique o nome da função de ponto de entrada do serviço de mensagens no arquivo de configuração MAPISVC. inf, incluindo a seguinte entrada na seção serviço de mensagens:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Crie uma ou mais caixas de diálogo de folha de propriedades para exibir dados de configuração.
    
4. Execute as seguintes tarefas se quiser permitir que o assistente de perfil configure o serviço de mensagens:
    
   - Implementar uma função de ponto de entrada que está de acordo com o protótipo [WIZARDENTRY](wizardentry.md) . 
    
   - Implemente um procedimento de caixa de diálogo padrão do Windows que esteja em conformidade com o protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
    
   - Aprimore sua função de ponto de entrada do serviço de mensagens para responder a eventos adicionais.
    
## <a name="see-also"></a>Confira também

- [Implementação do serviço de mensagens](message-service-implementation.md)

