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
description: Retorna o nome de uma página de plano de fundo como uma cadeia de caracteres.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771397"
---
# <a name="bkgpagename-function"></a>Função BKGPAGENAME

Retorna o nome de uma página de plano de fundo como uma cadeia de caracteres.
  
## <a name="syntax"></a>Sintaxe

BKGPAGENAME (* * *langID_opt* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Opcional  <br/> |**Numérico** <br/> |Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Se a página para o qual você estiver usando a função não tiver uma página de plano de fundo, a cadeia de caracteres "\<nenhum plano de fundo\>" é retornado. 
  
Se você passar um código de linguagem inválido, a linguagem local será utilizada. 
  

