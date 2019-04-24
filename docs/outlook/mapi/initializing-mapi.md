---
title: Iniciar MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309727"
---
# <a name="initializing-mapi"></a>Iniciar MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os aplicativos clientes que usam as bibliotecas MAPI devem chamar a função **MAPIInitialize** . Para obter mais informações, consulte [MAPIInitialize](mapiinitialize.md). **MAPIInitialize** inicializa dados globais para a sessão e prepara as bibliotecas MAPI para aceitar chamadas. Há alguns sinalizadores que são importantes para definir em algumas situações: 
  
- MAPI_NT_SERVICE
    
    Defina o sinalizador MAPI_NT_SERVICE se o cliente for implementado como um serviço do Windows. Se o cliente for um serviço do Windows e você não definir esse sinalizador, o MAPI não o reconhecerá como um serviço. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    O sinalizador MAPI_MULTITHREAD_NOTIFICATIONS está relacionado à forma como o MAPI gerencia as notificações. O MAPI cria uma janela oculta que recebe mensagens de janela quando ocorrem alterações em um objeto que gera notificações. As mensagens de janela são processadas em algum momento, fazendo com que as notificações sejam enviadas e os métodos [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) apropriados a serem chamados. 
    
- MAPI_NO_COINIT
    
    Defina o sinalizador MAPI_NO_COINT para que o **MAPIInitialize** não tente inicializar com com uma chamada para CoInitialize. [](https://msdn.microsoft.com/library/ms886303.aspx) Se uma estrutura **MAPIINIT_0** for passada para o **MAPIInitialize** com _parâmetroulflags_ definido como MAPI_NO_COINIT, o MAPI presumirá que com já tenha sido inicializado e ignore a chamada para CoInitialize. ****
    
Se o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS não for passado, MAPI cria a janela de notificação no thread que foi usado para sua primeira chamada de **MAPIInitialize** . MAPI cria a janela de notificação em uma thread separada se MAPI_MULTITHREAD_NOTIFICATIONS for passado — um thread dedicado para lidar com notificações. MAPI espera o thread que é usado para criar a janela de notificação oculta para: 
  
- Ter um loop de mensagem.
    
- Permaneça desbloqueado ao longo da vida da sessão.
    
- Ter um tempo de vida maior do que qualquer outro thread criado pelo cliente. 
    
Você pode escolher qual thread é usado definindo um sinalizador na primeira chamada **MAPIInitialize** . O perigo de permitir que um dos seus threads Manipule as notificações é que, se o thread desaparecer, a janela de notificação é destruída e não é mais possível enviar notificações para qualquer um dos outros threads. Além disso, o processamento especial pode ser necessário para controlar a expedição das mensagens de notificação que são postadas na fila de mensagens da janela oculta. 
  
Se você usar uma janela separada para lidar com notificações, tenha certeza de que as notificações serão exibidas no momento apropriado em um thread apropriado. Você não precisará de nenhum código especial para verificar e processar as mensagens do Windows que são postadas na janela de notificação. 
  
MAPI recomenda que os seguintes tipos de aplicativos cliente usem um thread separado para criar a janela oculta para suporte de notificação:
  
- Todos os clientes multissegmentados.
    
- Serviços do Windows de thread único e aplicativos de console do Win32.
    
- Clientes de thread único que não precisam usar o thread principal para notificação.
    
Para usar a abordagem de thread separada, chame **MAPIInitialize** em todos os threads, definindo o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS. 
  
> [!NOTE]
> Somente a primeira chamada do cliente para o **MAPIInitialize** faz com que uma janela oculta seja criada para dar suporte a notificações. As chamadas subsequentes apenas fazem com que uma contagem de referência seja incrementada. 
  

