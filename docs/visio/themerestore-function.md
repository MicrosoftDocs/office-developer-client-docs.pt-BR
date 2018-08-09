---
title: Função THEMERESTORE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Armazena o valor de formatação local de uma forma quando você aplica um tema para que você possa restaurar a formatação local se o usuário subsequentemente remove o tema.
ms.openlocfilehash: f22f603cad1d310adc59d19e9b3e3882bd797fce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773147"
---
# <a name="themerestore-function"></a><span data-ttu-id="205b8-103">Função THEMERESTORE</span><span class="sxs-lookup"><span data-stu-id="205b8-103">THEMERESTORE Function</span></span>

<span data-ttu-id="205b8-104">Armazena o valor de formatação local de uma forma quando você aplica um tema para que você possa restaurar a formatação local se o usuário subsequentemente remove o tema.</span><span class="sxs-lookup"><span data-stu-id="205b8-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="205b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="205b8-105">Syntax</span></span>

<span data-ttu-id="205b8-106">THEMERESTORE()</span><span class="sxs-lookup"><span data-stu-id="205b8-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="205b8-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="205b8-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="205b8-108">Restaura a formatação da cor de preenchimento local aplicada anteriormente a uma forma quanto o tema atual é removido.</span><span class="sxs-lookup"><span data-stu-id="205b8-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

