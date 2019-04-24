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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328004"
---
# <a name="ftaddft"></a><span data-ttu-id="30752-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="30752-103">FtAddFt</span></span>

  
  
<span data-ttu-id="30752-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30752-105">Adiciona um inteiro de 64 bits não assinado a outro.</span><span class="sxs-lookup"><span data-stu-id="30752-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30752-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="30752-106">Header file:</span></span>  <br/> |<span data-ttu-id="30752-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="30752-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="30752-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="30752-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="30752-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="30752-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="30752-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="30752-110">Called by:</span></span>  <br/> |<span data-ttu-id="30752-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="30752-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="30752-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30752-112">Parameters</span></span>

 <span data-ttu-id="30752-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="30752-113">_Addend1_</span></span>
  
> <span data-ttu-id="30752-114">no Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro de 64 bits não assinado a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="30752-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="30752-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="30752-115">_Addend2_</span></span>
  
> <span data-ttu-id="30752-116">no Uma estrutura **FILETIME** que contém o segundo inteiro não assinado de 64 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="30752-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="30752-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="30752-117">Return value</span></span>

<span data-ttu-id="30752-118">A função **FtAddFt** retorna uma estrutura **FILETIME** que contém a soma dos dois inteiros.</span><span class="sxs-lookup"><span data-stu-id="30752-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="30752-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="30752-119">The two input parameters remain unchanged.</span></span> 
  

