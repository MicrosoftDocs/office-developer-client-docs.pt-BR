---
title: Copiar um serviço de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766300"
---
# <a name="copying-a-message-service"></a>Copiar um serviço de mensagem

  
  
**Aplica-se a**: Outlook 
  
 **Para copiar um serviço de mensagem para um perfil**
  
- Chame [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Quando um serviço de mensagem é copiado, a nova instância do serviço é configurada exatamente da mesma maneira que o original. Em alguns casos, **CopyMsgService** retorna o erro MAPI_E_ACCESS_DENIED. A causa mais comum de retorno este erro é um serviço de mensagem que não permita a mesmo a ser duplicado. 
  

