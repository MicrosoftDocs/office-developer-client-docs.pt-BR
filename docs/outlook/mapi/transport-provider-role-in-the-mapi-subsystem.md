---
title: Função do provedor de transporte no subsistema MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7cadb57706e3feec7ed98dd5e4e8d75967036fef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424053"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Função do provedor de transporte no subsistema MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As bibliotecas de vínculo dinâmico (DLLs) do provedor de transporte fornecem a interface entre o spooler do MAPI e a parte de um sistema de mensagens responsável pelo envio e recebimento de mensagens. O spooler MAPI e o provedor de transporte trabalham juntos para lidar com as responsabilidades de envio de uma mensagem ou de recebimento de uma mensagem. O spooler MAPI carrega a DLL do provedor de transporte quando é usado pela primeira vez e a libera quando não é mais necessário. Vários provedores de transporte podem ser instalados no mesmo sistema, mas o MAPI fornece o único spooler necessário.
  
Os aplicativos clientes normalmente não se comunicam diretamente com o provedor de transporte. Em vez disso, os clientes enviam mensagens por meio de um provedor de armazenamento e o spooler MAPI envia mensagens de saída para o provedor de transporte apropriado e entrega mensagens de entrada para o repositório de mensagens apropriado. O MAPI spooler funciona e faz suas chamadas para provedores de transporte quando os aplicativos de primeiro plano estiverem ociosos. Depois de exibir opcionalmente caixas de diálogo quando o provedor de transporte é conectado pela primeira vez, os provedores de transporte operam em segundo plano, a menos que o cliente tenha sido chamado pelo cliente para liberar filas de envio e recebimento. 
  
Os provedores de transporte têm as seguintes responsabilidades em um sistema de mensagens MAPI:
  
- Registre os tipos de endereço que eles podem aceitar com o spooler MAPI, para que o spooler MAPI possa enviar mensagens ao provedor de transporte apropriado, dependendo do endereço de destino das mensagens. Um provedor de transporte pode registrar mais de um tipo de endereço. Os provedores de transporte também podem registrar endereços de destinatários específicos com o spooler MAPI. As mensagens endereçadas a um desses endereços serão enviadas ao provedor de transporte que registrou o endereço com o spooler MAPI. Para obter mais informações, consulte [Transport Provider and MAPI spooler operaTing Model](transport-provider-and-mapi-spooler-operational-model.md).
    
- Entregar mensagens de entrada para o spooler MAPI. Dependendo da natureza do sistema de mensagens, um provedor de transporte pode notificar diretamente o spooler MAPI quando uma nova mensagem chega ou pode solicitar que o spooler MAPI sondar o provedor de transporte periodicamente para verificar se há novas mensagens.
    
- Converter Propriedades de mensagens MAPI de e para propriedades de mensagens nativas para o sistema de mensagens. Por exemplo, o provedor de transporte pode ter que converter os endereços do remetente e do destinatário em uma mensagem de saída para um formato que seja aceitável para o sistema de mensagens. Alguns sistemas de mensagens não dão suporte a todas as propriedades de mensagens MAPI. Para obter mais informações sobre como preservar as propriedades de mensagens MAPI ao entregar mensagens a um sistema de mensagens, consulte [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
    
- Registre as opções de mensagem e destinatário específicas para o provedor de transporte.
    
- Execute qualquer verificação de credenciais exigidas pelo sistema de mensagens.
    
- Acessar mensagens de saída usando o objeto Message passado para ele pelo spooler MAPI.
    
- Traduza o formato de mensagem conforme exigido pelo sistema de mensagens subjacente.
    
- Notificar o MAPI spooler de que os destinatários de uma mensagem de saída o provedor de transporte aceitou a responsabilidade de tratamento, definindo a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para esses destinatários.
    
- Informe o spooler MAPI quando uma mensagem de entrada precisa ser manipulada.
    
- Transmitir dados de mensagem de entrada para o spooler MAPI usando objetos Message.
    
- Atribua valores a todas as propriedades de mensagem MAPI necessárias em mensagens de entrada.
    
- Exclua a mensagem do sistema de mensagens subjacente após a entrega, se necessário.
    
- Fornecer informações de status para o spooler MAPI e aplicativos cliente.
    
A ilustração a seguir mostra a função de um provedor de transporte com relação aos outros componentes da arquitetura MAPI.
  
**Transport provider role in a messaging system**
  
![Função do provedor de transporte em um sistema de mensagens] (media/xp01.gif "Função do provedor de transporte em um sistema de mensagens")
  

