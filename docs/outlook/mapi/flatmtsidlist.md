---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439216"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="fa92d-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="fa92d-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="fa92d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa92d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa92d-105">Contém uma matriz de [estruturas MTSID,](mtsid.md) cada uma contendo um identificador de entrada do sistema de transporte de mensagens (MTS) X.400.</span><span class="sxs-lookup"><span data-stu-id="fa92d-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa92d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fa92d-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa92d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa92d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fa92d-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="fa92d-108">Related macros:</span></span>  <br/> |<span data-ttu-id="fa92d-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="fa92d-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="fa92d-110">Members</span><span class="sxs-lookup"><span data-stu-id="fa92d-110">Members</span></span>

 <span data-ttu-id="fa92d-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="fa92d-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="fa92d-112">Contagem de **estruturas MTSID** na matriz descrita pelo **membro abMTSIDs.**</span><span class="sxs-lookup"><span data-stu-id="fa92d-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="fa92d-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="fa92d-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="fa92d-114">Contagem de bytes na matriz descrita por **abMTSIDs**.</span><span class="sxs-lookup"><span data-stu-id="fa92d-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="fa92d-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="fa92d-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="fa92d-116">Matriz de byte que contém uma ou mais **estruturas MTSID.**</span><span class="sxs-lookup"><span data-stu-id="fa92d-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa92d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa92d-117">Remarks</span></span>

<span data-ttu-id="fa92d-118">O uso da estrutura **FLATMTSIDLIST** em mensagens X.400 corresponde ao uso da estrutura [FLATENTRYLIST](flatentrylist.md) em mensagens MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa92d-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="fa92d-119">O MAPI usa **estruturas FLATMTSIDLIST** para manter propriedades X.400 durante o tratamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fa92d-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="fa92d-120">Os provedores de serviços usam **estruturas FLATMTSIDLIST** ao lidar com mensagens X.400 de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="fa92d-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="fa92d-121">Na matriz **abMTSIDs,** cada estrutura **MTSID** é alinhada em um limite alinhado naturalmente.</span><span class="sxs-lookup"><span data-stu-id="fa92d-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="fa92d-122">Bytes extras são incluídos como preenchimento para garantir o alinhamento natural entre duas estruturas **MTSID.**</span><span class="sxs-lookup"><span data-stu-id="fa92d-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="fa92d-123">A primeira **estrutura MTSID** na matriz é sempre alinhada corretamente porque o deslocamento do membro **abMTSIDs** é 8.</span><span class="sxs-lookup"><span data-stu-id="fa92d-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="fa92d-124">Para calcular o deslocamento da próxima estrutura, use o tamanho da primeira entrada arredondada para o próximo múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="fa92d-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="fa92d-125">Use a macro [CbNewMTSID](cbnewmtsid.md) para calcular o tamanho de uma **estrutura MTSID.**</span><span class="sxs-lookup"><span data-stu-id="fa92d-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa92d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa92d-126">See also</span></span>



[<span data-ttu-id="fa92d-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="fa92d-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="fa92d-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="fa92d-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="fa92d-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="fa92d-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="fa92d-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="fa92d-130">MAPI Structures</span></span>](mapi-structures.md)

