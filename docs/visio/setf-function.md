---
title: Função SETF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Define a fórmula de uma célula.
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772865"
---
# <a name="setf-function"></a>Função SETF

Define a fórmula de uma célula. 
  
## <a name="syntax"></a>Sintaxe

SETF (GETREF (* * *célula* * *), * * *fórmula* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _célula_ <br/> |Obrigatório  <br/> |**String** <br/> |A célula cuja fórmula deve ser definida.  <br/> |
| _formula_ <br/> |Obrigatório  <br/> |**String** <br/> |A fórmula a ser usada.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando avaliada, o resultado da expressão na _fórmula_ torna-se a nova fórmula na _célula_. Se a _fórmula_ está entre aspas, a expressão entre aspas foi escrita para a _célula_. Para definir a _célula_ como uma cadeia de caracteres, coloque a _fórmula_ em três conjuntos de aspas. 
  
A célula de destino deve ser especificada usando-se uma referência GETREF() ou uma cadeia de caracteres para evitar a circularidade. É preferível usar GETREF, porque o Microsoft Visio pode ajustar as referências quando a forma é movida para um documento diferente.
  
Se a _célula_ não for especificado, usando GETREF ou como uma cadeia de caracteres, a função retornará um erro e fórmula da célula não é alterada. Se a _fórmula_ contém um erro de sintaxe, a função retornará um erro e a fórmula na _célula_ não será alterada. 
  
## <a name="example-1"></a>Exemplo 1

SETF (GETREF(Scratch.A1), 1,5 pol \* 6 + 1 pé)
  
Define a fórmula de Scratch.A1 para 21 polegadas.
  
## <a name="example-2"></a>Exemplo 2

SETF (GETREF(Scratch.A1), "1,5 pol \* 6 + 1 pé")
  
Define a fórmula do zero. A1 à expressão 1,5 na\*6 + 1 pé.
  
## <a name="example-3"></a>Exemplo 3

SETF( GETREF(Scratch.A1), """Say """"ahh""""""")
  
Define a fórmula de Scratch.A1 para a sequência de caracteres "Say ""ahh""" que avalia para Say "ahh".
  

