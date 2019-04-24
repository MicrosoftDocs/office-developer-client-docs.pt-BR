---
title: Função LEFT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Retorna os caracteres mais à esquerda em uma sequência de caracteres de texto, com base no número de caracteres especificado.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309461"
---
# <a name="left-function-visioshapesheet"></a>Função LEFT (VisioShapeSheet)

Retorna os caracteres mais à esquerda em uma sequência de caracteres de texto, com base no número de caracteres especificado.
  
## <a name="syntax"></a>Sintaxe

Left (* * *Text* * *, [, * * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres de texto que contém os caracteres a serem extraídos.  <br/> |
| _num_chars_opt_ <br/> |Opcional  <br/> |**Numeric** <br/> |O número de caracteres que deseja extrair.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

O valor de _num_chars_opt_ deve ser maior ou igual a zero (0). 
  
Se _num_chars_opt_ for maior do que o comprimento do texto, Left retornará todo o texto. Se _num_chars_opt_ for omitido, será considerado 1. 
  
## <a name="example"></a>Exemplo

LEFT ("1º de janeiro de 2004", 3) 
  
Retorna o valor "Jan". 
  

