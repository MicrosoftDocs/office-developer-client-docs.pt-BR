---
title: Função ROUND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Rodadas de um número para a precisão representada por numberofdigits .
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439965"
---
# <a name="round-function-visioshapesheet"></a>Função ROUND (VisioShapeSheet)

Rodadas de um número para a precisão representada por  *numberofdigits*  . 
  
## <a name="syntax"></a>Sintaxe

ROUND(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _numberofdigits_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de casas decimais de precisão.  <br/> |
   
## <a name="remarks"></a>Comentários

Se  _numberofdigits_ for maior que 0,  _o_ número será arredondado pelo  _número dedigits_ à direita do decimal. Se  _numberofdigits_ for 0,  _núm_ será arredondado para um inteiro. Se  _numberofdigits_ for menor que 0,  _o_ número será arredondado pelo  _número dedigits_ à esquerda do decimal. 
  
## <a name="example-1"></a>Exemplo 1

ROUND(123,654,2)
  
Retornará 123,65.
  
## <a name="example-2"></a>Exemplo 2

ROUND(123,654,0)
  
Retornará 124.
  
## <a name="example-3"></a>Exemplo 3

ROUND(123,654,-1)
  
Retornará 120.
  

