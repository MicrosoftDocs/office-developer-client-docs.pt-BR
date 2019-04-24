---
title: Listar entradas nas seções do serviço de mensagens MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307830"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="b9ea4-103">Listar entradas nas seções do serviço de mensagens MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="b9ea4-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="b9ea4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9ea4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9ea4-105">Há dois tipos de entradas da lista de seções: um que lista as seções do provedor de serviços e uma que lista diversas seções específicas do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="b9ea4-106">Esses dois tipos de entradas aparecem no MAPISVC. inf usando os seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="b9ea4-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="b9ea4-107">Cada seção na entrada **Providers** mapeia para uma seção individual que fornece informações de configuração para um provedor de serviços que pertence ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="b9ea4-108">Cada seção na entrada **Sections** mapeia para uma seção que contém informações adicionais de configuração necessárias para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="b9ea4-109">Os implementadores de serviço de mensagens definem seções adicionais quando desejam incluir informações especiais que não se ajustam às seções padrão.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="b9ea4-110">Os serviços de mensagens que possuem configurações complicadas \*\*\*\* normalmente usam a entrada Sections para adicionar informações extras.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="b9ea4-111">Cada seção de serviços de mensagem tem uma entrada de **provedores** com pelo menos uma seção na lista; Nem todas as seções do serviço de mensagens têm uma entrada de **seções** .</span><span class="sxs-lookup"><span data-stu-id="b9ea4-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="b9ea4-112">Dois exemplos de seções do serviço de mensagens são apresentados a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="b9ea4-113">A primeira seção é para o serviço de catálogo de endereços padrão na ilustração anterior, um serviço de mensagens simples com um único provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="b9ea4-114">A segunda seção é para o serviço MsgService, um serviço de mensagens de exemplo mais complexo com três provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="b9ea4-115">A \*\*\*\* entrada Sections na seção **[MsgService]** lista duas seções adicionais, uma chamada **[First_Special_Section]** e a outra chamada **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="b9ea4-116">Os dados que podem aparecer em seções extras são significativos para o serviço de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="b9ea4-117">Essas seções são exibidas abaixo para ilustrar seções adicionais.</span><span class="sxs-lookup"><span data-stu-id="b9ea4-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


