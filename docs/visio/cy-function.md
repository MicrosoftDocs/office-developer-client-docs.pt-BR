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
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433553"
---
# <a name="cy-function"></a>Função CY

Retorna um valor de moeda.
  
## <a name="syntax"></a>Sintaxe

CY (* * *valor* * *, * * *cyID* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Opcional  <br/> |**Número ou Cadeia de caracteres** <br/> |Um número ou uma cadeia de caracteres que inclui formatação específica da moeda. Se não for especificado, o valor de moeda é formatado de acordo com o estilo de moeda nas configurações de idioma e região do sistema.  <br/> |
| _cyID_ <br/> |Opcional  <br/> |**Número** <br/> |Uma ID de moeda numérica ou uma cadeia de caracteres entre aspas de três caracteres para a abreviação ISO 4217.  <br/> |
   
## <a name="remarks"></a>Comentários

Para especificar uma moeda diferente, você deve incluir um _cyID_válido. Para obter uma lista, consulte [Sobre constantes de moeda](about-currency-constants.md).
  
Se o _valor_ for incompatível com o tipo de moeda designada ou se um argumento inválido, como "não um número", for especificado, um #VALUE! será retornado. Se o _valor_ for maior que 922337203685477,5807 ou menor que-922337203685477,5808, um #VALUE! será retornado. 
  
Para maior precisão com valores de moeda muito grandes que incluem frações de uma unidade, como 3.600.000.000.000, use argumentos de cadeia de caracteres para _Value_.
  
A especificação de um _cyID_ inválido retorna um erro. 
  
## <a name="example-1"></a>Exemplo 1

No caso das configurações de Região e Idioma do usuário, especifique dólares dos Estados Unidos:
  
CY (999998.993)
  
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
  

