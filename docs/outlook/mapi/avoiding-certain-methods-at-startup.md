---
title: Evitando determinados métodos na inicialização
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: db327fdd239684140e4feeeb2a6045a2fcd5c410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766233"
---
# <a name="avoiding-certain-methods-at-startup"></a>Evitando determinados métodos na inicialização

 
  
**Aplica-se a**: Outlook 
  
Para melhorar o desempenho em tempo de inicialização, evite fazendo as chamadas a seguintes:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
A chamada para **IMAPIStatus::ValidateState** afeta o desempenho somente quando feitas na lista o MAPI spooler ou subsistema de MAPI. A razão que esses métodos diminuir o processamento de inicialização é porque eles não é possível concluir até que o spooler MAPI concluiu suas tarefas de inicialização. 
  
Você também deve evitar pesquisar o armazenamento de mensagens em tempo de inicialização. Verifique sua chamada [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) quando tiver terminado de processamento de inicialização. 
  

