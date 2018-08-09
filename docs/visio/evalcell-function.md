---
title: Função EVALCELL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Utiliza uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional). Retorna o resultado calculado da função personalizada dado os argumentos e valores especificados.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771811"
---
# <a name="evalcell-function"></a>Função EVALCELL

Utiliza uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional). Retorna o resultado calculado da função personalizada dado os argumentos e valores especificados.
  
## <a name="syntax"></a>Sintaxe

EVALCELL (* * *cellRef* * *, [* * *arg1Name, arg1* * *], [* * *arg2Name, arg2* * *],...) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência para a célula que contém a função personalizada. Referências entre planilhas são permitidas.  <br/> |
| _arg1Name_ <br/> |Opcional  <br/> |**String** <br/> |O nome do primeiro argumento a ser passado para a função personalizada. Espaços são permitidos.  <br/> |
| _arg1_ <br/> |Opcional  <br/> |**Varia** <br/> |Valor do parâmetro _arg1_ .  <br/> |
| _arg2Name_ <br/> |Opcional  <br/> |**String** <br/> |O nome do segundo argumento a serem passados para a função personalizada. São permitidos espaços.  <br/> |
| _arg2_ <br/> |Opcional  <br/> |**Varia** <br/> |Valor do parâmetro _arg2_ .  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
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


