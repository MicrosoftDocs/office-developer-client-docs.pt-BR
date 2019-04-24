---
title: Função THEMERESTORE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Armazena o valor de formatação local de uma forma quando você aplica um tema para que você possa restaurar a formatação local se o usuário remover o tema subsequentemente.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332211"
---
# <a name="themerestore-function"></a>Função THEMERESTORE

Armazena o valor de formatação local de uma forma quando você aplica um tema para que você possa restaurar a formatação local se o usuário remover o tema subsequentemente.
  
## <a name="syntax"></a>Sintaxe

THEMERESTORE ()
  
## <a name="example"></a>Exemplo

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Restaura a formatação da cor de preenchimento local aplicada anteriormente a uma forma quanto o tema atual é removido.
  

