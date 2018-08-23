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
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574738"
---
# <a name="sizedadrlist"></a><span data-ttu-id="dd5a2-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="dd5a2-103">SizedADRLIST</span></span>

<span data-ttu-id="dd5a2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd5a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd5a2-105">Define uma estrutura [ADRLIST](adrlist.md) com o nome especificado que contém um número especificado de estruturas [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="dd5a2-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd5a2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dd5a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd5a2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd5a2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dd5a2-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="dd5a2-108">Related structure:</span></span>  <br/> |<span data-ttu-id="dd5a2-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="dd5a2-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="dd5a2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd5a2-110">Parameters</span></span>

<span data-ttu-id="dd5a2-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="dd5a2-111">__centries_</span></span>
  
> <span data-ttu-id="dd5a2-112">Contagem de estruturas **ADRENTRY** a serem incluídos na nova estrutura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="dd5a2-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="dd5a2-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="dd5a2-113">__name_</span></span>
  
> <span data-ttu-id="dd5a2-114">Nome para a nova estrutura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="dd5a2-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dd5a2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd5a2-115">Remarks</span></span>

<span data-ttu-id="dd5a2-116">A macro **SizedADRLIST** permite definir uma lista de destinatários que possui limites explícitos quando os requisitos de tamanho da matriz são conhecidos.</span><span class="sxs-lookup"><span data-stu-id="dd5a2-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="dd5a2-117">O código a seguir mostra como orientar o resultado da macro **SizedADRLIST** para um ponteiro de estrutura **ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="dd5a2-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="dd5a2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd5a2-118">See also</span></span>

- [<span data-ttu-id="dd5a2-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="dd5a2-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="dd5a2-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="dd5a2-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="dd5a2-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="dd5a2-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

