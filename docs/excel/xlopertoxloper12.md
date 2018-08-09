---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- função xlopertoxloper12 [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765500"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="874b2-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="874b2-104">XLOperToXLOper12</span></span>

<span data-ttu-id="874b2-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="874b2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="874b2-106">Usado para converter do antigo **XLOPER** o novo **XLOPER12**rotina de conversão.</span><span class="sxs-lookup"><span data-stu-id="874b2-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="874b2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="874b2-107">Parameters</span></span>

<span data-ttu-id="874b2-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="874b2-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="874b2-109">Ponteiro para a fonte **XLOPER** a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="874b2-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="874b2-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="874b2-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="874b2-111">Ponteiro para o destino **XLOPER12** contenha o valor convertido.</span><span class="sxs-lookup"><span data-stu-id="874b2-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="874b2-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="874b2-112">Property value/Return value</span></span>

<span data-ttu-id="874b2-113">**TRUE** se a conversão foi bem-sucedida, **FALSE** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="874b2-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="874b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="874b2-114">Remarks</span></span>

<span data-ttu-id="874b2-115">Dependendo do tipo de **XLOPER**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para no destino **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="874b2-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="874b2-116">O chamador é responsável por liberar qualquer memória associada a cópia se a conversão foi bem sucedida; **FreeXLOper12T** pode ser usado, ou pode ser feito diretamente usando **livre**.</span><span class="sxs-lookup"><span data-stu-id="874b2-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="874b2-117">Se a conversão falhar, o chamador não precisará liberar qualquer memória.</span><span class="sxs-lookup"><span data-stu-id="874b2-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="874b2-118">Em geral, a conversão de qualquer **XLOPER** em **XLOPER12** é possível.</span><span class="sxs-lookup"><span data-stu-id="874b2-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="874b2-119">Por outro lado, a conversão de **XLOPER12** em **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência é muito grande ou uma cadeia de caracteres que é muito longa para **XLOPER** conter.</span><span class="sxs-lookup"><span data-stu-id="874b2-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="874b2-120">**XLOPER** Cadeias de caracteres de byte ASCII são convertidas em cadeias de caracteres Unicode **XLOPER12** caractere largo de forma que depende da localidade.</span><span class="sxs-lookup"><span data-stu-id="874b2-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="874b2-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="874b2-121">Example</span></span>

<span data-ttu-id="874b2-122">Consulte o arquivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para o código para essa função.</span><span class="sxs-lookup"><span data-stu-id="874b2-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

