---
title: Função THEMEGUARD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protege as células de formatação de uma forma para garantir que eles usem os aspectos apropriados do tema atual.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404943"
---
# <a name="themeguard-function"></a>Função THEMEGUARD

Protege as células de formatação de uma forma para garantir que eles usem os aspectos apropriados do tema atual.
  
## <a name="syntax"></a>Sintaxe

THEMEGUARD()
  
## <a name="remarks"></a>Comentários

A aplicação da função THEMEGUARD a uma célula não a protege contra formatação manual, quando comparada à função GUARD. Se você aplicar formatação à forma na interface do usuário ou programaticamente, por meio de Automação, a fórmula THEMEGUARD será substituído, a menos que você inclua a função SETATREFEXPR na fórmula para armazenar o valor de formatação manual. 
  
## <a name="example"></a>Exemplo

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Especifica que a forma aceita a cor Ênfase 2 do tema atual, em vez da cor de preenchimento do tema principal.
  

