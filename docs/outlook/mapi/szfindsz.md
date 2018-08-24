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
ms.openlocfilehash: 0075db0a515166c5185657daf3fc6b1e121d6672
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585119"
---
# <a name="szfindsz"></a><span data-ttu-id="4d20a-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="4d20a-103">SzFindSz</span></span>

  
  
<span data-ttu-id="4d20a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d20a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d20a-105">Localiza a primeira ocorrência de uma subcadeia de caracteres terminada em nulo em uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="4d20a-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d20a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4d20a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4d20a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4d20a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4d20a-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4d20a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4d20a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4d20a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4d20a-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4d20a-110">Called by:</span></span>  <br/> |<span data-ttu-id="4d20a-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="4d20a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="4d20a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d20a-112">Parameters</span></span>

 <span data-ttu-id="4d20a-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="4d20a-113">_lpsz_</span></span>
  
> <span data-ttu-id="4d20a-114">[in] Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="4d20a-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="4d20a-115">O parâmetro _lpsz_ não deve exceder 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d20a-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="4d20a-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="4d20a-116">_lpszKey_</span></span>
  
> <span data-ttu-id="4d20a-117">[in] Ponteiro para a subcadeia de caracteres terminada em nulo a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="4d20a-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="4d20a-118">O parâmetro _lpszKey_ não deve exceder 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d20a-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d20a-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4d20a-119">Return value</span></span>

 <span data-ttu-id="4d20a-120">**SzFindSz** retorna um ponteiro para o primeiro caractere da primeira ocorrência da subcadeia de caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d20a-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="4d20a-121">Se a subcadeia de caracteres não ocorrer em qualquer lugar na cadeia de caracteres, se _lpszKey_ for maior do que _lpsz_, ou se o parâmetro for NULL, um valor NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="4d20a-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4d20a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d20a-122">Remarks</span></span>

<span data-ttu-id="4d20a-123">A função **SzFindSz** procura apenas; uma correspondência exata é sensível a maiusculas de minúsculas e diacríticos diferenças.</span><span class="sxs-lookup"><span data-stu-id="4d20a-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="4d20a-124">Pesquisas nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="4d20a-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="4d20a-125">O limite de tamanho em ambos os parâmetros é em caracteres, não necessariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="4d20a-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

