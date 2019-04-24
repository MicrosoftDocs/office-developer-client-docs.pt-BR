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
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338560"
---
# <a name="msgcallrelease"></a><span data-ttu-id="32678-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="32678-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="32678-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32678-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32678-105">Define uma função de retorno de chamada que pode liberar uma interface **IStorage** após a versão final de um objeto **IMessage** criado com a função [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="32678-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32678-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="32678-106">Header file:</span></span>  <br/> |<span data-ttu-id="32678-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="32678-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="32678-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="32678-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="32678-109">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="32678-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="32678-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="32678-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="32678-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="32678-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="32678-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32678-112">Parameters</span></span>

 <span data-ttu-id="32678-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="32678-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="32678-114">no Contém informações de aplicativo de chamada sobre a interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="32678-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="32678-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="32678-115">_lpMessage_</span></span>
  
> <span data-ttu-id="32678-116">no Ponteiro para a mensagem e os anexos de nível superior que foram liberados.</span><span class="sxs-lookup"><span data-stu-id="32678-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32678-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="32678-117">Return value</span></span>

<span data-ttu-id="32678-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="32678-118">None.</span></span>
  

