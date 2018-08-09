---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766632"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="9f30f-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="9f30f-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="9f30f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f30f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f30f-105">Multiplica um inteiro não assinado de 32 bits por outro.</span><span class="sxs-lookup"><span data-stu-id="9f30f-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f30f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9f30f-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f30f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9f30f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9f30f-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="9f30f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f30f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f30f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f30f-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="9f30f-110">Called by:</span></span>  <br/> |<span data-ttu-id="9f30f-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="9f30f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="9f30f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f30f-112">Parameters</span></span>

 <span data-ttu-id="9f30f-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="9f30f-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="9f30f-114">[in] Uma palavra dupla que contém o inteiro não assinado de 32 bits seja multiplicado pelo valor no parâmetro _multiplicador_ .</span><span class="sxs-lookup"><span data-stu-id="9f30f-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="9f30f-115">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="9f30f-115">_Multiplier_</span></span>
  
> <span data-ttu-id="9f30f-116">[in] Uma palavra dupla que contém o multiplicador de inteiro não assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9f30f-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f30f-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9f30f-117">Return value</span></span>

<span data-ttu-id="9f30f-118">A função **FtMulDwDw** retorna uma estrutura [FILETIME](filetime.md) que contém o produto dos dois valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="9f30f-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="9f30f-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="9f30f-119">The two input parameters remain unchanged.</span></span> 
  

