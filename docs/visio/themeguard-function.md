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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326751"
---
# <a name="themeguard-function"></a>Função THEMEGUARD

Protege as células de formatação de uma forma para garantir que elas usem aspectos apropriados do tema atual.
  
## <a name="syntax"></a>Sintaxe

THEMEGUARD ()
  
## <a name="remarks"></a>Comentários

A aplicação da função THEMEGUARD a uma célula não a protege contra formatação manual, quando comparada à função GUARD. Se você aplicar formatação à forma na interface do usuário ou programaticamente, por meio da automação, a fórmula THEMEGUARD será substituída, a menos que você inclua a função SETATREFEXPR na fórmula para armazenar o valor de formatação manual. 
  
## <a name="example"></a>Exemplo

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Especifica que a forma aceita a cor Ênfase 2 do tema atual, em vez da cor de preenchimento do tema principal.
  

