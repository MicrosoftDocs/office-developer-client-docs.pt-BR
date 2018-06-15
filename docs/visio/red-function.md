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
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772638"
---
# <a name="red-function"></a>Função RED

Retorna o componente vermelho de uma cor. 
  
## <a name="syntax"></a>Sintaxe

VERMELHO (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**Varia** <br/> |Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Número
  
## <a name="remarks"></a>Comentários

O valor de retorno é um número no intervalo de 0 a 255, inclusive, ou uma referência de célula que resulta em um índice. Se a _expressão_ for inválida, essa função retornará 0 (preto). 
  
## <a name="example-1"></a>Exemplo 1

RED(22)
  
Retornará 51 se o documento utilizar a paleta de cores padrão do Microsoft Office Visio, sendo cinza escuro a cor do índice 22.
  
## <a name="example-2"></a>Exemplo 2

Red(char.Color)
  
Retorna o valor do componente vermelho da cor de origem atual.
  
## <a name="example-3"></a>Exemplo 3

RED(RGB(10, 20, 30))
  
Retornará 10.
  

