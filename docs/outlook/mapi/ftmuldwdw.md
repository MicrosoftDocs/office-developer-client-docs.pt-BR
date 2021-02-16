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
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412909"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="94cb3-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="94cb3-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="94cb3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94cb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94cb3-105">Multiplica um inteiro de 32 bits não assinado por outro.</span><span class="sxs-lookup"><span data-stu-id="94cb3-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94cb3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="94cb3-106">Header file:</span></span>  <br/> |<span data-ttu-id="94cb3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="94cb3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="94cb3-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="94cb3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="94cb3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="94cb3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="94cb3-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="94cb3-110">Called by:</span></span>  <br/> |<span data-ttu-id="94cb3-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="94cb3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="94cb3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94cb3-112">Parameters</span></span>

 <span data-ttu-id="94cb3-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="94cb3-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="94cb3-114">[in] Uma palavra dupla que contém o inteiro de 32 bits não assinado a ser multiplicado pelo valor no _parâmetro Multiplicador._</span><span class="sxs-lookup"><span data-stu-id="94cb3-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="94cb3-115">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="94cb3-115">_Multiplier_</span></span>
  
> <span data-ttu-id="94cb3-116">[in] Uma palavra dupla que contém o multiplicador de inteiro de 32 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="94cb3-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94cb3-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="94cb3-117">Return value</span></span>

<span data-ttu-id="94cb3-118">A **função FtMulDwDw** retorna uma estrutura [FILETIME](filetime.md) que contém o produto dos dois inteiros.</span><span class="sxs-lookup"><span data-stu-id="94cb3-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="94cb3-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="94cb3-119">The two input parameters remain unchanged.</span></span> 
  

