---
title: Seção MapiSvc.inf [Services]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434778"
---
# <a name="mapisvcinf-services-section"></a>Seção MapiSvc.inf [Services]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **seção [Serviços]** lista os serviços de mensagem instalados em um computador. As entradas nesta seção usam o seguinte formato: 
  
 **[Serviços]**
  
 _nome da seção message-service_  =   _nome do serviço de mensagem_
  
O nome da seção de serviço de mensagens é uma cadeia de caracteres definida pelo serviço de mensagens que vincula essa entrada a uma seção correspondente para o serviço em outro lugar em mapisvc.inf. O nome do serviço de mensagens é o nome do serviço instalado. A seção a seguir mostra três serviços de mensagem: o Livro de Endereços Padrão, Meu Próprio Serviço e o Serviço de Armazenamento de Mensagens. Esses serviços são fictícios, apenas para fins ilustradores. Cada implementador de serviço de mensagens substituiria a entrada apropriada por seu serviço de mensagens nesta seção.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Cada entrada nesta seção tem uma seção correspondente própria onde as informações do serviço de mensagens são armazenadas. Por exemplo, a seção correspondente para o Livro de Endereços Padrão é chamada [AB].
  

