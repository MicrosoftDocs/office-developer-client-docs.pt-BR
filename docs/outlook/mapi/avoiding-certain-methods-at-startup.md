---
title: Evitar determinados métodos na inicialização
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580632"
---
# <a name="avoiding-certain-methods-at-startup"></a>Evitar determinados métodos na inicialização

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para melhorar o desempenho em tempo de inicialização, evite fazendo as chamadas a seguintes:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
A chamada para **IMAPIStatus::ValidateState** afeta o desempenho somente quando feitas na lista o MAPI spooler ou subsistema de MAPI. A razão que esses métodos diminuir o processamento de inicialização é porque eles não é possível concluir até que o spooler MAPI concluiu suas tarefas de inicialização. 
  
Você também deve evitar pesquisar o armazenamento de mensagens em tempo de inicialização. Verifique sua chamada [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) quando tiver terminado de processamento de inicialização. 
  

