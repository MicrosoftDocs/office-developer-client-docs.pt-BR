---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- Função xloperoper12 [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404593"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="5b95d-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="5b95d-104">XLOperToXLOper12</span></span>

<span data-ttu-id="5b95d-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5b95d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5b95d-106">Rotina de conversão usada para converter do **XLOPER antigo** para o novo **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="5b95d-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="5b95d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b95d-107">Parameters</span></span>

<span data-ttu-id="5b95d-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="5b95d-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="5b95d-109">Ponteiro para o **XLOPER de origem** a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="5b95d-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="5b95d-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="5b95d-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="5b95d-111">Ponteiro para o **XLOPER12 de destino** para conter o valor convertido.</span><span class="sxs-lookup"><span data-stu-id="5b95d-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5b95d-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5b95d-112">Property value/Return value</span></span>

<span data-ttu-id="5b95d-113">**TRUE** se a conversão foi bem-sucedida; caso contrário, **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="5b95d-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5b95d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b95d-114">Remarks</span></span>

<span data-ttu-id="5b95d-115">Dependendo do tipo de **XLOPER**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para o **XLOPER12 de destino.**</span><span class="sxs-lookup"><span data-stu-id="5b95d-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="5b95d-116">O chamador é responsável por liberar qualquer memória associada à cópia se a conversão for um sucesso; **FreeXLOper12T** pode ser usado ou pode ser feito diretamente usando **gratuitamente.**</span><span class="sxs-lookup"><span data-stu-id="5b95d-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="5b95d-117">Se a conversão falhar, o chamador não precisará liberar memória.</span><span class="sxs-lookup"><span data-stu-id="5b95d-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="5b95d-118">Em geral, a conversão de qualquer **XLOPER** para um **XLOPER12** é possível.</span><span class="sxs-lookup"><span data-stu-id="5b95d-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="5b95d-119">Por outro lado, a conversão de um **XLOPER12** para um **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência muito grande ou uma cadeia de caracteres muito longa para o **XLOPER** conter.</span><span class="sxs-lookup"><span data-stu-id="5b95d-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="5b95d-120">**XLOPER** As cadeias de caracteres de byte ASCII são convertidas em cadeias de caracteres largos Unicode **XLOPER12** de uma forma dependente de localidade.</span><span class="sxs-lookup"><span data-stu-id="5b95d-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="5b95d-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5b95d-121">Example</span></span>

<span data-ttu-id="5b95d-122">Consulte o arquivo  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para o código para esta função.</span><span class="sxs-lookup"><span data-stu-id="5b95d-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

