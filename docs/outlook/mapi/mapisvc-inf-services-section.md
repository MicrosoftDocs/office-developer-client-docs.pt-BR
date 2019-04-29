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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434778"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="df157-103">Seção MapiSvc. inf [serviços]</span><span class="sxs-lookup"><span data-stu-id="df157-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="df157-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df157-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df157-105">A seção **[serviços]** lista os serviços de mensagens que estão instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="df157-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="df157-106">As entradas nesta seção usam o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="df157-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="df157-107">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="df157-107">**[Services]**</span></span>
  
 <span data-ttu-id="df157-108">__ =  nome da seção do serviço de mensagens nome do_serviço_</span><span class="sxs-lookup"><span data-stu-id="df157-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="df157-109">O nome da seção Message-Service é uma cadeia de caracteres definida pelo serviço de mensagens que vincula essa entrada a uma seção correspondente para o serviço em outro lugar no MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="df157-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="df157-110">O nome do serviço de mensagens é o nome do serviço instalado.</span><span class="sxs-lookup"><span data-stu-id="df157-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="df157-111">A seção a seguir mostra três serviços de mensagens: o catálogo de endereços padrão, meu próprio serviço e o serviço de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="df157-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="df157-112">Esses serviços são fictícios, apenas para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="df157-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="df157-113">Cada implementador de serviço de mensagens substituiria a entrada apropriada para o seu serviço de mensagens nesta seção.</span><span class="sxs-lookup"><span data-stu-id="df157-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="df157-114">Cada entrada desta seção tem uma seção correspondente de seu próprio local em que as informações do serviço de mensagens são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="df157-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="df157-115">Por exemplo, a seção correspondente para o catálogo de endereços padrão é chamada de [AB].</span><span class="sxs-lookup"><span data-stu-id="df157-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

