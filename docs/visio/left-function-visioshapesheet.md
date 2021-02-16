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
description: Retorna o caractere ou caractere mais à esquerda em uma cadeia de caracteres de texto, com base no número de caracteres que você especificar.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427518"
---
# <a name="left-function-visioshapesheet"></a>Função LEFT (VisioShapeSheet)

Retorna o caractere ou caractere mais à esquerda em uma cadeia de caracteres de texto, com base no número de caracteres que você especificar.
  
## <a name="syntax"></a>Sintaxe

LEFT(** *text* **, [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres de texto que contém os caracteres a serem extraídos.  <br/> |
| _num_chars_opt_ <br/> |Opcional  <br/> |**Numérica** <br/> |O número de caracteres que deseja extrair.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

O valor de  _num_chars_opt_ deve ser maior ou igual a zero (0). 
  
Se  _num_chars_opt_ for maior que o comprimento do texto, LEFT retornará todo o texto. Se  _num_chars_opt_ for omitido, será assumido como 1. 
  
## <a name="example"></a>Exemplo

LEFT ("1º de janeiro de 2004", 3) 
  
Retorna o valor "Jan". 
  

