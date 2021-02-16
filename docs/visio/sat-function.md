---
title: Função SAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Retorna o valor do componente de saturação de uma cor.
ms.openlocfilehash: 3b3fd8e13ca9af4f0aea00d2f78c7b5c27be1932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415002"
---
# <a name="sat-function"></a>Função SAT

Retorna o valor do componente de saturação de uma cor. 
  
## <a name="syntax"></a>Sintaxe

Expressão SAT(** *** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obrigatório  <br/> |**Varia** <br/> |Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Numeric
  
## <a name="remarks"></a>Comentários

O valor retornado é um número no intervalo de 0 a 240, inclusive. A função retornará 0 para uma entrada inválida.
  
## <a name="example-1"></a>Exemplo 1

SAT(Sheet.4! FillForegnd)
  
Retornará a saturação da cor de preenchimento de primeiro plano de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

SAT(8)
  
Retornará 240 se o documento utilizar a paleta de cores padrão do Visio, sendo vermelho escuro a cor do índice 8.
  
## <a name="example-3"></a>Exemplo 3

SAT(HSL(10, 20, 30))
  
Retornará 20.
  

