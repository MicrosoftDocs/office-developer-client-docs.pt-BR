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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423458"
---
# <a name="sizedadrlist"></a><span data-ttu-id="406f3-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="406f3-103">SizedADRLIST</span></span>

<span data-ttu-id="406f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="406f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="406f3-105">Define uma estrutura [ADRLIST](adrlist.md) com o nome especificado que contém um número especificado de estruturas [ADRENTRY.](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="406f3-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="406f3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="406f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="406f3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="406f3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="406f3-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="406f3-108">Related structure:</span></span>  <br/> |<span data-ttu-id="406f3-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="406f3-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="406f3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="406f3-110">Parameters</span></span>

<span data-ttu-id="406f3-111">_ _centries_</span><span class="sxs-lookup"><span data-stu-id="406f3-111">_ _centries_</span></span>
  
> <span data-ttu-id="406f3-112">Contagem de **estruturas ADRENTRY** a serem incluídas na nova **estrutura ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="406f3-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="406f3-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="406f3-113">_ _name_</span></span>
  
> <span data-ttu-id="406f3-114">Nome da nova **estrutura ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="406f3-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="406f3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="406f3-115">Remarks</span></span>

<span data-ttu-id="406f3-116">A macro **SizedADRLIST** permite definir uma lista de destinatários com limites explícitos quando os requisitos de comprimento da matriz são conhecidos.</span><span class="sxs-lookup"><span data-stu-id="406f3-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="406f3-117">O código a seguir mostra como lançar o resultado da macro **SizedADRLIST** em um ponteiro **de estrutura ADRLIST:**</span><span class="sxs-lookup"><span data-stu-id="406f3-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="406f3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="406f3-118">See also</span></span>

- [<span data-ttu-id="406f3-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="406f3-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="406f3-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="406f3-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="406f3-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="406f3-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

