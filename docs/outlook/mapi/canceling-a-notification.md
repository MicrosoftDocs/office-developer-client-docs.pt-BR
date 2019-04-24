---
title: Cancelar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326401"
---
# <a name="canceling-a-notification"></a>Cancelar uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para cancelar uma notificação, os clientes chamam o método **Unadvise** de origem de um aviso. O **aviso** de chamada é importante porque faz com que o provedor de serviços Libere sua referência ao seu coletor de avisos. Desde que um provedor de serviços mantenha uma referência a um coletor de aviso, o coletor de avisos pode continuar a receber chamadas [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) . Na verdade, por causa da natureza assíncrona da notificação de eventos, os clientes podem ser notificados mesmo após uma chamada de **aviso** de cancelamento bem-sucedido. Os clientes devem ser capazes de lidar com o recebimento de notificações a qualquer momento. 
  
Como as implementações do provedor de serviços diferem, os clientes que não podem chamar **Unadvise** para cancelar uma notificação não poderão supor nada sobre quando um provedor vai liberar sua referência ao seu coletor de avisos. Alguns provedores de serviços liberam suas referências para avisar os coletores quando liberam suas fontes de aviso. Alguns provedores de serviços não. Desde que um provedor de serviços mantenha uma referência a um coletor de aviso, esse coletor de aviso pode continuar recebendo notificações. 
  

