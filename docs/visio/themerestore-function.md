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
# <a name="themerestore-function"></a>Função THEMERESTORE

Armazena o valor de formatação local de uma forma quando você aplica um tema para que você possa restaurar a formatação local se o usuário subsequentemente remove o tema.
  
## <a name="syntax"></a>Sintaxe

THEMERESTORE()
  
## <a name="example"></a>Exemplo

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Restaura a formatação da cor de preenchimento local aplicada anteriormente a uma forma quanto o tema atual é removido.
  

