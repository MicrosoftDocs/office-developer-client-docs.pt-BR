---
title: Função THEMEGUARD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protege as células de formatação de uma forma para garantir que elas usem aspectos apropriados do tema atual.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404943"
---
# <a name="themeguard-function"></a><span data-ttu-id="43b36-103">Função THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="43b36-103">THEMEGUARD Function</span></span>

<span data-ttu-id="43b36-104">Protege as células de formatação de uma forma para garantir que elas usem aspectos apropriados do tema atual.</span><span class="sxs-lookup"><span data-stu-id="43b36-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="43b36-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43b36-105">Syntax</span></span>

<span data-ttu-id="43b36-106">THEMEGUARD ()</span><span class="sxs-lookup"><span data-stu-id="43b36-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43b36-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="43b36-107">Remarks</span></span>

<span data-ttu-id="43b36-108">A aplicação da função THEMEGUARD a uma célula não a protege contra formatação manual, quando comparada à função GUARD.</span><span class="sxs-lookup"><span data-stu-id="43b36-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="43b36-109">Se você aplicar formatação à forma na interface do usuário ou programaticamente, por meio da automação, a fórmula THEMEGUARD será substituída, a menos que você inclua a função SETATREFEXPR na fórmula para armazenar o valor de formatação manual.</span><span class="sxs-lookup"><span data-stu-id="43b36-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="43b36-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="43b36-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="43b36-111">Especifica que a forma aceita a cor Ênfase 2 do tema atual, em vez da cor de preenchimento do tema principal.</span><span class="sxs-lookup"><span data-stu-id="43b36-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

