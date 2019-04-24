---
title: Função EVALCELL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Obtém uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional). Retorna o resultado calculado da função personalizada, dado os argumentos e valores especificados.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329068"
---
# <a name="evalcell-function"></a>Função EVALCELL

Obtém uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional). Retorna o resultado calculado da função personalizada, dado os argumentos e valores especificados.
  
## <a name="syntax"></a>Sintaxe

EVALCELL (* * *cellRef* * *, [* * *arg1name, arg1* * *], [* * *arg2Name, arg2* * *],...) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |Obrigatório  <br/> |**String** <br/> |A referência à célula que contém a função personalizada. Referências cruzadas são permitidas.  <br/> |
| _arg1name_ <br/> |Opcional  <br/> |**String** <br/> |O nome do primeiro argumento a ser passado para a função personalizada. Espaços são permitidos.  <br/> |
| _arg1_ <br/> |Opcional  <br/> |**Vai** <br/> |O valor do parâmetro _arg1_ .  <br/> |
| _arg2Name_ <br/> |Opcional  <br/> |**String** <br/> |O nome do segundo argumento a ser passado para a função personalizada. Espaços são permitidos.  <br/> |
| _arg2_ <br/> |Opcional  <br/> |**Vai** <br/> |O valor do parâmetro _arg2_ .  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

A célula de chamada não deve especificar cada argumento usado pela função personalizada. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a função EVALCELL em conjunto com a função ARG para encontrar o valor intermediários de um conjunto de três valores. 
  
Na célula de expressão, coloque o código a seguir, que define a função personalizada: 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

Nas células de chamada, coloque o código a seguir, que chama a função personalizada:
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


