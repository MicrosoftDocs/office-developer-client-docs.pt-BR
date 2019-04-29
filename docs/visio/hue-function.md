---
title: Função HUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Retorna o valor do componente de matiz de uma cor.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439489"
---
# <a name="hue-function"></a>Função HUE

Retorna o valor do componente de matiz de uma cor.
  
## <a name="syntax"></a>Sintaxe

MATIZ (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |Uma expressão que é avaliada para uma cor.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

O valor retornado é um número entre 0 e 239, inclusive. A entrada é um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores. A função retornará 0 para uma entrada inválida. 
  
## <a name="example-1"></a>Exemplo 1

MATIZ (planilha. 4! FillForegnd
  
Retornará a matiz da cor de preenchimento de primeiro plano de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

MATIZ (7)
  
Retornará 120 se o documento utilizar a paleta de cores padrão do Microsoft Visio, sendo ciano a cor do índice 7.
  
## <a name="example-3"></a>Exemplo 3

HUE(HSL(10, 20, 30) )
  
Retornará 10.
  

