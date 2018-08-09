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
description: Retorna o caractere mais à esquerda ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772178"
---
# <a name="left-function-visioshapesheet"></a>Função LEFT (VisioShapeSheet)

Retorna o caractere mais à esquerda ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.
  
## <a name="syntax"></a>Sintaxe

ESQUERDA (* * *texto* * *, [, * * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres de texto que contém os caracteres a serem extraídos.  <br/> |
| _num_chars_opt_ <br/> |Opcional  <br/> |**Numérico** <br/> |O número de caracteres a extrair.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

O valor de _num_chars_opt_ deve ser maior ou igual a zero (0). 
  
Se _num_chars_opt_ for maior que o comprimento do texto, esquerda retornará todo o texto. Se _num_chars_opt_ for omitido, presume-se a 1. 
  
## <a name="example"></a>Exemplo

LEFT ("1º de janeiro de 2004", 3) 
  
Retorna o valor "Jan". 
  

