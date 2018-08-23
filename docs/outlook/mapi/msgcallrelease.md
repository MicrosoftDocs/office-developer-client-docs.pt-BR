---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573184"
---
# <a name="msgcallrelease"></a><span data-ttu-id="ba03b-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="ba03b-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="ba03b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba03b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba03b-105">Define uma função de retorno de chamada que pode liberar uma interface **IStorage** após o lançamento final de um objeto **IMessage** construído sobre ele com a função [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="ba03b-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba03b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ba03b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba03b-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="ba03b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="ba03b-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="ba03b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="ba03b-109">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ba03b-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="ba03b-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="ba03b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="ba03b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ba03b-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="ba03b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba03b-112">Parameters</span></span>

 <span data-ttu-id="ba03b-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="ba03b-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="ba03b-114">[in] Contém informações de aplicativo chamada sobre a interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="ba03b-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="ba03b-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ba03b-115">_lpMessage_</span></span>
  
> <span data-ttu-id="ba03b-116">[in] Ponteiro para a mensagem de nível superior e os anexos que foram liberados.</span><span class="sxs-lookup"><span data-stu-id="ba03b-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba03b-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ba03b-117">Return value</span></span>

<span data-ttu-id="ba03b-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ba03b-118">None.</span></span>
  

