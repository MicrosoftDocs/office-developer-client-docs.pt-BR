---
title: Função REWIDEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Converte uma fórmula que produz códigos de caracteres de 16 bits que são largo códigos de conjunto de caracteres de byte único ou vários bytes em uma cadeia de códigos de caracteres Unicode 16 bits, usando os conjuntos de caracteres especificado.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772731"
---
# <a name="rewiden-function"></a>Função REWIDEN

Converte uma fórmula que produz códigos de caracteres de 16 bits que são largo códigos de conjunto de caracteres de byte único ou vários bytes em uma cadeia de códigos de caracteres Unicode 16 bits, usando os conjuntos de caracteres especificado. 
  
## <a name="syntax"></a>Sintaxe

REWIDEN (* * *srcCharSet* * *, * * *dstCharSet* * *, * * *texto* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Obrigatório  <br/> |**String** <br/> |O conjunto de caracteres no documento de origem.  <br/> |
| _dstCharSet_ <br/> |Obrigatório  <br/> |**String** <br/> | O conjunto de caracteres no documento de destino.  <br/> |
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto a ser convertido.  <br/> |
   
## <a name="remarks"></a>Comentários

A função REWIDEN é usada na conversão automática de documentos do Visio 2002 em documentos do Visio 2003. A utilização para outros fins não é recomendada.
  

