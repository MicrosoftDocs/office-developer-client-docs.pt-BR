---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- função xlAutoOpen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310287"
---
# <a name="xlautoopen"></a><span data-ttu-id="9df7a-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="9df7a-104">xlAutoOpen</span></span>

 <span data-ttu-id="9df7a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9df7a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9df7a-106">Função de retorno de chamada que deve ser implementada e exportada por cada XLL válido.</span><span class="sxs-lookup"><span data-stu-id="9df7a-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="9df7a-107">A função **xlAutoOpen** é o local recomendado de onde registrar funções e comandos XLL, inicializar estruturas de dados, personalizar a interface do usuário e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9df7a-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="9df7a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9df7a-108">Parameters</span></span>

<span data-ttu-id="9df7a-109">Essa função não usa argumentos.</span><span class="sxs-lookup"><span data-stu-id="9df7a-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9df7a-110">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9df7a-110">Property value/Return value</span></span>

<span data-ttu-id="9df7a-111">A implementação dessa função deve retornar 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="9df7a-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9df7a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9df7a-112">Remarks</span></span>

<span data-ttu-id="9df7a-113">O Microsoft Excel chama **xlAutoOpen** sempre que o XLL é ativado.</span><span class="sxs-lookup"><span data-stu-id="9df7a-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="9df7a-114">O XLL é ativado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="9df7a-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="9df7a-115">No início de uma sessão do Excel, se ela estiver ativa na última sessão do Excel que terminou normalmente.</span><span class="sxs-lookup"><span data-stu-id="9df7a-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="9df7a-116">Se carregado durante uma sessão do Excel.</span><span class="sxs-lookup"><span data-stu-id="9df7a-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="9df7a-117">Um XLL pode ser carregado de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="9df7a-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="9df7a-118">Escolhendo **abrir** no menu **arquivo** (onde a versão do Excel dá suporte a esse método de carregamento de XLLs).</span><span class="sxs-lookup"><span data-stu-id="9df7a-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="9df7a-119">Usando o Gerenciador de Suplemento.</span><span class="sxs-lookup"><span data-stu-id="9df7a-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="9df7a-120">De outro XLL que chama [xlfRegister](xlfregister-form-1.md) com o nome dessa DLL como o único argumento.</span><span class="sxs-lookup"><span data-stu-id="9df7a-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="9df7a-121">De uma planilha de macro XLM que chama [Register](xlfregister-form-1.md) com o nome dessa DLL como o único argumento.</span><span class="sxs-lookup"><span data-stu-id="9df7a-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="9df7a-122">Se o suplemento for desativado e reativado durante uma sessão do Excel, essa função será chamada na reativação.</span><span class="sxs-lookup"><span data-stu-id="9df7a-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="9df7a-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9df7a-123">Example</span></span>

<span data-ttu-id="9df7a-124">Consulte os arquivos `SAMPLES\EXAMPLE\EXAMPLE.C` e `SAMPLES\GENERIC\GENERIC.C`, e, por exemplo, implementações dessa função.</span><span class="sxs-lookup"><span data-stu-id="9df7a-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9df7a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9df7a-125">See also</span></span>



[<span data-ttu-id="9df7a-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="9df7a-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="9df7a-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="9df7a-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="9df7a-128">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="9df7a-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

