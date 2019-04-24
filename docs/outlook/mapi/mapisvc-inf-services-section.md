---
title: Seção MapiSvc. inf [serviços]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270018"
---
# <a name="mapisvcinf-services-section"></a>Seção MapiSvc. inf [serviços]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[serviços]** lista os serviços de mensagens que estão instalados em um computador. As entradas nesta seção usam o seguinte formato: 
  
 **Serviço**
  
 __ =  nome da seção do serviço de mensagens nome do_serviço_
  
O nome da seção Message-Service é uma cadeia de caracteres definida pelo serviço de mensagens que vincula essa entrada a uma seção correspondente para o serviço em outro lugar no MAPISVC. inf. O nome do serviço de mensagens é o nome do serviço instalado. A seção a seguir mostra três serviços de mensagens: o catálogo de endereços padrão, meu próprio serviço e o serviço de repositório de mensagens. Esses serviços são fictícios, apenas para fins ilustrativos. Cada implementador de serviço de mensagens substituiria a entrada apropriada para o seu serviço de mensagens nesta seção.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Cada entrada desta seção tem uma seção correspondente de seu próprio local em que as informações do serviço de mensagens são armazenadas. Por exemplo, a seção correspondente para o catálogo de endereços padrão é chamada de [AB].
  

