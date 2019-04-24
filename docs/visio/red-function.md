---
title: Função RED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Retorna o componente vermelho de uma cor.
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359980"
---
# <a name="red-function"></a>Função RED

Retorna o componente vermelho de uma cor. 
  
## <a name="syntax"></a>Sintaxe

VERMELHO (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**Vai** <br/> |Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

O valor retornado é um número entre 0 e 255, inclusive, ou uma referência de célula que resulta em um índice. Se a _expressão_ for inválida, esta função retornará 0 (preto). 
  
## <a name="example-1"></a>Exemplo 1

VERMELHO (22)
  
Retornará 51 se o documento utilizar a paleta de cores padrão do Microsoft Office Visio, sendo cinza escuro a cor do índice 22.
  
## <a name="example-2"></a>Exemplo 2

VERMELHO (Char. Color)
  
Retorna o valor do componente vermelho da cor de origem atual.
  
## <a name="example-3"></a>Exemplo 3

RED(RGB(10, 20, 30))
  
Retornará 10.
  

