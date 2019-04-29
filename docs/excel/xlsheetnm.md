---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- função xlsheetnm [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437410"
---
# <a name="xlsheetnm"></a><span data-ttu-id="30ef3-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="30ef3-104">xlSheetNm</span></span>

<span data-ttu-id="30ef3-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30ef3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="30ef3-106">Retorna o nome de uma planilha ou folha de macro de sua ID de folha interna contida em uma referência externa ou o nome da planilha atual se for passada uma referência interna.</span><span class="sxs-lookup"><span data-stu-id="30ef3-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="30ef3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30ef3-107">Parameters</span></span>

<span data-ttu-id="30ef3-108">_pxExtref_ (**xltypeRef** ou **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="30ef3-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="30ef3-109">Uma referência à planilha cujo nome você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="30ef3-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="30ef3-110">Se você estiver passando uma referência externa (**xltypeRef**), ela precisará conter apenas a ID da planilha.</span><span class="sxs-lookup"><span data-stu-id="30ef3-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="30ef3-111">As estruturas de dados que descrevem as células na planilha são ignoradas e não precisam ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="30ef3-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="30ef3-112">Se a ID estiver definida como zero, **xlSheetNm** retornará o nome da planilha atual.</span><span class="sxs-lookup"><span data-stu-id="30ef3-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="30ef3-113">Se você estiver passando uma referência interna (**xltypeSef**), **xlSheetNm** retornará o nome da planilha atual.</span><span class="sxs-lookup"><span data-stu-id="30ef3-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="30ef3-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="30ef3-114">Property value/Return value</span></span>

<span data-ttu-id="30ef3-115">Retorna o nome da planilha (**xltypeStr**) no formulário `[Book1]Sheet1`.</span><span class="sxs-lookup"><span data-stu-id="30ef3-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="30ef3-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="30ef3-116">Example</span></span>

<span data-ttu-id="30ef3-117">O exemplo a seguir exibe o nome da planilha a partir da qual a função foi chamada.</span><span class="sxs-lookup"><span data-stu-id="30ef3-117">The following example displays the name of the sheet from which the function was called.</span></span> <span data-ttu-id="30ef3-118">A função funciona corretamente somente se for chamado a partir de uma planilha de macro durante a execução de uma macro de comando XLM.</span><span class="sxs-lookup"><span data-stu-id="30ef3-118">The function works correctly only if called from a macro sheet while executing an XLM command macro.</span></span> <span data-ttu-id="30ef3-119">Isso ocorre porque ele chama **xlcAlert**, que somente os comandos podem fazer, e precisa ser chamado a partir de uma planilha em vez de uma caixa de diálogo, menu ou barra de comandos para que o **xlfCaller** retorne uma referência.</span><span class="sxs-lookup"><span data-stu-id="30ef3-119">This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="30ef3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ef3-120">See also</span></span>

- [<span data-ttu-id="30ef3-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="30ef3-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="30ef3-122">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="30ef3-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

