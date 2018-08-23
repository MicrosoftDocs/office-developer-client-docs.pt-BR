---
title: Garantindo uma notificação livre de threads
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ad10b2ebd835b21f207fd43ecd8aebc7e1f475f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585301"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantindo uma notificação livre de threads

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se seu cliente é executado em uma plataforma multithreaded, talvez você precise de garantia de que as chamadas para seus métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ocorrerem em um determinado thread. Porque as chamadas para **OnNotify** normalmente podem ocorrer em qualquer segmento, é possível receber notificações de threads inesperado e indesejado, levando a erros que são difíceis de depuração. 
  
Garantir que as chamadas para **OnNotify** para uma notificação em particular sejam feitas no mesmo thread que foi usado para o **Advise** chamada, chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de chamar **Advise**. * * * * HrThisThreadAdviseSink * * * cria um novo objeto coletor de eventos advise seu objeto de coletor de eventos advise. Passe este novo objeto na chamada a **Advise**. Todos os clientes com o coletor de eventos advise objetos que podem não funcionar fora do contexto de um determinado thread sempre devem registrar aconselhe os objetos de coletor de eventos criados com **HrThisThreadAdviseSink**.
  

