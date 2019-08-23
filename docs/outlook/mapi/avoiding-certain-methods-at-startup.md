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
ms.openlocfilehash: 21aafebefcb7e10e6ba432f2eb3cc5dc04978c20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318085"
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
  

