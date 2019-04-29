---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408520"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="c25e1-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="c25e1-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="c25e1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c25e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c25e1-105">Decrementa a contagem de referência, limpa e exclui dados globais por instância da DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="c25e1-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c25e1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c25e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="c25e1-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="c25e1-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c25e1-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c25e1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c25e1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c25e1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c25e1-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c25e1-110">Called by:</span></span>  <br/> |<span data-ttu-id="c25e1-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c25e1-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="c25e1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c25e1-112">Parameters</span></span>

<span data-ttu-id="c25e1-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c25e1-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="c25e1-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c25e1-114">Return value</span></span>

<span data-ttu-id="c25e1-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c25e1-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c25e1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c25e1-116">Remarks</span></span>

<span data-ttu-id="c25e1-117">Um aplicativo cliente chama a função **MAPIUninitialize** para finalizar sua interação com MAPI, iniciado com uma chamada para a função [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="c25e1-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="c25e1-118">Após a chamada de **MAPIUninitialize** , nenhuma outra chamada MAPI pode ser feita pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="c25e1-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="c25e1-119">**MAPIUninitialize** decrementa a contagem de referência, e a função **MAPIInitialize** correspondente incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="c25e1-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="c25e1-120">Portanto, o número de chamadas para uma função deve ser igual ao número de chamadas para o outro.</span><span class="sxs-lookup"><span data-stu-id="c25e1-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c25e1-121">Você não pode chamar o **MAPIInitialize** ou o **MAPIUninitialize** de dentro de uma função **DllMain** do Win32 ou qualquer outra função que crie ou encerre threads.</span><span class="sxs-lookup"><span data-stu-id="c25e1-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="c25e1-122">Para obter mais informações, consulte [usando objetos isentos de threads](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c25e1-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

