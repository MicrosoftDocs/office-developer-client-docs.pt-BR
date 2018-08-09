---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770418"
---
# <a name="sizedentryid"></a><span data-ttu-id="caa6f-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="caa6f-103">SizedENTRYID</span></span>

<span data-ttu-id="caa6f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="caa6f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="caa6f-105">Cria uma estrutura [ENTRYID](entryid.md) nomeada que contém um membro **ab** de um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="caa6f-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="caa6f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="caa6f-106">Header file:</span></span>  <br/> |<span data-ttu-id="caa6f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="caa6f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="caa6f-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="caa6f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="caa6f-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="caa6f-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="caa6f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caa6f-110">Parameters</span></span>

<span data-ttu-id="caa6f-111">__cb_</span><span class="sxs-lookup"><span data-stu-id="caa6f-111">__cb_</span></span>
  
> <span data-ttu-id="caa6f-112">Contagem de bytes no membro **ab** da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="caa6f-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="caa6f-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="caa6f-113">__name_</span></span>
  
> <span data-ttu-id="caa6f-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="caa6f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="caa6f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="caa6f-115">Remarks</span></span>

<span data-ttu-id="caa6f-116">A macro **SizedENTRYID** permite definir um identificador de entrada após os requisitos de tamanho da matriz são conhecidos.</span><span class="sxs-lookup"><span data-stu-id="caa6f-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="caa6f-117">Use essa macro para criar um identificador de entrada com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="caa6f-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="caa6f-118">Para usar a nova estrutura que é resultado da macro **SizedENTRYID** como um ponteiro para uma estrutura **ENTRYID** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="caa6f-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="caa6f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="caa6f-119">See also</span></span>

- [<span data-ttu-id="caa6f-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="caa6f-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="caa6f-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="caa6f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

