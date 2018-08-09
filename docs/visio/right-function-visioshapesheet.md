---
title: Função RIGHT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Retorna o último caractere ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772724"
---
# <a name="right-function-visioshapesheet"></a>Função RIGHT (VisioShapeSheet)

Retorna o último caractere ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.
  
## <a name="syntax"></a>Sintaxe

DIREITA (* * *texto* * * [, * * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> | A cadeia de caracteres de texto que contém os caracteres a serem extraídos.  <br/> |
| _num_chars_opt_ <br/> |Opcional  <br/> |**Número** <br/> |O número de caracteres que deseja extrair. O padrão é 1.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

O valor de _num_chars_opt_ deve ser maior ou igual a zero (0). 
  
Se _num_chars_opt_ for maior que o comprimento do texto, direita retorna todo o texto. Se _num_chars_opt_ for omitido, presume-se a 1. 
  
## <a name="example"></a>Exemplo

RIGHT ("1º de janeiro de 2004", 4) 
  
Retornará o valor 2004. 
  

