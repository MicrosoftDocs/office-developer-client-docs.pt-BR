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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327976"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="29323-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="29323-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="29323-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29323-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29323-105">Multiplica um inteiro de 32 bits não assinado por outro.</span><span class="sxs-lookup"><span data-stu-id="29323-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29323-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="29323-106">Header file:</span></span>  <br/> |<span data-ttu-id="29323-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="29323-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="29323-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="29323-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="29323-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="29323-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="29323-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="29323-110">Called by:</span></span>  <br/> |<span data-ttu-id="29323-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="29323-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="29323-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29323-112">Parameters</span></span>

 <span data-ttu-id="29323-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="29323-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="29323-114">no Uma palavra dupla que contém o inteiro de 32 bits não assinado a ser multiplicado pelo valor no parâmetro multiplicador __ .</span><span class="sxs-lookup"><span data-stu-id="29323-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="29323-115">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="29323-115">_Multiplier_</span></span>
  
> <span data-ttu-id="29323-116">no Uma palavra dupla que contém o multiplicador inteiro de 32 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="29323-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29323-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="29323-117">Return value</span></span>

<span data-ttu-id="29323-118">A função **FtMulDwDw** retorna uma estrutura [FILETIME](filetime.md) que contém o produto dos dois números inteiros.</span><span class="sxs-lookup"><span data-stu-id="29323-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="29323-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="29323-119">The two input parameters remain unchanged.</span></span> 
  

