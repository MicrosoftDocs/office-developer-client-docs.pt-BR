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
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585679"
---
# <a name="mtsid"></a><span data-ttu-id="ed5a9-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="ed5a9-103">MTSID</span></span>

  
  
<span data-ttu-id="ed5a9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed5a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed5a9-105">Contém um identificador de entrada x. 400 mensagem transporte MTS (sistema).</span><span class="sxs-lookup"><span data-stu-id="ed5a9-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed5a9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ed5a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed5a9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed5a9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ed5a9-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="ed5a9-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ed5a9-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="ed5a9-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="ed5a9-110">Members</span><span class="sxs-lookup"><span data-stu-id="ed5a9-110">Members</span></span>

 <span data-ttu-id="ed5a9-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="ed5a9-111">**cb**</span></span>
  
> <span data-ttu-id="ed5a9-112">Contagem de bytes na matriz descrito pelo membro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="ed5a9-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="ed5a9-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="ed5a9-113">**abEntry**</span></span>
  
> <span data-ttu-id="ed5a9-114">Matriz de bytes que contém os dados do identificador de entrada MTS.</span><span class="sxs-lookup"><span data-stu-id="ed5a9-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed5a9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed5a9-115">Remarks</span></span>

<span data-ttu-id="ed5a9-116">A estrutura **MTSID** é usada somente para mapeamentos de x. 400 dos identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed5a9-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="ed5a9-117">Ela corresponde à estrutura de MAPI [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="ed5a9-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="ed5a9-118">Um identificador MTS tem o mesmo formato apresentado um identificador de entrada MAPI ou um valor de propriedade binária.</span><span class="sxs-lookup"><span data-stu-id="ed5a9-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="ed5a9-119">Identificadores MTS podem ser particularmente útil para cancelamento de mensagens adiadas.</span><span class="sxs-lookup"><span data-stu-id="ed5a9-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed5a9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed5a9-120">See also</span></span>



[<span data-ttu-id="ed5a9-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="ed5a9-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="ed5a9-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="ed5a9-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="ed5a9-123">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="ed5a9-123">MAPI Structures</span></span>](mapi-structures.md)

