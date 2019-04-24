---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Uma variável desse tipo de dados contém um valor binário.
ms.openlocfilehash: 3dcaaf73a04ddc608e68ca7bd1f801d0a5d99bb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316909"
---
# <a name="acctbin"></a><span data-ttu-id="9d653-103">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="9d653-103">ACCT_BIN</span></span>

<span data-ttu-id="9d653-104">Uma variável desse tipo de dados contém um valor binário.</span><span class="sxs-lookup"><span data-stu-id="9d653-104">A variable of this data type holds a binary value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9d653-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9d653-105">Quick info</span></span>

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a><span data-ttu-id="9d653-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9d653-106">Members</span></span>

<span data-ttu-id="9d653-107">_cb_</span><span class="sxs-lookup"><span data-stu-id="9d653-107">_cb_</span></span>
  
> <span data-ttu-id="9d653-108">Número de bytes aos quais _PB_ aponta.</span><span class="sxs-lookup"><span data-stu-id="9d653-108">Number of bytes that  _pb_ points to.</span></span> 
    
<span data-ttu-id="9d653-109">_pb_</span><span class="sxs-lookup"><span data-stu-id="9d653-109">_pb_</span></span>
  
> <span data-ttu-id="9d653-110">Ponteiro para informações binárias.</span><span class="sxs-lookup"><span data-stu-id="9d653-110">Pointer to binary information.</span></span>
    

