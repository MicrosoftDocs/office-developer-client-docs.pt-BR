---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- função fdance [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409045"
---
# <a name="fdance"></a><span data-ttu-id="fc0b6-104">fDance</span><span class="sxs-lookup"><span data-stu-id="fc0b6-104">fDance</span></span>

 <span data-ttu-id="fc0b6-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fc0b6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fc0b6-106">Exemplo de comando definido pelo usuário que altera as células selecionadas na planilha ativa até o usuário pressionar **ESC**.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="fc0b6-107">Quando GENERIC. XLL é carregado, ele cria um menu definido pelo usuário, genérico, através do qual este comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="fc0b6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc0b6-108">Parameters</span></span>

<span data-ttu-id="fc0b6-109">A função não utiliza parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fc0b6-110">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fc0b6-110">Property value/Return value</span></span>

<span data-ttu-id="fc0b6-111">A função sempre retorna 1.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc0b6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc0b6-112">Remarks</span></span>

<span data-ttu-id="fc0b6-113">Este é um exemplo de operação extensa.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="fc0b6-114">Ele chama a função [xlAbort](xlabort.md) ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="fc0b6-115">Isso gera o processador (ajuda com multitarefa cooperativa) e verifica se o usuário pressionou **ESC** para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="fc0b6-116">Em caso afirmativo, ele oferece ao usuário a oportunidade de cancelar a anulação.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="fc0b6-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fc0b6-117">Example</span></span>

<span data-ttu-id="fc0b6-118">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="fc0b6-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc0b6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc0b6-119">See also</span></span>



[<span data-ttu-id="fc0b6-120">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="fc0b6-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

