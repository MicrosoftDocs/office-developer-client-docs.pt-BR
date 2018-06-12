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
# <a name="themeguard-function"></a>Função THEMEGUARD

Protege as células de formatação de uma forma para garantir que eles usem os aspectos apropriados do tema atual.
  
## <a name="syntax"></a>Sintaxe

THEMEGUARD()
  
## <a name="remarks"></a>Comentários

Aplicando a função THEMEGUARD a uma célula não protege contra a formatação manual da mesma maneira que aplicando o protetor de função faz. Se você aplicar formatação à forma na interface do usuário ou programaticamente, por meio da automação, a fórmula THEMEGUARD é substituída, a menos que você inclua a função SETATREFEXPR na fórmula para armazenar o valor de formatação de manual. 
  
## <a name="example"></a>Example

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Especifica que a forma aceita a cor Ênfase 2 do tema atual, em vez da cor de preenchimento do tema principal.
  

