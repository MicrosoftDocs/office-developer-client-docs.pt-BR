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
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438103"
---
# <a name="green-function"></a>Função GREEN

Retorna o componente verde de uma cor.
  
## <a name="syntax"></a>Sintaxe

Expressão GREEN(** *** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obrigatório  <br/> |**Varia** <br/> |Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cor.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O valor retornado é um número entre 0 e 255, inclusive, ou uma referência de célula que resulta em um índice. Se  *a expressão*  for inválida, ela retornará 0 (preto). 
  
## <a name="example-1"></a>Exemplo 1

GREEN(Sheet.4! FillForegnd)
  
Retornará o componente verde da cor de primeiro plano do preenchimento de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

GREEN(11)
  
Retornará 128 se o documento utilizar a paleta de cores padrão do Visio, sendo amarelo escuro a cor do índice 11.
  
## <a name="example-3"></a>Exemplo 3

GREEN(RGB(10, 20, 30))
  
Retornará 20.
  

