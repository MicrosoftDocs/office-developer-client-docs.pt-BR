---
title: Função MASTERNAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Retorna o nome do mestre de uma planilha como uma cadeia de caracteres ou não retorna a cadeia de caracteres 'nenhum mestre' se a folha não tiver um mestre.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772325"
---
# <a name="mastername-function"></a>Função MASTERNAME

Retorna o nome do mestre de uma planilha como uma cadeia de caracteres ou retorna a cadeia de caracteres "\<nenhum mestre\>" se a folha não tiver um mestre.
  
## <a name="syntax"></a>Sintaxe

MASTERNAME ([* * *langID_opt* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Opcional  <br/> |**Número** <br/> |Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Se você passar um código de linguagem inválido, a linguagem local será utilizada. 
  

