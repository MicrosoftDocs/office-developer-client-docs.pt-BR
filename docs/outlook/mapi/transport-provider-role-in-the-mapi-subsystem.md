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
  
As bibliotecas de vínculo dinâmico (DLLs) do provedor de transporte fornecem a interface entre o spooler MAPI e a parte de um sistema de mensagens responsável pelo envio e recebimento de mensagens. O spooler MAPI e o provedor de transporte trabalham juntos para lidar com as responsabilidades de enviar uma mensagem ou receber uma mensagem. O spooler MAPI carrega a DLL do provedor de transporte quando ele é usado pela primeira vez e o libera quando não é mais necessário. Vários provedores de transporte podem ser instalados no mesmo sistema, mas o MAPI fornece o spooler necessário.
  
Os aplicativos cliente normalmente não se comunicam diretamente com o provedor de transporte. Em vez disso, os clientes enviam mensagens por meio de um provedor de armazenamento e o spooler MAPI envia mensagens de saída para o provedor de transporte apropriado e entrega mensagens de entrada para o armazenamento de mensagens apropriado. O spooler MAPI faz seu trabalho e faz suas chamadas para provedores de transporte quando os aplicativos em primeiro plano estão ociosos. Depois de exibir opcionalmente caixas de diálogo quando o provedor de transporte é conectado pela primeira vez, os provedores de transporte operam em segundo plano, a menos que seja chamado pelo cliente para liberar filas de envio e recebimento. 
  
Os provedores de transporte têm as seguintes responsabilidades em um sistema de mensagens MAPI:
  
- Registre os tipos de endereço que eles podem aceitar com o spooler MAPI para que o spooler MAPI possa enviar mensagens para o provedor de transporte apropriado, dependendo do endereço de destino das mensagens. Um provedor de transporte pode registrar mais de um tipo de endereço. Os provedores de transporte também podem registrar endereços de destinatários específicos com o spooler MAPI. As mensagens endereçadas a um desses endereços serão enviadas ao provedor de transporte que registrou o endereço com o spooler MAPI. Para obter mais informações, [consulte o Provedor de Transporte e o Modelo Operacional do Spooler MAPI.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Entregar mensagens de entrada ao spooler MAPI. Dependendo da natureza do sistema de mensagens, um provedor de transporte pode notificar diretamente o spooler MAPI quando uma nova mensagem chega ou pode solicitar que o spooler MAPI sondar periodicamente o provedor de transporte para verificar se há novas mensagens.
    
- Converter propriedades de mensagem MAPI de e para propriedades de mensagem nativas para o sistema de mensagens. Por exemplo, o provedor de transporte pode ter que converter os endereços do remetente e do destinatário em uma mensagem de saída para um formulário que seja aceitável para o sistema de mensagens. Alguns sistemas de mensagens não suportam todas as propriedades de mensagens MAPI. Para obter mais informações sobre como preservar propriedades de mensagens MAPI ao entregar mensagens para um sistema de mensagens, [consulte Desenvolvendo](developing-a-tnef-enabled-transport-provider.md)um provedor de TNEF-Enabled transporte de mensagens.
    
- Registre opções de mensagem e destinatário específicas para o provedor de transporte.
    
- Execute qualquer verificação das credenciais exigidas pelo sistema de mensagens.
    
- Acessar mensagens de saída usando o objeto de mensagem passado a ela pelo spooler MAPI.
    
- Traduza o formato da mensagem conforme exigido pelo sistema de mensagens subjacente.
    
- Notifique o spooler MAPI que destinatários de uma mensagem de saída o provedor de transporte aceitou a responsabilidade pelo tratamento definindo a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para esses destinatários.
    
- Informe o spooler MAPI quando uma mensagem de entrada precisar ser tratada.
    
- Passe dados de mensagem de entrada para o spooler MAPI usando objetos de mensagem.
    
- Atribua valores a todas as propriedades de mensagem MAPI necessárias em mensagens de entrada.
    
- Exclua a mensagem do sistema de mensagens subjacente após a entrega, se necessário.
    
- Forneça informações de status para o spooler MAPI e aplicativos cliente.
    
A ilustração a seguir mostra a função de um provedor de transporte em relação aos outros componentes da arquitetura MAPI.
  
**Transport provider role in a messaging system**
  
![Função de provedor de transporte em uma função de provedor]de Transporte do sistema de mensagens em um sistema de(media/xp01.gif "mensagens")
  

