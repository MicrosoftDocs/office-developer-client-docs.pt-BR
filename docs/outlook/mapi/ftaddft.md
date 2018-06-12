---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766635"
---
# <a name="ftaddft"></a><span data-ttu-id="c3e12-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="c3e12-103">FtAddFt</span></span>

  
  
<span data-ttu-id="c3e12-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3e12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3e12-105">Adiciona um inteiro não assinado de 64 bits para outro.</span><span class="sxs-lookup"><span data-stu-id="c3e12-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3e12-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c3e12-106">Header file:</span></span>  <br/> |<span data-ttu-id="c3e12-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c3e12-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c3e12-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="c3e12-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c3e12-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c3e12-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c3e12-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="c3e12-110">Called by:</span></span>  <br/> |<span data-ttu-id="c3e12-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c3e12-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="c3e12-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c3e12-112">Parameters</span></span>

 <span data-ttu-id="c3e12-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="c3e12-113">_Addend1_</span></span>
  
> <span data-ttu-id="c3e12-114">[in] Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro não assinado de 64 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="c3e12-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="c3e12-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="c3e12-115">_Addend2_</span></span>
  
> <span data-ttu-id="c3e12-116">[in] Uma estrutura **FILETIME** que contém o segundo inteiro não assinado de 64 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="c3e12-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c3e12-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c3e12-117">Return value</span></span>

<span data-ttu-id="c3e12-118">A função **FtAddFt** retorna uma estrutura **FILETIME** que contém a soma dos dois valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="c3e12-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="c3e12-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="c3e12-119">The two input parameters remain unchanged.</span></span> 
  

