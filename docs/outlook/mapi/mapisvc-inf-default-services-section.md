---
title: Seção MapiSvc. inf [serviços padrão]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435317"
---
# <a name="mapisvcinf-default-services-section"></a>Seção MapiSvc. inf [serviços padrão]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[default Services]** lista todos os serviços de mensagem selecionados como serviços de mensagens padrão. Esses serviços de mensagens padrão são um subconjunto dos serviços de mensagens listados na seção **[serviços]** . Quando um programa de configuração de perfil cria um perfil padrão, os serviços de mensagem nesta seção são incluídos automaticamente. 
  
As entradas usam o mesmo formato que as entradas na seção **[serviços]** , conforme mostrado a seguir: 
  
 **[Serviços padrão]**
  
 __ =  nome da seção do serviço de mensagens nome do_serviço_
  
As entradas a seguir seriam incluídas na seção **[default Services]** para o MAPISVC. inf mostrado na ilustração anterior: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


