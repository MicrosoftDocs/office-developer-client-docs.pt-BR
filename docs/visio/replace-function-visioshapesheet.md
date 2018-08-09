---
title: Substituir função (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Substitui parte de uma cadeia de texto, baseada no número de caracteres especificado, por uma cadeia de texto diferente.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772684"
---
# <a name="replace-function-visioshapesheet"></a>Substituir função (VisioShapeSheet)

Substitui parte de uma sequência de caracteres de texto, baseada no número de caracteres especificado, por uma sequência de caracteres de texto diferente.
  
## <a name="syntax"></a>Sintaxe

Substituir (* * *old_text* * *, * * *Núm_inicial* * *, * * *Núm_caract* * *, * * *Novo_texto* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Texto_antigo_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto no qual você deseja substituir alguns caracteres.  <br/> |
| _Núm_inicial_ <br/> |Obrigatório  <br/> |**Número** <br/> |A posição do caractere em _texto_antigo_ que você deseja substituir por _Novo_texto_. O primeiro caractere na cadeia de caracteres é a posição 1.  <br/> |
| _Núm_caract_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de caracteres em _texto_antigo_ que você deseja substituir  <br/> |
| _Novo_texto_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto que substituirá os caracteres em _texto_antigo_.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Use a função REPLACE para substituir o texto que ocorre em um determinado local da sequência de texto. Para substituir um texto específico na sequência de texto, use a função SUBSTITUTE.
  
## <a name="example"></a>Exemplo

REPLACE ("01/03/2002",9,2,"03") 
  
Retornará 01/03/2003. 
  

