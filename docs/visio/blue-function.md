---
title: Função BLUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Retorna o componente azul de uma cor. O valor de retorno é um inteiro no intervalo de 0 a 255, inclusive. A função retornará 0 para uma entrada inválida.
ms.openlocfilehash: 6a86a0ee91054c89f2def95c0e3521508462bdaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771399"
---
# <a name="blue-function"></a>Função BLUE

Retorna o componente azul de uma cor. O valor de retorno é um inteiro no intervalo de 0 a 255, inclusive. A função retornará 0 para uma entrada inválida.
  
## <a name="syntax"></a>Sintaxe

AZUL (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="example-1"></a>Exemplo 1

AZUL (Sheet.4! FillForegnd)
  
Retornará o componente azul da cor de primeiro plano do preenchimento de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

BLUE(13)
  
Retornará 128 se o documento utilizar a paleta de cores padrão do Visio, sendo ciano a cor do índice 13.
  
## <a name="example-3"></a>Exemplo 3

BLUE(RGB(10, 20, 30))
  
Retornará 30.
  

