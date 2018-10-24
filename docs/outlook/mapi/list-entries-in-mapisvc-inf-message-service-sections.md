---
title: Listar entradas nas seções do serviço de mensagens MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c5b5c468b56e5b34d265e7f00bbee96142a88e1c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591118"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Listar entradas nas seções do serviço de mensagens MapiSvc.inf

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Existem dois tipos de entradas da lista de seção: que lista seções do provedor de serviço e que lista seções de específico ao serviço de mensagem diversos. Esses dois tipos de entradas aparecem no Mapisvc usando os seguintes formatos:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Cada seção na entrada **provedores** mapeia para uma seção individual, fornecendo informações de configuração para um provedor de serviço que pertence ao serviço de mensagem. Cada seção na entrada **seções** mapeia para uma seção que contém informações de configuração adicional necessárias para o serviço de mensagem. Implementadores de serviço de mensagem definem seções extras, quando eles desejam incluir informações especiais que não se ajusta nas seções padrão. Serviços de mensagens que têm complicado configurações geralmente usam a entrada de **seções** para adicionar informações extras. Cada seção de serviços de mensagem tem uma entrada de **provedores** pelo menos uma seção na lista; nem todas as seções de serviço de mensagem têm uma entrada de **seções** . 
  
Dois exemplos das seções do serviço de mensagem a seguir. A primeira seção destina-se o serviço de catálogo de endereços padrão da ilustração anterior, um serviço de mensagem simples com um provedor de serviço único. A segunda seção é para o serviço MsgService, um serviço de mensagem de amostra mais complexo com três provedores de serviço. 
  
```cpp
[AB]
PR_DISPLAY_NAME=Default Address Book
Providers=AB Provider
PR_SERVICE_DLL_NAME=AB.DLL
PR_SERVICE_SUPPORT_FILES=AB.DLL
PR_SERVICE_ENTRY_NAME=DABServiceEntry
PR_RESOURCE_FLAGS=SERVICE_NO_PRIMARY_IDENTITY
[MsgService]
PR_DISPLAY_NAME=My Own Service
Providers=MsgService Prov1, MsgService Prov2, MsgService Prov3
Sections=First_Special_Section, Second_Special_Section
PR_SERVICE_DLL_NAME=MYSERV.DLL
PR_SERVICE_SUPPORT_FILES=MYSERV.DLL, MYXXX.DLL, MYZZZ.DLL
PR_SERVICE_ENTRY_NAME=MyServiceEntry
PR_RESOURCE_FLAGS=SERVICE_SINGLE_COPY
66040003=00000000

```

A entrada de **seções** na seção **[MsgService]** lista duas seções adicionais, um chamado **[First_Special_Section]** e a outra chamada **[Second_Special_Section]**. Os dados que podem aparecer nas seções extras são significativos para o serviço de mensagem específica. Estas seções aparecem para ilustrar extras seções seguintes. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


