---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- Função xloper12esloper [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422905"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="317f0-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="317f0-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="317f0-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="317f0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="317f0-106">Rotina de conversão usada para converter do novo **XLOPER12 para** o **XLOPER antigo.**</span><span class="sxs-lookup"><span data-stu-id="317f0-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="317f0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="317f0-107">Parameters</span></span>

<span data-ttu-id="317f0-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="317f0-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="317f0-109">Ponteiro para o **XLOPER12** de origem a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="317f0-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="317f0-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="317f0-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="317f0-111">Ponteiro para o **XLOPER de destino** para conter o valor convertido.</span><span class="sxs-lookup"><span data-stu-id="317f0-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="317f0-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="317f0-112">Property value/Return value</span></span>

<span data-ttu-id="317f0-113">**TRUE** se a conversão foi bem-sucedida; caso contrário, **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="317f0-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="317f0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="317f0-114">Remarks</span></span>

<span data-ttu-id="317f0-115">Dependendo do tipo de **XLOPER12**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para o **XLOPER de** destino.</span><span class="sxs-lookup"><span data-stu-id="317f0-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="317f0-116">O chamador é responsável por liberar qualquer memória associada à cópia se a conversão for bem-sucedida; **FreeXLOperT** pode ser usado ou pode ser feito diretamente usando **gratuitamente.**</span><span class="sxs-lookup"><span data-stu-id="317f0-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="317f0-117">Se a conversão falhar, o chamador não precisará liberar memória.</span><span class="sxs-lookup"><span data-stu-id="317f0-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="317f0-118">A conversão de um **XLOPER12** para um **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência muito grande ou uma cadeia de caracteres muito longa para o **XLOPER** conter.</span><span class="sxs-lookup"><span data-stu-id="317f0-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="317f0-119">**XLOPER12** Cadeias de caracteres largos Unicode são convertidas em cadeias de caracteres de byte ASCII **XLOPER** de uma maneira dependente da localidade.</span><span class="sxs-lookup"><span data-stu-id="317f0-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="317f0-120">**XlOPER12** **xltypeInt** é um inteiro assinado de 32 bits, enquanto **XLOPER** **xltypeInt** é um inteiro assinado de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="317f0-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="317f0-121">Quando um inteiro **XLOPER12** fornecido excede o limite de um inteiro **XLOPER,** o inteiro é convertido em um duplo de 8 byte e retornado em um **XLOPER** do tipo **xltypeNum**.</span><span class="sxs-lookup"><span data-stu-id="317f0-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="317f0-122">Este é o único caso em que essa função altera o tipo do **XLOPER convertido.**</span><span class="sxs-lookup"><span data-stu-id="317f0-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="317f0-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="317f0-123">Example</span></span>

<span data-ttu-id="317f0-124">Consulte o arquivo  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para o código para esta função.</span><span class="sxs-lookup"><span data-stu-id="317f0-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="317f0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="317f0-125">See also</span></span>

- [<span data-ttu-id="317f0-126">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="317f0-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

