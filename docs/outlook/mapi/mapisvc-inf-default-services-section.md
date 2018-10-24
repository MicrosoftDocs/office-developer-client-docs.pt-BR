---
title: Seção MapiSvc.inf [Serviços padrão]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573142"
---
# <a name="mapisvcinf-default-services-section"></a>Seção MapiSvc.inf [Serviços padrão]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[Padrão serviços]** lista todos os serviços de mensagem que são selecionados como serviços de mensagem padrão. Esses serviços de mensagem padrão são um subconjunto dos serviços de mensagem listadas na seção **[Services]** . Quando um programa de configuração do perfil cria um perfil padrão, os serviços de mensagem nesta seção são incluídos automaticamente. 
  
As entradas de usam o mesmo formato como entradas na seção **[Services]** , como mostrado seguinte: 
  
 **[Padrão Services]**
  
 _nome da seção do serviço de mensagem_ =  _nome do serviço de mensagem_
  
As entradas a seguir seriam incluídas na seção **[Services Default]** para o Mapisvc mostrado na ilustração anterior: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


