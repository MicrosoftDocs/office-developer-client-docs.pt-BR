---
title: Garantir uma notificação Thread-Safe dados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424844"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantir uma notificação Thread-Safe dados

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se o cliente for executado em uma plataforma de vários threads, talvez seja necessário garantir que as chamadas para seus métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ocorram em um determinado thread. Como as chamadas para **OnNotify** normalmente podem ocorrer em qualquer thread, é possível receber notificações sobre threads inesperados e indesejados, levando a erros que são difíceis de depurar. 
  
Para garantir que as chamadas para **OnNotify** para uma notificação específica sejam feitas no mesmo thread que foi usado para a chamada **De** aviso, chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de chamar **Advise**. ** **HrThisThreadAdviseSink**** creates a new advise sink object from your advise sink object. Passe esse novo objeto na chamada para **Advise**. Todos os clientes com objetos sink aconselhados que podem não funcionar fora do contexto de um thread específico devem sempre registrar objetos sink de consultoria criados com **HrThisThreadAdviseSink**.
  

