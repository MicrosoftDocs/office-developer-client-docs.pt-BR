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
description: Aplica o padrão de linha, o padrão de preenchimento ou o nome de fim de linha chamado à forma quando colocado na célula LinePattern, FillPattern, BeginArrow ou endArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337146"
---
# <a name="use-function"></a>Função USE

Aplica o padrão de linha, o padrão de preenchimento ou o _nome_ de fim de linha chamado à forma quando colocado na célula LinePattern, FillPattern, BeginArrow ou endarrow. 
  
## <a name="syntax"></a>Sintaxe

USE ("* * *nome* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres que seja um nome de mestre válido.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Se um _nome_ mestre nomeado estiver presente no estêncil de documento do documento, o padrão será aplicado como um padrão de linha, padrão de preenchimento, seta de início ou seta de fim. 
  
Essa função sempre retornará 254.
  
## <a name="example"></a>Exemplo

USE("Railroad Tracks") 
  
Formata a forma aplicando o padrão de mestre nomeado Railroad Tracks à forma que contém a fórmula. 
  

