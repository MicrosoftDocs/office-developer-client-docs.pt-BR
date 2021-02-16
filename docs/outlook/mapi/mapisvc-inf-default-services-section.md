---
title: Seção MapiSvc.inf [Serviços Padrão]
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
# <a name="mapisvcinf-default-services-section"></a>Seção MapiSvc.inf [Serviços Padrão]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **seção [Serviços Padrão]** lista todos os serviços de mensagens selecionados como serviços de mensagem padrão. Esses serviços de mensagens padrão são um subconjunto dos serviços de mensagem listados **na seção [Serviços].** Quando um programa de configuração de perfil cria um perfil padrão, os serviços de mensagem nesta seção são incluídos automaticamente. 
  
As entradas usam o mesmo formato das entradas na seção **[Serviços],** conforme mostrado a seguir: 
  
 **[Serviços Padrão]**
  
 _nome da seção message-service_  =   _nome do serviço de mensagem_
  
As entradas a seguir seriam incluídas na seção **[Serviços Padrão]** para o mapisvc.inf mostrado na ilustração anterior: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


