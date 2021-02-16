---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406343"
---
# <a name="ftmuldw"></a><span data-ttu-id="8cde8-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="8cde8-103">FtMulDw</span></span>

  
  
<span data-ttu-id="8cde8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cde8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cde8-105">Multiplica um inteiro de 64 bits não assinado por um inteiro de 32 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="8cde8-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8cde8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8cde8-106">Header file:</span></span>  <br/> |<span data-ttu-id="8cde8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8cde8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8cde8-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="8cde8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8cde8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8cde8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8cde8-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="8cde8-110">Called by:</span></span>  <br/> |<span data-ttu-id="8cde8-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="8cde8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="8cde8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cde8-112">Parameters</span></span>

 <span data-ttu-id="8cde8-113">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="8cde8-113">_Multiplier_</span></span>
  
> <span data-ttu-id="8cde8-114">[in] Uma palavra dupla que contém o multiplicador de inteiro de 32 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="8cde8-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="8cde8-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="8cde8-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="8cde8-116">[in] Uma [estrutura FILETIME](filetime.md) que contém o inteiro de 64 bits não assinado a ser multiplicado pelo valor no parâmetro _Multiplicador._</span><span class="sxs-lookup"><span data-stu-id="8cde8-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8cde8-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8cde8-117">Return value</span></span>

<span data-ttu-id="8cde8-118">A **função FtMulDw** retorna uma estrutura **FILETIME** que contém o produto dos dois inteiros.</span><span class="sxs-lookup"><span data-stu-id="8cde8-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="8cde8-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="8cde8-119">The two input parameters remain unchanged.</span></span> 
  

