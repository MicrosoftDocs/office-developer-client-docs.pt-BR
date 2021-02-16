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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412083"
---
# <a name="mapi-message-classes"></a>Classes de mensagens MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada mensagem tem uma propriedade de classe de **mensagem, PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), que identifica o tipo, a finalidade ou o conteúdo da mensagem. **PR_MESSAGE_CLASS** é uma propriedade necessária em todas as novas mensagens. A classe de uma mensagem determina o formulário usado para apresentar a mensagem ao usuário e a pasta para colocar mensagens de entrada. 
  
Classes de mensagem são cadeias de caracteres com diferenciação de minúsculas que contêm caracteres ASCII de 32 a 127 e são delimitadas por pontos, mas não podem terminar com um ponto. Cada cadeia de caracteres representa um nível de subclasse e não há limite para o número de níveis permitidos. 
  
Por exemplo, a maioria das mensagens que os aplicativos cliente enviam e recebem se enquadram na classe de mensagens **do IPM,** uma categoria ampla que descreve todas as mensagens interpersonales (ou seja, mensagens que devem ser lidas por um usuário humano, em vez de programaticamente por um computador). Os provedores de armazenamento de mensagens descrevem com mais precisão uma mensagem IPM criando uma **subclasse do IPM.** A **subclasse** do IPM herda as propriedades da **classe de mensagens do IPM.** As subclasses da **classe IPM** são nomeadas concatenando outras cadeias de caracteres no identificador IPM, como **IPM. Observação** para descrever uma mensagem de anotação e **um IPM. Contato** para descrever uma mensagem de contato. 
  
Para lidar com a exibição e o gerenciamento de mensagens IPM, os clientes podem usar um formulário padrão que o MAPI fornece. Para lidar com a exibição e o gerenciamento de novas classes de mensagens, você como desenvolvedor de aplicativo cliente tem duas opções:
  
1. Você pode criar um novo formulário usando o conjunto de interfaces de formulário definidas por MAPI que um cliente padrão pode usar.
    
2. Você pode escrever seu próprio cliente implementando um aplicativo autônomo completo. 
    
Embora os clientes deverão definir a propriedade **PR_MESSAGE_CLASS** para cada mensagem de saída como uma subclasse de **IPM** ou **IPC**, o provedor de armazenamento de mensagens tem a responsabilidade final por defini-la. Portanto, se um cliente enviar uma mensagem sem definir sua classe de mensagem, o provedor de armazenamento de mensagens a definirá como o valor padrão apropriado para o tipo apropriado de cliente. A classe de mensagem padrão para clientes de mensagens interpersonal é **IPM**; a classe de mensagem padrão para clientes de comunicação entre processos é **IPC**. 
  
As classes de mensagem têm uma restrição de comprimento de 255 caracteres. No entanto, as classes de mensagem não devem exceder 127 caracteres para dar suporte às classes de mensagem usadas em relatórios. As classes de mensagem de relatório são baseadas na classe da mensagem original, com duas adições: um prefixo e um sufixo. O prefixo REPORT indica que a mensagem é um relatório, e o sufixo indica o tipo de relatório: DR (relatório de entrega), NDR (relatório de não entrega), IPNRN (relatório de leitura) ou IPNNRN (relatório não lido). Observe que essas restrições de comprimento são fornecidas em caracteres; em plataformas que usam um conjunto de caracteres de dois byte, a contagem de byte real pode ser maior. 
  
Provedores de armazenamento de mensagens devem retornar MAPI_E_INVALID_PARAMETER de suas implementações de método [IMAPIProp::SetProps](imapiprop-setprops.md) quando um cliente tenta atribuir uma cadeia de caracteres que excede o limite permitido para sua classe de mensagem. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

