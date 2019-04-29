---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435170"
---
# <a name="mtsid"></a><span data-ttu-id="4575f-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="4575f-103">MTSID</span></span>

  
  
<span data-ttu-id="4575f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4575f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4575f-105">Contém um identificador de entrada MTS (sistema de transporte de mensagens) X. 400.</span><span class="sxs-lookup"><span data-stu-id="4575f-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4575f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4575f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4575f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4575f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4575f-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="4575f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="4575f-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="4575f-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="4575f-110">Members</span><span class="sxs-lookup"><span data-stu-id="4575f-110">Members</span></span>

 <span data-ttu-id="4575f-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="4575f-111">**cb**</span></span>
  
> <span data-ttu-id="4575f-112">Contagem de bytes na matriz descrita pelo membro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="4575f-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="4575f-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="4575f-113">**abEntry**</span></span>
  
> <span data-ttu-id="4575f-114">Matriz de bytes que contém os dados do identificador de entrada MTS.</span><span class="sxs-lookup"><span data-stu-id="4575f-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4575f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4575f-115">Remarks</span></span>

<span data-ttu-id="4575f-116">A estrutura **MTSID** é usada apenas para mapeamentos X. 400 de identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="4575f-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="4575f-117">Ela corresponde à estrutura [FLATENTRY](flatentry.md) MAPI.</span><span class="sxs-lookup"><span data-stu-id="4575f-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="4575f-118">Um identificador MTS tem o mesmo formato que um identificador de entrada MAPI ou um valor de propriedade binária.</span><span class="sxs-lookup"><span data-stu-id="4575f-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="4575f-119">Os identificadores MTS podem ser particularmente úteis para cancelar mensagens adiadas.</span><span class="sxs-lookup"><span data-stu-id="4575f-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4575f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4575f-120">See also</span></span>



[<span data-ttu-id="4575f-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="4575f-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="4575f-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="4575f-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="4575f-123">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="4575f-123">MAPI Structures</span></span>](mapi-structures.md)

