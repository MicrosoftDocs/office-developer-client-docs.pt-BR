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
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405706"
---
# <a name="sizedentryid"></a><span data-ttu-id="95654-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="95654-103">SizedENTRYID</span></span>

<span data-ttu-id="95654-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95654-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95654-105">Cria uma estrutura [EntryID](entryid.md) nomeada que contém um membro **AB** de um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="95654-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95654-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="95654-106">Header file:</span></span>  <br/> |<span data-ttu-id="95654-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="95654-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="95654-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="95654-108">Related structure:</span></span>  <br/> |<span data-ttu-id="95654-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="95654-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="95654-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95654-110">Parameters</span></span>

<span data-ttu-id="95654-111">__CB_</span><span class="sxs-lookup"><span data-stu-id="95654-111">__cb_</span></span>
  
> <span data-ttu-id="95654-112">Contagem de bytes no membro **AB** da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="95654-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="95654-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="95654-113">__name_</span></span>
  
> <span data-ttu-id="95654-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="95654-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95654-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="95654-115">Remarks</span></span>

<span data-ttu-id="95654-116">A macro **SizedENTRYID** permite que você defina um identificador de entrada após os requisitos de comprimento de matriz serem conhecidos.</span><span class="sxs-lookup"><span data-stu-id="95654-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="95654-117">Use essa macro para criar um identificador de entrada com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="95654-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="95654-118">Para usar a nova estrutura que resulta da macro **SizedENTRYID** como um ponteiro para uma estrutura **EntryID** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="95654-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="95654-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="95654-119">See also</span></span>

- [<span data-ttu-id="95654-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="95654-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="95654-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="95654-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

