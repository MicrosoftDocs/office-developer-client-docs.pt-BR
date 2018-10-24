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
ms.openlocfilehash: 6f9ac5d9cef09ce6d4f3006ecc804db6291cae77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579337"
---
# <a name="supporting-message-service-configuration"></a>Suporte à configuração do serviço de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para suportar a configuração do serviço de mensagens, use o procedimento a seguir:
  
1. Implemente uma função de ponto de entrada que está em conformidade com o protótipo [MSGSERVICEENTRY](msgserviceentry.md) . Funções de ponto de entrada de serviço de mensagem gerenciam o acesso aos dados de configuração e são chamadas nas seguintes circunstâncias: 
    
   - Quando um cliente fizer logon em recuperar informações para configurar seu serviço de mensagem.
    
   - Quando um cliente deseja exibir ou alterar uma propriedade de configuração. 
    
   Embora a maioria dos serviços de mensagem fornecerá funções de ponto de entrada, como deveriam, essas funções não são estritamente necessárias. Serviços de mensagens podem fornecer acesso aos dados de configuração de outras formas. No entanto, usando uma função de ponto de entrada padroniza e simplifica o processo de configuração.
    
   MAPI espera que todas as mensagens serviço entrada ponto funções para ser capaz de armazenar e recuperar as propriedades de seções perfil associados ao seu serviço de mensagem. Você pode oferecer suporte a essa funcionalidade interativamente, programaticamente, ou ambos interativamente e programaticamente.
    
   Para oferecer suporte à configuração interativa, fornecer uma folha de propriedades que exibe as propriedades envolvidas na configuração do seu serviço de mensagem. Como opção, também é possível oferecer folhas de propriedades para cada provedor configurável. Alguns serviços de mensagem restringem os usuários a um modo de exibição somente leitura das propriedades de configuração; outros serviços de mensagem permitem que os usuários façam alterações.
    
   Para oferecer suporte à configuração de programação, sua função de ponto de entrada de serviço de mensagem deve ser capaz de trabalhar sem intervenção do usuário. Se o seu serviço de mensagem pode ser chamado pelo Assistente de perfil, você deve suportar configuração programática. Se o seu serviço de mensagem não permitir que a própria a ser configurado usando o Assistente de perfil, você poderá escolher se deseja ou não oferecer suporte a configurações de programação.
    
   Para obter mais informações sobre como suportar a configuração em uma entrada de serviço de mensagem ponto função, consulte [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Publica o nome da sua função de ponto de entrada de serviço de mensagem no arquivo de configuração Mapisvc, incluindo a seguinte entrada na seção serviço de mensagem:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Crie um ou mais propriedade folha caixas de diálogo para exibir os dados de configuração.
    
4. Se você quiser permitir que o Assistente de perfil configurar seu serviço de mensagem, execute as seguintes tarefas:
    
   - Implemente uma função de ponto de entrada que está em conformidade com o protótipo [WIZARDENTRY](wizardentry.md) . 
    
   - Implemente um procedimento de caixa de diálogo Windows padrão que está em conformidade com o protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
    
   - Melhore sua função do ponto de entrada do serviço de mensagem para responder a eventos adicionais.
    
## <a name="see-also"></a>Confira também

- [Implementação do serviço de mensagem](message-service-implementation.md)

