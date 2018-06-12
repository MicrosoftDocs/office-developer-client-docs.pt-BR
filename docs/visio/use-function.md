---
title: Função USE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Aplica o padrão de linha, o padrão de preenchimento ou o fim de linha denominado nome à forma quando colocada na célula LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773224"
---
# <a name="use-function"></a>Função USE

Aplica o padrão de linha, o padrão de preenchimento ou o fim de linha denominado _nome_ à forma quando colocada na célula LinePattern, FillPattern, BeginArrow ou EndArrow. 
  
## <a name="syntax"></a>Sintaxe

USO ("* * *nome* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres que seja um nome de mestre válido.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Número
  
## <a name="remarks"></a>Comentários

Se um mestre chamado _name_ estiver presente no estêncil do documento do documento, o padrão será aplicado como um padrão de linha, o padrão de preenchimento, uma seta inicial ou seta final. 
  
Essa função sempre retornará 254.
  
## <a name="example"></a>Example

USE("Railroad Tracks") 
  
Formata a forma aplicando o padrão de mestre nomeado Railroad Tracks à forma que contém a fórmula. 
  

