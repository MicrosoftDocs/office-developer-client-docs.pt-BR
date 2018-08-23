---
title: Seção MapiSvc.inf [Serviços]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 520478061e192f9fec97c6b13edde7833a13a3d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571392"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="269fc-103">Seção MapiSvc.inf [Serviços]</span><span class="sxs-lookup"><span data-stu-id="269fc-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="269fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="269fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="269fc-105">A seção **[serviços]** lista os serviços de mensagem que são instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="269fc-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="269fc-106">Entradas nesta seção usam o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="269fc-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="269fc-107">**[Services]**</span><span class="sxs-lookup"><span data-stu-id="269fc-107">**[Services]**</span></span>
  
 <span data-ttu-id="269fc-108">_nome da seção do serviço de mensagem_ =  _nome do serviço de mensagem_</span><span class="sxs-lookup"><span data-stu-id="269fc-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="269fc-109">O nome da seção do serviço de mensagem é que uma cadeia de caracteres definidos pelo serviço de mensagem que vincula essa entrada a uma seção correspondente para o serviço em algum lugar no Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="269fc-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="269fc-110">O nome do serviço de mensagem é o nome do serviço instalado.</span><span class="sxs-lookup"><span data-stu-id="269fc-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="269fc-111">A seção a seguir mostra os três serviços de mensagem: o catálogo de endereços padrão, My Service próprio e o serviço de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="269fc-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="269fc-112">Esses serviços são fictícios, apenas para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="269fc-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="269fc-113">Cada implementador de serviço de mensagem seria substituir a entrada apropriada para seu serviço de mensagem nesta seção.</span><span class="sxs-lookup"><span data-stu-id="269fc-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="269fc-114">Cada entrada nesta seção tem uma seção correspondente do seu próprio onde as informações para o serviço de mensagem estão armazenadas.</span><span class="sxs-lookup"><span data-stu-id="269fc-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="269fc-115">Por exemplo, a seção correspondente para o catálogo de endereços padrão é chamada [AB].</span><span class="sxs-lookup"><span data-stu-id="269fc-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

