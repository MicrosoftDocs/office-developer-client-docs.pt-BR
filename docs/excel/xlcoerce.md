---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- função xlCoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424830"
---
# <a name="xlcoerce"></a><span data-ttu-id="2aa63-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="2aa63-104">xlCoerce</span></span>

 <span data-ttu-id="2aa63-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2aa63-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2aa63-106">Converte um tipo de **XLOPER**/ **XLOPER12** para outro ou procura valores de célula em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="2aa63-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="2aa63-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2aa63-107">Parameters</span></span>

 <span data-ttu-id="2aa63-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="2aa63-108">_pxSource_</span></span>
  
<span data-ttu-id="2aa63-109">O **XLOPER**/ de origem do**XLOPER12** que precisa ser convertido.</span><span class="sxs-lookup"><span data-stu-id="2aa63-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="2aa63-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="2aa63-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="2aa63-111">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="2aa63-111">(Optional).</span></span> <span data-ttu-id="2aa63-112">Uma máscara de bits dos tipos resultantes que você está disposto a aceitar.</span><span class="sxs-lookup"><span data-stu-id="2aa63-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="2aa63-113">Você deve usar o operador **ou** o operador (|) para especificar vários tipos possíveis.</span><span class="sxs-lookup"><span data-stu-id="2aa63-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="2aa63-114">Se esse argumento for omitido, referências a células únicas serão convertidas em um dos tipos de valor **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (se a célula referida estiver vazia) e referências aos blocos de células são convertidos em **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="2aa63-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="2aa63-115">Isso torna o **xlCoerce** a maneira mais conveniente de procurar valores de célula.</span><span class="sxs-lookup"><span data-stu-id="2aa63-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2aa63-116">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2aa63-116">Property value/Return value</span></span>

<span data-ttu-id="2aa63-117">Retorna o valor forçado (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**ou **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="2aa63-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2aa63-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aa63-118">Remarks</span></span>

 <span data-ttu-id="2aa63-119">**xlCoerce** não pode converter para ou de **xltypeBigData** ou **xltypeFlow**.</span><span class="sxs-lookup"><span data-stu-id="2aa63-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="2aa63-120">Passar um tipo **xltypeMissing** ou **xltypeNil** como _pxDestType_ equivale a omitir o argumento.</span><span class="sxs-lookup"><span data-stu-id="2aa63-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="2aa63-121">A conversão pode falhar em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="2aa63-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="2aa63-122">Por exemplo, algumas cadeias de caracteres não podem ser convertidas em números, enquanto outras podem.</span><span class="sxs-lookup"><span data-stu-id="2aa63-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="2aa63-123">Se uma matriz ou uma referência de várias células for convertida para um tipo de valor único, o resultado será o valor da célula superior esquerda ou do elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="2aa63-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="2aa63-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2aa63-124">Example</span></span>

<span data-ttu-id="2aa63-125">O código a seguir pode ser encontrado `\SAMPLES\EXAMPLE\EXAMPLE.C`em.</span><span class="sxs-lookup"><span data-stu-id="2aa63-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2aa63-126">A função **xlcAlert** implicitamente tenta converter seu argumento em uma cadeia de caracteres para que a etapa de coerção mostrada aqui possa ser removida, e **xInt** possa ser passado diretamente para o **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="2aa63-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="2aa63-127">Como o **xlcAlert** é uma macro de comando, esse código só funciona corretamente quando chamado a partir de uma folha de macro.</span><span class="sxs-lookup"><span data-stu-id="2aa63-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2aa63-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2aa63-128">See also</span></span>



[<span data-ttu-id="2aa63-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="2aa63-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="2aa63-130">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="2aa63-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

