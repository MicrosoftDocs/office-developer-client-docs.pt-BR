---
title: Listar entradas nas seções do serviço de mensagens MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cfb06e8dd305add6049d035c44685be047dc744f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767763"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="15137-103">Listar entradas nas seções do serviço de mensagens MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="15137-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="15137-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15137-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15137-105">Existem dois tipos de entradas da lista de seção: que lista seções do provedor de serviço e que lista seções de específico ao serviço de mensagem diversos.</span><span class="sxs-lookup"><span data-stu-id="15137-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="15137-106">Esses dois tipos de entradas aparecem no Mapisvc usando os seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="15137-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="15137-107">Cada seção na entrada **provedores** mapeia para uma seção individual, fornecendo informações de configuração para um provedor de serviço que pertence ao serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="15137-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="15137-108">Cada seção na entrada **seções** mapeia para uma seção que contém informações de configuração adicional necessárias para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="15137-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="15137-109">Implementadores de serviço de mensagem definem seções extras, quando eles desejam incluir informações especiais que não se ajusta nas seções padrão.</span><span class="sxs-lookup"><span data-stu-id="15137-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="15137-110">Serviços de mensagens que têm complicado configurações geralmente usam a entrada de **seções** para adicionar informações extras.</span><span class="sxs-lookup"><span data-stu-id="15137-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="15137-111">Cada seção de serviços de mensagem tem uma entrada de **provedores** pelo menos uma seção na lista; nem todas as seções de serviço de mensagem têm uma entrada de **seções** .</span><span class="sxs-lookup"><span data-stu-id="15137-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="15137-112">Dois exemplos das seções do serviço de mensagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="15137-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="15137-113">A primeira seção destina-se o serviço de catálogo de endereços padrão da ilustração anterior, um serviço de mensagem simples com um provedor de serviço único.</span><span class="sxs-lookup"><span data-stu-id="15137-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="15137-114">A segunda seção é para o serviço MsgService, um serviço de mensagem de amostra mais complexo com três provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="15137-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="15137-115">A entrada de **seções** na seção **[MsgService]** lista duas seções adicionais, um chamado **[First_Special_Section]** e a outra chamada **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="15137-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="15137-116">Os dados que podem aparecer nas seções extras são significativos para o serviço de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="15137-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="15137-117">Estas seções aparecem para ilustrar extras seções seguintes.</span><span class="sxs-lookup"><span data-stu-id="15137-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


