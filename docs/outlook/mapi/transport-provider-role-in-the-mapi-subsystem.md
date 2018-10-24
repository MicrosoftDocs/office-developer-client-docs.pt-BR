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
ms.openlocfilehash: 263370590a35f19482cc5ad7e56c65f6df0087fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581297"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Função do provedor de transporte no subsistema MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Bibliotecas de vínculo dinâmico de provedor de transporte (DLLs) fornecem a interface entre o spooler MAPI e a parte de um sistema de mensagens responsável pelo envio e recebimento de mensagens. O spooler MAPI e o provedor de transporte funcionam em conjunto para lidar com as responsabilidades de enviar uma mensagem ou receber uma mensagem. O MAPI spooler carrega o provedor de transporte DLL quando ele é usado inicialmente e libera-lo quando ele não é mais necessária. Vários provedores de transporte que podem ser instalados no mesmo sistema, mas MAPI fornece o spooler de um necessários.
  
Aplicativos cliente não normalmente se comunicam diretamente com o provedor de transporte. Em vez disso, clientes enviar mensagens por meio de um provedor de armazenamento e o MAPI spooler envia mensagens de saída para o provedor de transporte apropriadas e entrega de mensagens de entrada para o repositório de mensagem apropriada. O MAPI spooler faz o seu trabalho e faz suas chamadas para provedores de transporte quando os aplicativos de primeiro plano ociosos. Depois, opcionalmente, exibindo caixas de diálogo quando o provedor de transporte é primeiro logon, provedores de transporte operam em segundo plano, a menos que chamado pelo cliente flush enviem e recebam filas. 
  
Provedores de transporte tem as seguintes responsabilidades em um sistema de mensagens de MAPI:
  
- Registre os tipos de endereço que eles podem aceitar o MAPI spooler portanto o MAPI spooler pode enviar mensagens para o provedor de transporte apropriadas dependendo das mensagens, o endereço de destino. Um provedor de transporte pode registrar mais de um tipo de endereço. Provedores de transporte também podem registrar os endereços de destinatários específicos com o spooler MAPI. As mensagens endereçadas a um desses endereços serão enviadas para o provedor de transporte que registrou o endereço com o spooler MAPI. Para obter mais informações, consulte o [provedor de transporte e o modelo operacional do Spooler de MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Entrega mensagens de entrada para o spooler MAPI. Dependendo da natureza do sistema de mensagens, um provedor de transporte pode seja diretamente notificar o MAPI spooler quando uma nova mensagem chega ou ele pode solicitar que o MAPI spooler sondar o provedor de transporte periodicamente para verificar se há novas mensagens.
    
- Converta propriedades de mensagem MAPI para e de propriedades de mensagem nativas do sistema de mensagens. Por exemplo, o provedor de transporte pode precisar converter endereços do remetente e do destinatário em uma mensagem de saída em um formulário que é aceitável para o sistema de mensagens. Alguns sistemas de mensagens não suportam todas as propriedades de mensagem MAPI. Para obter mais informações sobre como preservar as propriedades de mensagem MAPI quando a entrega de mensagens para um sistema de mensagens, consulte [desenvolvendo um provedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
    
- Registre as opções de mensagem e destinatário específicas do provedor de transporte.
    
- Execute qualquer verificação de credenciais exigidos pelo sistema de mensagens.
    
- Mensagens de saída do Access usando o objeto de mensagem passadas pelo spooler MAPI.
    
- Traduza o formato da mensagem conforme exigido pelo sistema de mensagens subjacente.
    
- Notifica o MAPI spooler quais destinatários de uma mensagem de saída que o provedor de transporte aceitou a responsabilidade para tratamento definindo a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para os destinatários.
    
- Informe o MAPI spooler quando uma mensagem de entrada precisa ser manipulados.
    
- Passe dados de mensagem de entrada para o MAPI spooler usando objetos de mensagem.
    
- Atribua valores para todas as propriedades obrigatórias de mensagem MAPI em mensagens de entrada.
    
- Exclua a mensagem do sistema de mensagens subjacente após a entrega, se necessário.
    
- Fornecer informações de status para os aplicativos cliente e o spooler MAPI.
    
A ilustração a seguir mostra a função de um provedor de transporte com relação as outros componentes da arquitetura do MAPI.
  
**Transport provider role in a messaging system**
  
![Função do provedor de transporte em um sistema de mensagens] (media/xp01.gif "Função do provedor de transporte em um sistema de mensagens")
  

