---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345133"
---
# <a name="szfindlastch"></a><span data-ttu-id="da5f1-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="da5f1-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="da5f1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da5f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da5f1-105">Procura a última ocorrência de um caractere em uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="da5f1-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da5f1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="da5f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="da5f1-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="da5f1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="da5f1-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="da5f1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="da5f1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="da5f1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="da5f1-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="da5f1-110">Called by:</span></span>  <br/> |<span data-ttu-id="da5f1-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="da5f1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="da5f1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da5f1-112">Parameters</span></span>

 <span data-ttu-id="da5f1-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="da5f1-113">_lpsz_</span></span>
  
> <span data-ttu-id="da5f1-114">no Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="da5f1-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="da5f1-115">_CA_</span><span class="sxs-lookup"><span data-stu-id="da5f1-115">_ch_</span></span>
  
> <span data-ttu-id="da5f1-116">no O caractere a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="da5f1-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da5f1-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="da5f1-117">Return value</span></span>

 <span data-ttu-id="da5f1-118">**SzFindLastCh** retorna um ponteiro para a última ocorrência do caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="da5f1-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="da5f1-119">Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres ou se o parâmetro _lpsz_ for NULL, um valor NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="da5f1-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="da5f1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="da5f1-120">Remarks</span></span>

<span data-ttu-id="da5f1-121">A função **SzFindLastCh** pesquisa apenas uma correspondência exata; é sensível às diferenças de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="da5f1-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="da5f1-122">As pesquisas nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="da5f1-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

