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
# <a name="szfindch"></a><span data-ttu-id="25a14-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="25a14-103">SzFindCh</span></span>
 
<span data-ttu-id="25a14-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25a14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25a14-105">Procura a primeira ocorrência de um caractere em uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="25a14-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25a14-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="25a14-106">Header file:</span></span>  <br/> |<span data-ttu-id="25a14-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="25a14-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="25a14-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="25a14-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="25a14-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="25a14-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="25a14-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="25a14-110">Called by:</span></span>  <br/> |<span data-ttu-id="25a14-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="25a14-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="25a14-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25a14-112">Parameters</span></span>

<span data-ttu-id="25a14-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="25a14-113">_lpsz_</span></span>
  
> <span data-ttu-id="25a14-114">no Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="25a14-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="25a14-115">_CA_</span><span class="sxs-lookup"><span data-stu-id="25a14-115">_ch_</span></span>
  
> <span data-ttu-id="25a14-116">no O caractere a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="25a14-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25a14-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="25a14-117">Return value</span></span>

<span data-ttu-id="25a14-118">**SzFindCh** retorna um ponteiro para a primeira ocorrência do caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="25a14-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="25a14-119">Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres ou se o parâmetro _lpsz_ for NULL, um valor NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="25a14-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25a14-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="25a14-120">Remarks</span></span>

<span data-ttu-id="25a14-121">A função **SzFindCh** pesquisa apenas uma correspondência exata; é sensível às diferenças de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="25a14-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="25a14-122">As pesquisas nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="25a14-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

