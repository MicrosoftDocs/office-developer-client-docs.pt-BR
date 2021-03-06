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
description: Converte uma fórmula que produz códigos de caracteres de 16 bits que são códigos de conjunto de caracteres de um ou vários byte ampliados em uma cadeia de caracteres Unicode de 16 bits, usando os conjuntos de caracteres especificados.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405209"
---
# <a name="rewiden-function"></a>Função REWIDEN

Converte uma fórmula que produz códigos de caracteres de 16 bits que são códigos de conjunto de caracteres de um ou vários byte ampliados em uma cadeia de caracteres Unicode de 16 bits, usando os conjuntos de caracteres especificados. 
  
## <a name="syntax"></a>Sintaxe

REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Obrigatório  <br/> |**String** <br/> |O conjunto de caracteres no documento de origem.  <br/> |
| _dstCharSet_ <br/> |Obrigatório  <br/> |**String** <br/> | O conjunto de caracteres no documento de destino.  <br/> |
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto a ser convertido.  <br/> |
   
## <a name="remarks"></a>Comentários

A função REWIDEN é usada na conversão automática de documentos do Visio 2002 em documentos do Visio 2003. A utilização para outros fins não é recomendada.
  

