---
title: Garantindo que uma notificação de Thread-Safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 70e594057f2d654e0527b0caa0951e44842df809
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766496"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantindo que uma notificação de Thread-Safe

  
  
**Aplica-se a**: Outlook 
  
Se seu cliente é executado em uma plataforma multithreaded, talvez você precise de garantia de que as chamadas para seus métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ocorrerem em um determinado thread. Porque as chamadas para **OnNotify** normalmente podem ocorrer em qualquer segmento, é possível receber notificações de threads inesperado e indesejado, levando a erros que são difíceis de depuração. 
  
Garantir que as chamadas para **OnNotify** para uma notificação em particular sejam feitas no mesmo thread que foi usado para o **Advise** chamada, chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de chamar **Advise**. * * * * HrThisThreadAdviseSink * * * cria um novo objeto coletor de eventos advise seu objeto de coletor de eventos advise. Passe este novo objeto na chamada a **Advise**. Todos os clientes com o coletor de eventos advise objetos que podem não funcionar fora do contexto de um determinado thread sempre devem registrar aconselhe os objetos de coletor de eventos criados com **HrThisThreadAdviseSink**.
  

