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
  
Todos os aplicativos cliente que usam as bibliotecas MAPI devem chamar a **função MAPIInitialize.** Para obter mais informações, [consulte MAPIInitialize](mapiinitialize.md). **MAPIInitialize** inicializa dados globais para a sessão e prepara as bibliotecas MAPI para aceitar chamadas. Existem alguns sinalizadores que são importantes para definir em algumas situações: 
  
- MAPI_NT_SERVICE
    
    De definir o MAPI_NT_SERVICE de configuração se o cliente for implementado como um serviço do Windows. Se o cliente for um serviço do Windows e você não definir esse sinalizador, o MAPI não o reconhecerá como um serviço. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    O MAPI_MULTITHREAD_NOTIFICATIONS sinalizador está relacionado à forma como o MAPI gerencia as notificações. MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications. As mensagens de janela são processadas em algum momento, fazendo com que as notificações sejam enviadas e os métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) apropriados a serem chamados. 
    
- MAPI_NO_COINIT
    
    De definida MAPI_NO_COINT sinalizador para que **MAPIInitialize** não tente inicializar COM com uma chamada para [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx). Se uma estrutura **MAPIINIT_0** for passada para **MAPIInitialize** com  _ulFlags_ definido como MAPI_NO_COINIT, o MAPI assumirá que COM já foi inicializado e ignorará a chamada para **CoInitialize**.
    
Se MAPI_MULTITHREAD_NOTIFICATIONS sinalizador não for passado, o MAPI criará a janela de notificação no thread que foi usado para sua primeira chamada **MAPIInitialize.** MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications. O MAPI espera que o thread usado para criar a janela de notificação oculta para: 
  
- Ter um loop de mensagem.
    
- Permaneça desbloqueado durante toda a sessão.
    
- Ter um tempo de vida mais longo do que qualquer outro thread criado pelo cliente. 
    
Você pode escolher qual thread é usado definindo um sinalizador na primeira **chamada MAPIInitialize.** O risco de permitir que um de seus threads manipular as notificações é que, se o thread desaparecer, a janela de notificação será destruída e as notificações não poderão mais ser enviadas a nenhum dos outros threads. Além disso, pode ser necessário um processamento especial para controlar a expedição das mensagens de notificação publicadas na fila de mensagens da janela oculta. 
  
Se você usar uma janela separada para manipular notificações, tenha certeza de que as notificações aparecerão no momento apropriado em um thread apropriado. Você não precisará de nenhum código especial para verificar e processar as mensagens do Windows que são postadas na janela de notificação. 
  
A MAPI recomenda que os seguintes tipos de aplicativos cliente usem um thread separado para criar a janela oculta para suporte à notificação:
  
- Todos os clientes multithreaded.
    
- Serviços do Windows de thread único e aplicativos de console Win32.
    
- Clientes de thread único que não precisam usar seu thread principal para notificação.
    
Para usar a abordagem de thread separada, chame **MAPIInitialize** em cada thread, definindo o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS linha. 
  
> [!NOTE]
> Somente a primeira chamada de um cliente para **MAPIInitialize** faz com que uma janela oculta seja criada para dar suporte a notificações. Chamadas subsequentes só causam uma contagem de referência a ser incrementada. 
  

