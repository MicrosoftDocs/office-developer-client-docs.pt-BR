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
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439034"
---
# <a name="blue-function"></a>Função BLUE

Retorna o componente azul de uma cor. O valor de retorno é um inteiro no intervalo de 0 a 255, inclusive. A função retornará 0 para uma entrada inválida.
  
## <a name="syntax"></a>Sintaxe

Expressão BLUE(**  ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> |Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="example-1"></a>Exemplo 1

BLUE(Sheet.4! FillForegnd)
  
Retornará o componente azul da cor de primeiro plano do preenchimento de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

BLUE(13)
  
Retornará 128 se o documento utilizar a paleta de cores padrão do Visio, sendo ciano a cor do índice 13.
  
## <a name="example-3"></a>Exemplo 3

BLUE(RGB(10, 20, 30))
  
Retornará 30.
  

