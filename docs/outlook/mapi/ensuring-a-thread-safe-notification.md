---
title: Garantir uma notificação de thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316580"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantir uma notificação de thread-safe

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se seu cliente é executado em uma plataforma multithread, talvez você precise de garantia de que as chamadas para os métodos [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) ocorram em um thread específico. Como as chamadas **** para onnotificar normalmente podem ocorrer em qualquer thread, é possível receber notificações em threads indesejados e indesejados, levando a erros difíceis de depurar. 
  
Para garantir que as chamadas **** para OnNotify para uma determinada notificação sejam feitas no mesmo thread que foi usado para a chamada de **aviso** , chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de chamar **Advise**. * * * * HrThisThreadAdviseSink * * * * cria um novo objeto de coletor de aviso do seu objeto de coletor de aviso. Passe este novo objeto na chamada para **Advise**. Todos os clientes com objetos de coletor de aviso que podem não funcionar fora do contexto de um determinado thread devem sempre registrar objetos de coletor de aviso criados com o **HrThisThreadAdviseSink**.
  

