---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282772"
---
# <a name="sizedadrlist"></a><span data-ttu-id="c558e-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="c558e-103">SizedADRLIST</span></span>

<span data-ttu-id="c558e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c558e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c558e-105">Define uma estrutura [das ADRLIST](adrlist.md) com o nome especificado que contém um número especificado de estruturas [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="c558e-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c558e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c558e-106">Header file:</span></span>  <br/> |<span data-ttu-id="c558e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c558e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c558e-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="c558e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c558e-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="c558e-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="c558e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c558e-110">Parameters</span></span>

<span data-ttu-id="c558e-111">__cEntries_</span><span class="sxs-lookup"><span data-stu-id="c558e-111">__centries_</span></span>
  
> <span data-ttu-id="c558e-112">Contagem de estruturas **ADRENTRY** a serem incluídas na nova estrutura **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="c558e-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="c558e-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="c558e-113">__name_</span></span>
  
> <span data-ttu-id="c558e-114">Nome para a nova estrutura **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="c558e-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c558e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c558e-115">Remarks</span></span>

<span data-ttu-id="c558e-116">A macro **SizedADRLIST** permite definir uma lista de destinatários que tenha limites explícitos quando os requisitos de comprimento de matriz forem conhecidos.</span><span class="sxs-lookup"><span data-stu-id="c558e-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="c558e-117">O código a seguir mostra como converter o resultado da macro **SizedADRLIST** para um ponteiro de estrutura **das ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="c558e-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="c558e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c558e-118">See also</span></span>

- [<span data-ttu-id="c558e-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c558e-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="c558e-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="c558e-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="c558e-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="c558e-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

