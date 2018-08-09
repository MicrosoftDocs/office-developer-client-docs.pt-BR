---
title: Seção MapiSvc.inf [Serviços padrão]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768018"
---
# <a name="mapisvcinf-default-services-section"></a>Seção MapiSvc.inf [Serviços padrão]

  
  
**Aplica-se a**: Outlook 
  
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


