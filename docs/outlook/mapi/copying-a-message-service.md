---
title: Copiar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573716"
---
# <a name="copying-a-message-service"></a>Copiar um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para copiar um serviço de mensagem para um perfil**
  
- Chame [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Quando um serviço de mensagem é copiado, a nova instância do serviço é configurada exatamente da mesma maneira que o original. Em alguns casos, **CopyMsgService** retorna o erro MAPI_E_ACCESS_DENIED. A causa mais comum de retorno este erro é um serviço de mensagem que não permita a mesmo a ser duplicado. 
  

