---
title: Função GREEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Retorna o componente verde de uma cor.
ms.openlocfilehash: 04bdadc0fa34dc4f51061d428b9366a433b669a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772010"
---
# <a name="green-function"></a>Função GREEN

Retorna o componente verde de uma cor.
  
## <a name="syntax"></a>Sintaxe

VERDE (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**Varia** <br/> |Um índice de uma cor na tabela de cores do documento, uma expressão que resolve para uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um resultado de cor ou o índice de cores.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

O valor de retorno é um número no intervalo de 0 a 255, inclusive, ou uma referência de célula que resulta em um índice. Se a *expressão* for inválido, ele retornará 0 (preto). 
  
## <a name="example-1"></a>Exemplo 1

VERDE (Sheet.4! FillForegnd)
  
Retornará o componente verde da cor de primeiro plano do preenchimento de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

GREEN(11)
  
Retornará 128 se o documento utilizar a paleta de cores padrão do Visio, sendo amarelo escuro a cor do índice 11.
  
## <a name="example-3"></a>Exemplo 3

GREEN(RGB(10, 20, 30))
  
Retornará 20.
  

