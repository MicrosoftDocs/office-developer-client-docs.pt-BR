---
title: Seção MapiSvc.inf [Serviços]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768023"
---
# <a name="mapisvcinf-services-section"></a>Seção MapiSvc.inf [Serviços]

  
  
**Aplica-se a**: Outlook 
  
A seção **[serviços]** lista os serviços de mensagem que são instalados em um computador. Entradas nesta seção usam o seguinte formato: 
  
 **[Services]**
  
 _nome da seção do serviço de mensagem_ =  _nome do serviço de mensagem_
  
O nome da seção do serviço de mensagem é que uma cadeia de caracteres definidos pelo serviço de mensagem que vincula essa entrada a uma seção correspondente para o serviço em algum lugar no Mapisvc. O nome do serviço de mensagem é o nome do serviço instalado. A seção a seguir mostra os três serviços de mensagem: o catálogo de endereços padrão, My Service próprio e o serviço de repositório de mensagem. Esses serviços são fictícios, apenas para fins ilustrativos. Cada implementador de serviço de mensagem seria substituir a entrada apropriada para seu serviço de mensagem nesta seção.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Cada entrada nesta seção tem uma seção correspondente do seu próprio onde as informações para o serviço de mensagem estão armazenadas. Por exemplo, a seção correspondente para o catálogo de endereços padrão é chamada [AB].
  

