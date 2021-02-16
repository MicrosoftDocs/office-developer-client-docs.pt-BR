---
title: Visão geral do spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432713"
---
# <a name="mapi-spooler-overview"></a>Visão geral do spooler MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O spooler MAPI é uma função do processo do Microsoft Office Outlook responsável por enviar e receber mensagens de um sistema de mensagens. O spooler MAPI desempenha um papel vital no recebimento e na entrega de mensagens. Quando um sistema de mensagens não está disponível, o spooler MAPI armazena as mensagens e as encaminha automaticamente posteriormente. Essa capacidade de manter ou enviar dados quando necessário é conhecida como armazenamento e encaminhamento, um recurso crítico em ambientes onde as conexões remotas são comuns e o tráfego de rede é alto. O spooler MAPI é executado como um thread em segundo plano no Outlook.
  
O spooler MAPI tem responsabilidades adicionais relacionadas à distribuição de mensagens. Essas tarefas extras incluem o seguinte:
  
- Acompanhar os tipos de destinatários manipulados por provedores de transporte específicos.
    
- Informar um aplicativo cliente quando uma nova mensagem for entregue.
    
- Invocando o pré-processamento e o pós-processamento de mensagens.
    
- Gerar relatórios que indicam que a entrega da mensagem ocorreu.
    
- Mantendo o status de destinatários processados.
    
A ilustração a seguir mostra em um alto nível como uma mensagem flui de um cliente para o sistema de mensagens.
  
**Outgoing message flow**
  
![Fluxo de mensagens de saída Fluxo]de mensagens de(media/amapi_46.gif "saída")
  
O usuário de um aplicativo cliente envia uma mensagem para um ou mais destinatários. O provedor de armazenamento de mensagens inicia o processo de envio, formatando a mensagem com informações adicionais necessárias para transmissão.
  
O spooler MAPI recebe a mensagem a ser processada se qualquer uma das seguintes condições ocorrer:
  
- O provedor de armazenamento de mensagens não está fortemente unido a um provedor de transporte.
    
- A mensagem requer pré-processamento.
    
- O armazenamento de mensagens e o provedor de transporte estão fortemente próximos, mas não podem lidar com todos os destinatários aos quais a mensagem é endereçada.
    
Se o spooler MAPI receber a mensagem, ele executará qualquer pré-processamento necessário e entregará a mensagem ao provedor de transporte apropriado. O provedor de transporte fornece a mensagem ao seu sistema de mensagens, que a envia ao destinatário pretendido.
  
Com as mensagens de entrada, o fluxo é revertido. O provedor de transporte recebe uma mensagem de seu sistema de mensagens e notifica o spooler MAPI. O Spooler executa qualquer pós-processamento necessário e informa ao provedor do armazenamento de mensagens que uma nova mensagem chegou. Essa notificação faz com que o cliente atualize a exibição da mensagem, permitindo que o usuário leia a nova mensagem.
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

