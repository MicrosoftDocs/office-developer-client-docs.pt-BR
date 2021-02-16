---
title: Função MID (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Retorna um número específico de caracteres de uma cadeia de caracteres de texto, começando na posição especificada, com base no número de caracteres especificado.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410263"
---
# <a name="mid-function-visioshapesheet"></a>Função MID (VisioShapeSheet)

Retorna um número específico de caracteres de uma cadeia de caracteres de texto, começando na posição especificada, com base no número de caracteres especificado.
  
## <a name="syntax"></a>Sintaxe

MID (** *texto* **, ** *start_num* **, ** *num_chars* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres de texto que contém os caracteres a serem extraídos.  <br/> |
| _start_num_ <br/> |Obrigatório  <br/> |**Número** <br/> |A posição do primeiro caractere a ser extraído. O primeiro caractere na cadeia de caracteres de texto está na posição 1.  <br/> |
| _num_chars_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de caracteres a retornar.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

Se  *start_num*  for: 
  
- Maior que o comprimento do  *texto,*  MID retornará "" (texto vazio). 
    
- Menor que o comprimento do  *texto,*  mas  *start_num*  mais  *num_chars*  exceder o comprimento do texto  *,*  MID retorna os caracteres até o final do  *texto*  . 
    
- Menor que 1, MID retornará o #VALUE! valor de erro. 
    
Se  *num_chars*  for negativo, MID retornará a #VALUE! valor de erro. 
  
## <a name="example"></a>Exemplo

MID ("SSN 999-99-9999",5,11) 
  
Retorna 999-99-9999. 
  

