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
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425971"
---
# <a name="setf-function"></a>Função SETF

Define a fórmula de uma célula. 
  
## <a name="syntax"></a>Sintaxe

SETF( GETREF(** *cell* ** ), ** *formula* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cell_ <br/> |Obrigatório  <br/> |**String** <br/> |A célula cuja fórmula definir.  <br/> |
| _formula_ <br/> |Obrigatório  <br/> |**String** <br/> |A fórmula a ser usada.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando avaliado, o resultado da expressão _na_ fórmula se torna a nova fórmula na _célula._ Se _a_ fórmula estiver entre aspas, a expressão entre aspas será escrita na _célula._ Para definir  _a célula_ como uma cadeia de caracteres, coloque a  _fórmula_ em três conjuntos de aspas. 
  
A célula de destino deve ser especificada usando-se uma referência GETREF() ou uma cadeia de caracteres para evitar a circularidade. É preferível usar GETREF, porque o Microsoft Visio pode ajustar as referências quando a forma é movida para um documento diferente.
  
Se  _a_ célula não for especificada usando GETREF ou como uma cadeia de caracteres, a função retornará um erro e nenhuma fórmula da célula será alterada. Se  _a_ fórmula contiver um erro de sintaxe, a função retornará um erro e a fórmula na  _célula_ não será alterada. 
  
## <a name="example-1"></a>Exemplo 1

SETF( GETREF(Scratch.A1), 1,5 in \* 6 + 1 pé)
  
Define a fórmula de Scratch.A1 para 21 polegadas.
  
## <a name="example-2"></a>Exemplo 2

SETF( GETREF(Scratch.A1), "1,5 in \* 6 + 1 pé")
  
Define a fórmula de Scratch. A1 para a expressão 1,5 em \* 6+1 pé.
  
## <a name="example-3"></a>Exemplo 3

SETF( GETREF(Scratch.A1), """Say """"ahh""""""")
  
Define a fórmula de Scratch.A1 para a sequência de caracteres "Say ""ahh""" que avalia para Say "ahh".
  

