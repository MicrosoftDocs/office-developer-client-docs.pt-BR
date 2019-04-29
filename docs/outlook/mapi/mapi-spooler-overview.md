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
  
MAPI spooler é uma função do processo do Microsoft Office Outlook responsável por enviar mensagens e receber mensagens de um sistema de mensagens. O spooler MAPI exerce uma função vital no recebimento e na entrega de mensagens. Quando um sistema de mensagens está indisponível, o spooler MAPI armazena as mensagens e as encaminha automaticamente mais tarde. Essa capacidade de manter ou enviar dados quando necessário é conhecido como armazenar e encaminhar, um recurso crítico em ambientes onde as conexões remotas são comuns e o tráfego de rede é alto. O spooler MAPI é executado como um thread de segundo plano no Outlook.
  
O spooler MAPI tem responsabilidades adicionais relacionadas à distribuição de mensagens. Essas tarefas adicionais incluem o seguinte:
  
- Manter o controle dos tipos de destinatários que são tratados por provedores de transporte específicos.
    
- Informando um aplicativo cliente quando uma nova mensagem é entregue.
    
- Invocar o pré-processamento e o processamento de mensagens.
    
- Geração de relatórios que indicam que a entrega de mensagens ocorreu.
    
- Manutenção do status em destinatários processados.
    
A ilustração a seguir mostra em nível alto como uma mensagem flui de um cliente para o sistema de mensagens.
  
**Outgoing message flow**
  
![Fluxo de mensagens de saída] (media/amapi_46.gif "Fluxo de mensagens de saída")
  
O usuário de um aplicativo cliente envia uma mensagem para um ou mais destinatários. O provedor de repositório de mensagens inicia o processo de envio, Formatando a mensagem com informações adicionais necessárias para a transmissão.
  
MAPI spooler recebe a mensagem a ser processada se ocorrer qualquer uma das seguintes condições:
  
- O provedor de repositório de mensagens não está rigidamente acoplado a um provedor de transporte.
    
- A mensagem requer pré-processamento.
    
- O repositório de mensagens e o provedor de transporte estão rigidamente acoplados, mas não podem lidar com todos os destinatários para os quais a mensagem é endereçada.
    
Se o spooler MAPI receber a mensagem, ele realiza qualquer pré-processamento necessário e entrega a mensagem para o provedor de transporte apropriado. O provedor de transporte fornece a mensagem ao seu sistema de mensagens, que a envia para o destinatário pretendido.
  
Com mensagens de entrada, o fluxo é revertido. O provedor de transporte recebe uma mensagem de seu sistema de mensagens e notifica o spooler MAPI. O spooler realiza todos os processamentos e informa o provedor do repositório de mensagens de que uma nova mensagem chegou. Essa notificação faz com que o cliente atualize sua exibição de mensagem, permitindo que o usuário leia a nova mensagem.
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

