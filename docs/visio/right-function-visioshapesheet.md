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
description: Retorna o último caractere ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres que você especificar.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411453"
---
# <a name="right-function-visioshapesheet"></a>Função RIGHT (VisioShapeSheet)

Retorna o último caractere ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres que você especificar.
  
## <a name="syntax"></a>Sintaxe

RIGHT(** *text* ** [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> | A cadeia de caracteres de texto que contém os caracteres a serem extraídos.  <br/> |
| _num_chars_opt_ <br/> |Opcional  <br/> |**Número** <br/> |O número de caracteres que deseja extrair. O padrão é 1.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

O valor de  _num_chars_opt_ deve ser maior ou igual a zero (0). 
  
Se  _num_chars_opt_ for maior que o comprimento do texto, RIGHT retornará todo o texto. Se  _num_chars_opt_ for omitido, será assumido como 1. 
  
## <a name="example"></a>Exemplo

RIGHT ("1º de janeiro de 2004", 4) 
  
Retornará o valor 2004. 
  

