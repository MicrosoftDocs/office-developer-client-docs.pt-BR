---
title: Copiando um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425390"
---
# <a name="copying-a-message-service"></a>Copiando um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para copiar um serviço de mensagens para um perfil**
  
- Chame [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Quando um serviço de mensagens é copiado, a nova instância do serviço é configurada exatamente da mesma maneira que o original. Às **vezes, CopyMsgService** retorna o erro MAPI_E_ACCESS_DENIED. A causa mais comum desse retorno de erro é um serviço de mensagens que não se permite ser duplicado. 
  

