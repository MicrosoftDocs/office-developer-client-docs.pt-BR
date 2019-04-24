---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345742"
---
# <a name="szfindsz"></a><span data-ttu-id="e7b95-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="e7b95-103">SzFindSz</span></span>

  
  
<span data-ttu-id="e7b95-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7b95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7b95-105">Localiza a primeira ocorrência de uma subcadeia de caracteres terminada em nulo em uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="e7b95-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7b95-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e7b95-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7b95-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e7b95-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7b95-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e7b95-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7b95-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7b95-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7b95-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e7b95-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7b95-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="e7b95-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="e7b95-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7b95-112">Parameters</span></span>

 <span data-ttu-id="e7b95-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e7b95-113">_lpsz_</span></span>
  
> <span data-ttu-id="e7b95-114">no Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="e7b95-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="e7b95-115">O parâmetro _lpsz_ não deve exceder 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7b95-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="e7b95-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="e7b95-116">_lpszKey_</span></span>
  
> <span data-ttu-id="e7b95-117">no Ponteiro para a subcadeia de caracteres terminada em nulo a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="e7b95-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="e7b95-118">O parâmetro _lpszKey_ não deve exceder 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7b95-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7b95-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e7b95-119">Return value</span></span>

 <span data-ttu-id="e7b95-120">**SzFindSz** retorna um ponteiro para o primeiro caractere da primeira ocorrência da subcadeia de caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7b95-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="e7b95-121">Se a subcadeia de caracteres não ocorrer em qualquer lugar na cadeia de caracteres, se _lpszKey_ for maior do que _lpsz_, ou se um dos parâmetros for NULL, um valor NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="e7b95-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e7b95-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7b95-122">Remarks</span></span>

<span data-ttu-id="e7b95-123">A função **SzFindSz** pesquisa apenas uma correspondência exata; é sensível às diferenças de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e7b95-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="e7b95-124">Pesquisas em formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="e7b95-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="e7b95-125">O limite de tamanho em ambos os parâmetros é em caracteres, não necessariamente em bytes.</span><span class="sxs-lookup"><span data-stu-id="e7b95-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

