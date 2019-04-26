---
title: Função BKGPAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Retorna um nome de página de plano de fundo como uma cadeia de caracteres.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358538"
---
# <a name="bkgpagename-function"></a>Função BKGPAGENAME

Retorna um nome de página de plano de fundo como uma cadeia de caracteres.
  
## <a name="syntax"></a>Sintaxe

BKGPAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Opcional  <br/> |**Numérica** <br/> |Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

Se a página para a qual você está usando a função não tiver uma página de plano de fundo, a cadeia de caracteres "\<sem plano de fundo\>" é retornada. 
  
Se você passar um código de linguagem inválido, a linguagem local será utilizada. 
  

