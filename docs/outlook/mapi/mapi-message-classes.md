---
title: Classes de mensagem MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eecbbb3b806ecaee6c7ceba5c92bd4b713ad1075
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575137"
---
# <a name="mapi-message-classes"></a>Classes de mensagem MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada mensagem tem uma propriedade de classe de mensagem, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), que identifica o tipo, finalidade ou o conteúdo da mensagem. **PR_MESSAGE_CLASS** é uma propriedade necessária em todas as novas mensagens. Classe da mensagem determina o formulário que é usado para apresentar a mensagem ao usuário e a pasta para a colocação de mensagens de entrada. 
  
As classes de mensagem são cadeias de caracteres de maiusculas e minúsculas que contêm caracteres ASCII 32 a 127 e são delimitadas por períodos, mas eles não podem terminar com um ponto. Cada cadeia de caracteres representa um nível de subclassificação e não há nenhum limite no número de níveis permitidos. 
  
Por exemplo, a maioria das mensagens que os aplicativos cliente envia e recebem o são classificados em que a mensagem **IPM** class, uma categoria ampla que descreve todos os emails interpessoais emails (ou seja, as mensagens devem ser lidas por um usuário humano, em vez de forma programática por um computador). Provedores de armazenamento de mensagem mais precisamente descrevem uma mensagem IPM criando uma subclasse **IPM** . A subclasse **IPM** herda as propriedades da classe de mensagem **IPM** . Subclasses da classe **IPM** são nomeadas concatenando outras cadeias de caracteres do caractere o identificador IPM, como **IPM. Observação** para descrever uma mensagem de observação e **IPM. Entre em contato com** para descrever uma mensagem de contato. 
  
Para lidar com a exibição e o gerenciamento das mensagens IPM, os clientes podem usar um formulário padrão que fornece de MAPI. Para lidar com a exibição e o gerenciamento das novas classes de mensagem, você como um desenvolvedor de aplicativos cliente tem duas opções:
  
1. Você pode criar um novo formulário usando o conjunto de interfaces de formulário definidos pelo MAPI que um cliente padrão pode usar.
    
2. Você pode escrever seu próprio cliente por meio da implementação completa e aplicativo autônomo. 
    
Embora clientes devem definir a propriedade **PR_MESSAGE_CLASS** para todas as mensagens de saída para uma subclasse do **IPM** ou **CPI**, o provedor de armazenamento de mensagem tem a responsabilidade ultimate para defini-la. Portanto, se um cliente envia uma mensagem sem a definição de classe da mensagem, o provedor de armazenamento de mensagem define-lo como o valor padrão apropriado para o tipo apropriado de cliente. A classe de mensagem padrão para clientes de mensagens interpessoais é **IPM**; a classe de mensagem padrão para clientes de comunicação entre processos é **CPI**. 
  
Classes de mensagens tem uma restrição de comprimento de 255 caracteres. No entanto, as classes de mensagens não devem exceder 127 caracteres para suportar as classes de mensagem usadas em relatórios. Classes de mensagens de relatório baseiam-se na classe da mensagem original, com duas adições: um prefixo e um sufixo. O prefixo relatório indica que a mensagem é um relatório e o sufixo indica o tipo de relatório: recuperação de desastres (relatório de entrega), NDR (relatório de não entrega), IPNRN (leitura relatório) ou IPNNRN (relatório nonread). Observe que essas restrições de tamanho são fornecidas em caracteres; em plataformas que usam um conjunto de caracteres de byte duplo, a contagem de bytes real pode ser maior. 
  
Provedores de armazenamento de mensagem devem retornar MAPI_E_INVALID_PARAMETER de suas implementações de método [IMAPIProp::SetProps](imapiprop-setprops.md) quando um cliente tenta atribuir uma cadeia de caracteres que excede o limite permitido para seu classe de mensagem. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

