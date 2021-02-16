---
title: Função ARG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Especifica um argumento que a célula de chamada pode passar para uma função personalizada, bem como o valor padrão retornado pela função personalizada se a célula de chamada não passar um valor para o argumento. Retorna o valor especificado pela célula de chamada e o parâmetro argName correspondente.
ms.openlocfilehash: 3cde7fe55d7bc60d15f32d7ad954443e545af914
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293482"
---
# <a name="arg-function"></a>Função ARG

Especifica um argumento que a célula de chamada pode passar para uma função personalizada, bem como o valor padrão retornado pela função personalizada se a célula de chamada não passar um valor para o argumento. Retorna o valor especificado pela célula de chamada e o parâmetro argName correspondente.
  
## <a name="syntax"></a>Sintaxe

ARG(***argName***,[ ***defaultValue*** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome de um argumento que a célula de chamada pode passar para a função.  <br/> |
| _valor padrão_ <br/> |Opcional  <br/> |**Numérica** <br/> |O valor retornado por ARG se a célula de chamada não passar um valor para o _parâmetro argName._  <br/> |
   
## <a name="remarks"></a>Comentários

Como desenvolvedor de formas, você pode criar funções personalizadas colocando uma expressão em uma célula e chamando essa expressão a partir de uma ou mais células. A expressão pode incluir cadeias de caracteres literais, funções de ShapeSheet e referências de células. A expressão também pode incluir argumentos específicos que são passados pela célula de chamada. 
  
A célula de chamada especifica a célula que contém a função personalizada, bem como qualquer argumento que precise passar para a função. A célula de expressão é avaliada e o resultado retornado para a célula de chamada.
  
## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a função ARG em conjunto com a função EVALCELL para encontrar o valor intermediário de um conjunto de três valores. 
  
Na célula de expressão, coloque o código a seguir, que define a função personalizada: 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

Nas células de chamada, coloque o código a seguir, que chama a função personalizada:
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


