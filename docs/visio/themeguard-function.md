---
title: Função THEMEGUARD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protege as células de formatação de uma forma para garantir que eles usem os aspectos apropriados do tema atual.
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773134"
---
# <a name="themeguard-function"></a><span data-ttu-id="9393e-103">Função THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="9393e-103">THEMEGUARD Function</span></span>

<span data-ttu-id="9393e-104">Protege as células de formatação de uma forma para garantir que eles usem os aspectos apropriados do tema atual.</span><span class="sxs-lookup"><span data-stu-id="9393e-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9393e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9393e-105">Syntax</span></span>

<span data-ttu-id="9393e-106">THEMEGUARD()</span><span class="sxs-lookup"><span data-stu-id="9393e-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9393e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9393e-107">Remarks</span></span>

<span data-ttu-id="9393e-108">Aplicando a função THEMEGUARD a uma célula não protege contra a formatação manual da mesma maneira que aplicando o protetor de função faz.</span><span class="sxs-lookup"><span data-stu-id="9393e-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="9393e-109">Se você aplicar formatação à forma na interface do usuário ou programaticamente, por meio da automação, a fórmula THEMEGUARD é substituída, a menos que você inclua a função SETATREFEXPR na fórmula para armazenar o valor de formatação de manual.</span><span class="sxs-lookup"><span data-stu-id="9393e-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9393e-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9393e-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="9393e-111">Especifica que a forma aceita a cor Ênfase 2 do tema atual, em vez da cor de preenchimento do tema principal.</span><span class="sxs-lookup"><span data-stu-id="9393e-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

