---
title: Evitar determinados métodos na inicialização
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Última modificação: 07 de dezembro de 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580632"
---
# <a name="avoiding-certain-methods-at-startup"></a>Evitar determinados métodos na inicialização

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para melhorar o desempenho no momento da inicialização, evite fazer seguintes chamadas:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
Chamadas para **IMAPIStatus::ValidateState** afetam o desempenho somente quando feitas no spooler MAPI ou no subsistema MAPI. O motivo pelo qual esses métodos reduzem a velocidade do processo de inicialização é porque eles não podem se concluir até que o spooler MAPI termine suas tarefas de inicialização. 
  
Você deve evitar pesquisar o repositório de mensagens no momento da inicialização. Verifique sua chamada [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) quando to processo de inicialização for concluído. 
  

