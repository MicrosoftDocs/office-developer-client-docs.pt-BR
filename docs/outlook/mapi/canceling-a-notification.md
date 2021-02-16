---
title: Cancelando uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409759"
---
# <a name="canceling-a-notification"></a>Cancelando uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para cancelar uma notificação, os clientes chamam o método **Unadvise** de uma fonte de aviso. Chamar **Unadvise é** importante porque faz com que o provedor de serviços libere sua referência ao seu cliente de consultoria. Contanto que um provedor de serviços mantenha uma referência a um sink de aconselhador, o evento de alerta pode continuar a receber chamadas [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md) Na verdade, devido à natureza assíncrona da notificação de eventos, os clientes podem ser notificados mesmo depois de uma chamada Não **Prevista** bem-sucedida. Os clientes devem ser capazes de lidar com o recebimento de notificações a qualquer momento. 
  
Como as implementações do provedor de serviços são diferentes, os clientes que não conseguem chamar **Unadvise** para cancelar uma notificação não podem assumir nada sobre quando um provedor liberará sua referência ao seu cliente de aviso. Alguns provedores de serviços liberam suas referências para avisar os clientes quando liberam suas fontes de consultoria. Alguns provedores de serviços não. Contanto que um provedor de serviços mantenha uma referência a um sink de aviso, esse evento de aviso pode continuar a receber notificações. 
  

