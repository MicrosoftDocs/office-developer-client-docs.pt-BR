---
title: Visão geral de spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ec581e2170b92721410106eae00e2d36b3c775a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591335"
---
# <a name="mapi-spooler-overview"></a>Visão geral de spooler MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Spooler MAPI é uma função do processo do Microsoft Office Outlook que é responsável por mensagens de recebimento e envio de mensagens para a partir de um sistema de mensagens. Spooler MAPI tem uma função vital no recebimento da mensagem e entrega. Quando um sistema de mensagens não estiver disponível, MAPI spooler armazena as mensagens e os encaminha automaticamente mais tarde. Essa capacidade de retenção logon em ou enviar dados quando necessário conhecida como armazenar e encaminhar, um recurso fundamental em ambientes onde conexões remotas são comuns e tráfego de rede é alto. Spooler MAPI é executado como um segmento de plano de fundo dentro do Outlook.
  
Spooler MAPI tem responsabilidades adicionais relacionadas à distribuição de mensagem. Essas tarefas adicionais incluem o seguinte:
  
- Manter o controle dos tipos de destinatário são manipulados pelos provedores de transporte específica.
    
- Informando um aplicativo cliente quando uma nova mensagem foi entregue.
    
- Mensagem de invocação pré-processamento e o pós-processamento.
    
- Geração de relatórios que indicam a entrega da mensagem ocorreu.
    
- Mantendo status nos destinatários processados.
    
A ilustração a seguir mostra nitidamente como uma mensagem flui de um cliente para o sistema de mensagens.
  
**Outgoing message flow**
  
![Fluxo de mensagens de saída] (media/amapi_46.gif "Fluxo de mensagens de saída")
  
O usuário de um aplicativo cliente envia uma mensagem para um ou mais destinatários. A mensagem armazenar provedor inicia o processo de envio, formatação da mensagem com informações adicionais necessárias para transmissão.
  
Spooler MAPI recebe a mensagem para processar se qualquer uma das seguintes condições ocorrerem:
  
- O provedor de armazenamento de mensagem não está firmemente combinado com um provedor de transporte.
    
- A mensagem requer pré-processamento.
    
- O armazenamento de mensagens e o transporte provedor estão intimamente ligado, mas eles não podem lidar com todos os destinatários para quem a mensagem é endereçada.
    
Se o spooler MAPI recebe a mensagem, ela realiza qualquer pré-processamento necessário e entrega a mensagem para o provedor de transporte adequado. O provedor de transporte concede a mensagem para seu sistema de mensagens, que envia para o receptor pretendido.
  
Com as mensagens de entrada, o fluxo é invertido. O provedor de transporte recebe uma mensagem de seu sistema de mensagens e notifica o spooler MAPI. Spooler realiza qualquer pós-processamento necessário e informa o provedor de armazenamento de mensagem que uma nova mensagem chegou. Essa notificação faz com que o cliente atualizar sua exibição da mensagem, permitindo ao usuário ler a nova mensagem.
  
## <a name="see-also"></a>Confira também

- [Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

