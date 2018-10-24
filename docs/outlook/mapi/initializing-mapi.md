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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399036"
---
# <a name="initializing-mapi"></a>Iniciar MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os aplicativos de cliente que usam as bibliotecas MAPI devem chamar a função **MAPIInitialize** . Para obter mais informações, consulte [MAPIInitialize](mapiinitialize.md). **MAPIInitialize** inicializa dados globais para a sessão e prepara as bibliotecas MAPI aceite as chamadas. Existem alguns sinalizadores que são importantes para definir em determinadas situações: 
  
- MAPI_NT_SERVICE
    
    Defina o sinalizador MAPI_NT_SERVICE se seu cliente é implementado como um serviço do Windows. Se seu cliente é um serviço do Windows e você não definir esse sinalizador, MAPI não reconhecerá-lo como um serviço. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    O sinalizador MAPI_MULTITHREAD_NOTIFICATIONS se refere à como MAPI gerencia notificações. MAPI cria uma janela oculta que recebe mensagens de janela quando ocorrem alterações a um objeto gerar notificações. As mensagens de janela são processadas em algum momento, fazendo com que as notificações sejam enviadas e os métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) apropriados seja chamado. 
    
- MAPI_NO_COINIT
    
    Defina o sinalizador MAPI_NO_COINT para que **MAPIInitialize** não tenta inicializar COM uma chamada a [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx). Se uma estrutura **MAPIINIT_0** é passada para **MAPIInitialize** com _ulFlags_ definido como MAPI_NO_COINIT, MAPI partirá do pressuposto de que COM já foi inicializado e ignorar a chamada para **CoInitialize**.
    
Se o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS não for passado, MAPI cria a janela de notificação no thread que foi usada para a primeira chamada de **MAPIInitialize** . MAPI cria a janela de notificação em um segmento separado se passar MAPI_MULTITHREAD_NOTIFICATIONS — um thread dedicada para manipular notificações. MAPI espera o segmento que é usado para criar a janela de notificação oculto para: 
  
- Ter um loop de mensagem.
    
- Permanecem desbloqueadas em toda a duração da sessão.
    
- Ter uma vida útil mais longa que qualquer outro segmento criado por seu cliente. 
    
Você pode escolher qual thread é usado, definindo um sinalizador na primeira chamada **MAPIInitialize** . O perigo permitindo que um dos seus threads de lidar com as notificações é que, se o segmento desaparece, a janela de notificação é destruída e notificações não podem ser enviadas para qualquer um dos seus outros threads. Além disso, o processamento especial pode ser necessários para controlar o expedir das mensagens de notificação que são lançadas para a fila de mensagens da janela oculta. 
  
Se você usar uma janela separada para manipular notificações, ter certeza de que a notificação será exibida no momento apropriado em um segmento apropriado. Você não precisará qualquer código especial para procurar e processar as mensagens postadas na janela de notificação do Windows. 
  
MAPI recomenda que os seguintes tipos de aplicativos cliente usam um segmento separado para criar a janela oculta para suporte de notificação:
  
- Todos os clientes multithread.
    
- Aplicativos de console de serviços do Windows e Win32 com um único segmento.
    
- Clientes com um único segmento que não precisam usar seu thread principal para fins de notificação.
    
Para usar a abordagem de segmento separado, chame **MAPIInitialize** em cada segmento, definindo o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS. 
  
> [!NOTE]
> Apenas de um cliente primeira chamada ao **MAPIInitialize** faz com que uma janela oculta a ser criado para oferecer suporte a notificações. Subsequentes chama causa somente uma contagem de referência para ser incrementada. 
  

