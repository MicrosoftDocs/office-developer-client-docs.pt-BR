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
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772395"
---
# <a name="mid-function-visioshapesheet"></a>Função MID (VisioShapeSheet)

Retorna um número específico de caracteres de uma cadeia de caracteres de texto, começando na posição especificada, com base no número de caracteres especificado.
  
## <a name="syntax"></a>Sintaxe

MID (* * *texto* * *, * * *Núm_inicial* * *, * * *Núm_caract* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres de texto que contém os caracteres a serem extraídos.  <br/> |
| _Núm_inicial_ <br/> |Obrigatório  <br/> |**Número** <br/> |A posição do primeiro caractere a ser extraído. O primeiro caractere na cadeia de caracteres de texto está na posição 1.  <br/> |
| _Núm_caract_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de caracteres a retornar.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Se *Núm_inicial* for: 
  
- Maior que o comprimento de *text* , MID retornará "" (texto vazio). 
    
- Menor que o comprimento do *texto* , mas se *start_num* mais *num_chars* ultrapassarem o comprimento de *text* , MID retornará os caracteres até o final do *texto* . 
    
- Menor que 1, MID retornará o valor de erro #VALUE! 
    
Se *num_chars* for negativo, MID retornará o #VALUE! valor de erro. 
  
## <a name="example"></a>Exemplo

MID ("SSN 999-99-9999",5,11) 
  
Retorna 999-99-9999. 
  

