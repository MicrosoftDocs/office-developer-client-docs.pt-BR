---
title: Função SUBSTITUTE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Substitui parte de uma cadeia de caracteres de texto por uma sequência de texto diferente.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346820"
---
# <a name="substitute-function"></a>Função SUBSTITUTE

Substitui parte de uma cadeia de caracteres de texto por uma sequência de texto diferente. 
  
## <a name="syntax"></a>Sintaxe

 Substitua (* * *Text* * *, * * *texto_antigo* * *, * * *novo_texto* * * [, * * *Núm_inicial* * *] [, * * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto ou a referência a uma célula que contém o texto em que você deseja substituir os caracteres.  <br/> |
| _iguais_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto a ser substituído.  <br/> |
| _novo_texto_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto que você deseja usar para substituir _texto_antigo_.  <br/> |
| _start_num_opt_ <br/> |Opcional  <br/> |**Numeric** <br/> |Especifica quais ocorrências de texto_antigo serão substituídas.  <br/> |
| _ignore_case_opt_ <br/> |Opcional  <br/> |**Boolean** <br/> |FALSE se diferenciar maiúscula e minúscula; caso contrário, TRUE. O padrão é FALSE.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

 Se você especificar _start_num_opt_, somente essa ocorrência de _texto_antigo_ será substituída. Caso contrário, todas as ocorrências de _texto_antigo_ em _texto_ serão alteradas para _novo_texto._
  
Use a função SUBSTITUTE para substituir um texto específico que ocorre em uma sequência de texto. Se você quiser substituir o texto que ocorre em um local específico em uma cadeia de caracteres de texto, use a função REPLACE.
  
## <a name="example"></a>Exemplo

SUBSTITUTE ("1º de janeiro de 2003", "Janeiro", "JAN") 
  
Retornará "1 JAN 2003". 
  
SUBSTITUTE ("1º de janeiro de 2003","janeiro","JAN") 
  
Retornará "1 January 2003". Nenhuma alteração será feita pois a pesquisa do texto diferencia maiúscula e minúscula. 
  

