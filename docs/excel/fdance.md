---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- função fdance [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765375"
---
# <a name="fdance"></a><span data-ttu-id="226fc-104">fDance</span><span class="sxs-lookup"><span data-stu-id="226fc-104">fDance</span></span>

 <span data-ttu-id="226fc-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="226fc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="226fc-106">Comando de exemplo definida pelo usuário que altera as células selecionadas na planilha ativa ao redor até que o usuário pressiona **ESC**.</span><span class="sxs-lookup"><span data-stu-id="226fc-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="226fc-107">Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado.</span><span class="sxs-lookup"><span data-stu-id="226fc-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="226fc-108">Par�metros</span><span class="sxs-lookup"><span data-stu-id="226fc-108">Parameters</span></span>

<span data-ttu-id="226fc-109">A função não assumir nenhum parâmetro.</span><span class="sxs-lookup"><span data-stu-id="226fc-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="226fc-110">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="226fc-110">Property value/Return value</span></span>

<span data-ttu-id="226fc-111">A função sempre retornará 1.</span><span class="sxs-lookup"><span data-stu-id="226fc-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="226fc-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="226fc-112">Remarks</span></span>

<span data-ttu-id="226fc-113">Este é um exemplo de uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="226fc-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="226fc-114">Ele chama a função [xlAbort](xlabort.md) ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="226fc-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="226fc-115">Isso produz o processador (ajudando com multitarefa cooperativa) e verifica se o usuário pressiona **ESC** para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="226fc-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="226fc-116">Em caso afirmativo, ele oferece ao usuário uma oportunidade de cancelar a anulação.</span><span class="sxs-lookup"><span data-stu-id="226fc-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="226fc-117">Example</span><span class="sxs-lookup"><span data-stu-id="226fc-117">Example</span></span>

<span data-ttu-id="226fc-118">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="226fc-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="226fc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="226fc-119">See also</span></span>



[<span data-ttu-id="226fc-120">Funções na DLL genérico</span><span class="sxs-lookup"><span data-stu-id="226fc-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

