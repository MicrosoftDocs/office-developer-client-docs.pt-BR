---
title: Classes de mensagens MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b2ab5d56c53216152a83ca207ff5ba1d53c9049d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345889"
---
# <a name="mapi-message-classes"></a>Classes de mensagens MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada mensagem tem uma propriedade de classe Message, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), que identifica o tipo, finalidade ou conteúdo da mensagem. **PR_MESSAGE_CLASS** é uma propriedade obrigatória em todas as novas mensagens. Uma classe de mensagem determina o formulário que é usado para apresentar a mensagem ao usuário e a pasta para colocar mensagens de entrada. 
  
As classes de mensagem são cadeias de caracteres com distinção entre maiúsculas e minúsculas que contêm caracteres ASCII 32 a 127 e delimitadas por pontos, mas não podem terminar com um ponto. Cada cadeia de caracteres representa um nível de subclassificação, e não há limite para o número de níveis permitido. 
  
Por exemplo, a maioria das mensagens que os aplicativos clientes enviam e recebem o outono na classe de mensagem **IPM** , uma categoria ampla que descreve todas as mensagens interpessoais (ou seja, as mensagens que devem ser lidas por um usuário humano, em vez de programaticamente por um computador). Os provedores de repositórios de mensagens descrevem mais precisamente uma mensagem IPM criando uma subclasse **IPM** . A subclasse **IPM** herda as propriedades da classe de mensagem **IPM** . As subclasses da classe **IPM** são nomeadas por meio da concatenação de outras cadeias de caracteres no identificador IPM, como **IPM. Observação** para descrever uma mensagem de aviso e **IPM. Contato** para descrever uma mensagem de contato. 
  
Para lidar com a exibição e o gerenciamento de mensagens IPM, os clientes podem usar um formulário padrão que o MAPI fornece. Para lidar com a exibição e o gerenciamento de novas classes de mensagens, você como desenvolvedor de aplicativo cliente tem duas opções:
  
1. Você pode criar um novo formulário usando o conjunto de interfaces de formulários definidas por MAPI que um cliente padrão pode usar.
    
2. Você pode escrever seu próprio cliente implementando um aplicativo completo e autônomo. 
    
Embora os clientes devam definir a propriedade **PR_MESSAGE_CLASS** para cada mensagem de saída para uma subclasse de **IPM** ou **IPC**, o provedor de repositório de mensagens tem a responsabilidade final de defini-la. Portanto, se um cliente enviar uma mensagem sem definir sua classe de mensagem, o provedor do repositório de mensagens a definirá como o valor padrão apropriado para o tipo apropriado de cliente. A classe de mensagem padrão para clientes de mensagens interpessoais é **IPM**; a classe de mensagem padrão para clientes de comunicação entre processos é **IPC**. 
  
As classes de mensagens têm uma restrição de tamanho de 255 caracteres. No enTanto, as classes de mensagem não devem exceder 127 caracteres para suportar as classes de mensagens usadas nos relatórios. As classes de mensagens de relatório são baseadas na classe da mensagem original, com duas adições: um prefixo e um sufixo. O prefixo REPORT indica que a mensagem é um relatório e o sufixo indica o tipo de relatório: DR (relatório de entrega), NDR (notificação de não entrega), IPNRN (ler relatório) ou IPNNRN (relatório não lido). Observe que essas restrições de tamanho são dadas em caracteres; em plataformas que usam um conjunto de caracteres de byte duplo, a contagem de bytes real pode ser maior. 
  
Os provedores de repositórios de mensagens devem retornar MAPI_E_INVALID_PARAMETER de suas implementações de método [IMAPIProp::](imapiprop-setprops.md) SetProps quando um cliente tenta atribuir uma cadeia de caracteres que excede o limite permitido para sua classe de mensagem. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

