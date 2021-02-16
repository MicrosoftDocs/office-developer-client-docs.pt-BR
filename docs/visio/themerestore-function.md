---
title: Função THEMERESTORE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Armazena o valor de formatação local de uma forma quando você aplica um tema para que você possa restaurar a formatação local se o usuário remover subsequentemente o tema.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404285"
---
# <a name="themerestore-function"></a><span data-ttu-id="baa61-103">Função THEMERESTORE</span><span class="sxs-lookup"><span data-stu-id="baa61-103">THEMERESTORE Function</span></span>

<span data-ttu-id="baa61-104">Armazena o valor de formatação local de uma forma quando você aplica um tema para que você possa restaurar a formatação local se o usuário remover subsequentemente o tema.</span><span class="sxs-lookup"><span data-stu-id="baa61-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="baa61-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baa61-105">Syntax</span></span>

<span data-ttu-id="baa61-106">THEMERESTORE()</span><span class="sxs-lookup"><span data-stu-id="baa61-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="baa61-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="baa61-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="baa61-108">Restaura a formatação da cor de preenchimento local aplicada anteriormente a uma forma quanto o tema atual é removido.</span><span class="sxs-lookup"><span data-stu-id="baa61-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

