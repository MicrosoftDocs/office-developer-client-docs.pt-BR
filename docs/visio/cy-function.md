---
title: Função CY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Retorna um valor de moeda.
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771628"
---
# <a name="cy-function"></a>Função CY

Retorna um valor de moeda.
  
## <a name="syntax"></a>Sintaxe

CY (* * *valor* * *, * * *cyID* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Opcional  <br/> |**Número ou Cadeia de caracteres** <br/> |Um número ou uma cadeia de caracteres que inclui formatação específica de moeda. Se não especificado, o valor de moeda é formatado de acordo com o estilo de moeda nas configurações de região e idioma do sistema.  <br/> |
| _cyID_ <br/> |Opcional  <br/> |**Número** <br/> |Uma identificação de moeda numérica ou uma sequência de três caracteres entre aspas para a abreviação ISO 4217.  <br/> |
   
## <a name="remarks"></a>Comentários

Para especificar uma moeda diferente, você deve incluir um válido _cyID_. Para obter uma lista, consulte [sobre constantes de moeda](about-currency-constants.md).
  
Se o _valor_ é incompatível com o tipo de moeda designado, ou se um argumento inválido, como "não é um número" for especificado, um #VALUE! erro será retornado. Se o _valor_ for maior que 922.337.203.685.477,5807 ou menor que-922.337.203.685.477,5808, um #VALUE! erro será retornado. 
  
Para obter uma precisão maior com valores de moeda muito elevados que incluam frações de uma unidade, como 3,6 trilhões, use os argumentos de cadeia de caracteres de _valor_.
  
Especificar um inválido _cyID_ retornará um erro. 
  
## <a name="example-1"></a>Exemplo 1

No caso das configurações de Região e Idioma do usuário, especifique dólares dos Estados Unidos:
  
CY(999998.993)
  
Retornará $999.998,99
  
## <a name="example-2"></a>Exemplo 2

CY(12345678,.993, "USD")
  
Retornará $12.345.678,99
  
## <a name="example-3"></a>Exemplo 3

CY(12345678,993, "DEM")
  
Retornará 12.345.678,99 DEM
  
## <a name="example-4"></a>Exemplo 4

CY(12345678,7832, "XXX")
  
Retornará 12.345.678,78
  

