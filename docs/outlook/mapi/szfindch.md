---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770566"
---
# <a name="szfindch"></a><span data-ttu-id="28d73-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="28d73-103">SzFindCh</span></span>
 
<span data-ttu-id="28d73-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28d73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28d73-105">Localiza a primeira ocorrência de um caractere em uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="28d73-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28d73-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="28d73-106">Header file:</span></span>  <br/> |<span data-ttu-id="28d73-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28d73-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="28d73-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="28d73-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="28d73-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="28d73-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="28d73-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="28d73-110">Called by:</span></span>  <br/> |<span data-ttu-id="28d73-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="28d73-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="28d73-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28d73-112">Parameters</span></span>

<span data-ttu-id="28d73-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="28d73-113">_lpsz_</span></span>
  
> <span data-ttu-id="28d73-114">[in] Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="28d73-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="28d73-115">_CH_</span><span class="sxs-lookup"><span data-stu-id="28d73-115">_ch_</span></span>
  
> <span data-ttu-id="28d73-116">[in] O caractere a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="28d73-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="28d73-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="28d73-117">Return value</span></span>

<span data-ttu-id="28d73-118">**SzFindCh** retorna um ponteiro para a primeira ocorrência do caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="28d73-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="28d73-119">Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres, ou se o parâmetro _lpsz_ é NULL, um valor NULL é retornado.</span><span class="sxs-lookup"><span data-stu-id="28d73-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="28d73-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="28d73-120">Remarks</span></span>

<span data-ttu-id="28d73-121">A função **SzFindCh** procura apenas; uma correspondência exata é sensível a maiusculas de minúsculas e diacríticos diferenças.</span><span class="sxs-lookup"><span data-stu-id="28d73-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="28d73-122">Pesquisas nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="28d73-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

