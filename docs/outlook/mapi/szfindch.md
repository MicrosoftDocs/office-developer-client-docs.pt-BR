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
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421939"
---
# <a name="szfindch"></a><span data-ttu-id="90e64-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="90e64-103">SzFindCh</span></span>
 
<span data-ttu-id="90e64-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90e64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90e64-105">Procura a primeira ocorrência de um caractere em uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="90e64-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90e64-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="90e64-106">Header file:</span></span>  <br/> |<span data-ttu-id="90e64-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90e64-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="90e64-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="90e64-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="90e64-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="90e64-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="90e64-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="90e64-110">Called by:</span></span>  <br/> |<span data-ttu-id="90e64-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="90e64-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="90e64-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90e64-112">Parameters</span></span>

<span data-ttu-id="90e64-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="90e64-113">_lpsz_</span></span>
  
> <span data-ttu-id="90e64-114">[in] Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="90e64-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="90e64-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="90e64-115">_ch_</span></span>
  
> <span data-ttu-id="90e64-116">[in] O caractere a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="90e64-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90e64-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="90e64-117">Return value</span></span>

<span data-ttu-id="90e64-118">**SzFindCh** retorna um ponteiro para a primeira ocorrência do caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="90e64-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="90e64-119">Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres ou se o parâmetro  _lpsz_ for NULL, um valor null será retornado.</span><span class="sxs-lookup"><span data-stu-id="90e64-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90e64-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="90e64-120">Remarks</span></span>

<span data-ttu-id="90e64-121">A **função SzFindCh** procura apenas uma combinação exata; é sensível a diferenças de caso e diacrítico.</span><span class="sxs-lookup"><span data-stu-id="90e64-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="90e64-122">Há suporte para pesquisas nos formatos Unicode e DBCS.</span><span class="sxs-lookup"><span data-stu-id="90e64-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

