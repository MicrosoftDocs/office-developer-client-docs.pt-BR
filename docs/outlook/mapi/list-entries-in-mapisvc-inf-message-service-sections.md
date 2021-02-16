---
title: Listar entradas em Seções do Serviço de Mensagens MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435926"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Listar entradas em Seções do Serviço de Mensagens MapiSvc.inf

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há dois tipos de entradas de lista de seções: um que lista seções do provedor de serviços e outro que lista diversas seções específicas do serviço de mensagens. Esses dois tipos de entradas aparecem em mapisvc.inf usando os seguintes formatos:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Cada seção na entrada **Provedores** mapeia para uma seção individual que fornece informações de configuração para um provedor de serviços que pertence ao serviço de mensagens. Cada seção na entrada **Seções** é mapeada para uma seção que contém informações adicionais de configuração necessárias para o serviço de mensagens. Os implementadores de serviço de mensagens definem seções extras quando quiserem incluir informações especiais que não se encaixem nas seções padrão. Os serviços de mensagens que têm configurações complicadas normalmente usam **a entrada Seções** para adicionar informações extras. Cada seção de serviços de mensagens tem **uma entrada provedores** com pelo menos uma seção na lista; nem todas as seções do serviço de mensagens têm **uma entrada de Seções.** 
  
Seguem dois exemplos de seções do serviço de mensagens. A primeira seção é para o serviço de Agenda Padrão da ilustração anterior, um serviço de mensagens simples com um único provedor de serviços. A segunda seção é para o serviço MsgService, um serviço de mensagens de exemplo mais complexo com três provedores de serviços. 
  
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

A **entrada Seções** na seção **[MsgService]** lista duas seções adicionais, uma chamada **[First_Special_Section]** e a outra chamada **[Second_Special_Section]**. Os dados que podem aparecer em seções extras são significativos para o serviço de mensagens específico. Estas seções aparecem a seguir para ilustrar seções extras. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


