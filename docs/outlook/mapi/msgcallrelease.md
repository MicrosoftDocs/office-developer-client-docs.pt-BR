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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405909"
---
# <a name="msgcallrelease"></a><span data-ttu-id="573ba-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="573ba-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="573ba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="573ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="573ba-105">Define uma função de retorno de chamada que pode liberar uma interface **IStorage** após o lançamento final de um objeto **IMessage** criado sobre ele com a função [OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="573ba-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="573ba-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="573ba-106">Header file:</span></span>  <br/> |<span data-ttu-id="573ba-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="573ba-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="573ba-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="573ba-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="573ba-109">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="573ba-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="573ba-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="573ba-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="573ba-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="573ba-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="573ba-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="573ba-112">Parameters</span></span>

 <span data-ttu-id="573ba-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="573ba-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="573ba-114">[in] Contém informações de aplicativo de chamada sobre a interface **IMessage.**</span><span class="sxs-lookup"><span data-stu-id="573ba-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="573ba-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="573ba-115">_lpMessage_</span></span>
  
> <span data-ttu-id="573ba-116">[in] Ponteiro para a mensagem de nível superior e anexos que foram liberados.</span><span class="sxs-lookup"><span data-stu-id="573ba-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="573ba-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="573ba-117">Return value</span></span>

<span data-ttu-id="573ba-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="573ba-118">None.</span></span>
  

