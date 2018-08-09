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
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768157"
---
# <a name="mtsid"></a><span data-ttu-id="86948-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="86948-103">MTSID</span></span>

  
  
<span data-ttu-id="86948-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86948-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86948-105">Contém um identificador de entrada x. 400 mensagem transporte MTS (sistema).</span><span class="sxs-lookup"><span data-stu-id="86948-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86948-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="86948-106">Header file:</span></span>  <br/> |<span data-ttu-id="86948-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86948-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="86948-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="86948-108">Related macros:</span></span>  <br/> |<span data-ttu-id="86948-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="86948-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="86948-110">Members</span><span class="sxs-lookup"><span data-stu-id="86948-110">Members</span></span>

 <span data-ttu-id="86948-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="86948-111">**cb**</span></span>
  
> <span data-ttu-id="86948-112">Contagem de bytes na matriz descrito pelo membro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="86948-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="86948-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="86948-113">**abEntry**</span></span>
  
> <span data-ttu-id="86948-114">Matriz de bytes que contém os dados do identificador de entrada MTS.</span><span class="sxs-lookup"><span data-stu-id="86948-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86948-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="86948-115">Remarks</span></span>

<span data-ttu-id="86948-116">A estrutura **MTSID** é usada somente para mapeamentos de x. 400 dos identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="86948-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="86948-117">Ela corresponde à estrutura de MAPI [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="86948-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="86948-118">Um identificador MTS tem o mesmo formato apresentado um identificador de entrada MAPI ou um valor de propriedade binária.</span><span class="sxs-lookup"><span data-stu-id="86948-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="86948-119">Identificadores MTS podem ser particularmente útil para cancelamento de mensagens adiadas.</span><span class="sxs-lookup"><span data-stu-id="86948-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86948-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="86948-120">See also</span></span>



[<span data-ttu-id="86948-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="86948-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="86948-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="86948-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="86948-123">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="86948-123">MAPI Structures</span></span>](mapi-structures.md)

