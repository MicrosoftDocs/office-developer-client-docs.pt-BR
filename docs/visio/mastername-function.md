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
description: Retorna o nome mestre de uma planilha como uma cadeia de caracteres ou retorna a cadeia de caracteres 'nenhum mestre' se a planilha não tiver um mestre.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414750"
---
# <a name="mastername-function"></a>Função MASTERNAME

Retorna o nome mestre de uma planilha como uma cadeia de caracteres ou retorna a cadeia de caracteres " no master " se \< a planilha não tiver um \> mestre.
  
## <a name="syntax"></a>Sintaxe

MASTERNAME ([ ** *langID_opt* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Opcional  <br/> |**Número** <br/> |Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

Se você passar um código de linguagem inválido, a linguagem local será utilizada. 
  

