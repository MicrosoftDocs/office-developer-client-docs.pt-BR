---
title: Seção MapiSvc.inf [Serviços]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 520478061e192f9fec97c6b13edde7833a13a3d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571392"
---
# <a name="mapisvcinf-services-section"></a>Seção MapiSvc.inf [Serviços]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

