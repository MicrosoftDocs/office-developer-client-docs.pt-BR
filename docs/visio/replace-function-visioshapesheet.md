---
title: Função REPLACE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Substitui parte de uma sequência de caracteres de texto, baseada no número de caracteres especificado, por uma sequência de caracteres de texto diferente.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414351"
---
# <a name="replace-function-visioshapesheet"></a>Função REPLACE (VisioShapeSheet)

Substitui parte de uma sequência de caracteres de texto, baseada no número de caracteres especificado, por uma sequência de caracteres de texto diferente.
  
## <a name="syntax"></a>Sintaxe

REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto no qual você deseja substituir alguns caracteres.  <br/> |
| _start_num_ <br/> |Obrigatório  <br/> |**Número** <br/> |A posição do caractere no  _old_text_ que você deseja substituir por  _new_text_. O primeiro caractere na cadeia é a posição 1.  <br/> |
| _num_chars_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de caracteres  _old_text_ que você deseja substituir  <br/> |
| _new_text_ <br/> |Obrigatório  <br/> |**String** <br/> |O texto que substituirá caracteres em  _old_text_.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

Use a função REPLACE para substituir o texto que ocorre em um determinado local da sequência de texto. Para substituir um texto específico na sequência de texto, use a função SUBSTITUTE.
  
## <a name="example"></a>Exemplo

REPLACE ("01/03/2002",9,2,"03") 
  
Retornará 01/03/2003. 
  

