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
description: Substitui parte de uma cadeia de caracteres de texto com uma cadeia de caracteres de texto diferente.
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773085"
---
# <a name="substitute-function"></a>Função SUBSTITUTE

Substitui parte de uma cadeia de caracteres de texto com uma cadeia de caracteres de texto diferente. 
  
## <a name="syntax"></a>Sintaxe

 SUBSTITUTO (* * *texto* * *, * * *old_text* * *, * * *Novo_texto* * * [, * * *Núm_inicial* * *] [, * * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto ou a referência a uma célula que contém o texto em que você deseja substituir os caracteres.  <br/> |
| _Texto_antigo_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto a ser substituído.
  <br/> |
| _Novo_texto_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto que você deseja usar para substituir _old_text_.  <br/> |
| _start_num_opt_ <br/> |Opcional  <br/> |**Numérico** <br/> |Especifica quais ocorrências de old_text serão substituídas.  <br/> |
| _ignore_case_opt_ <br/> |Opcional  <br/> |**Boolean** <br/> |FALSE se diferenciar maiúscula e minúscula; caso contrário, TRUE. O padrão é FALSE.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

 Se você especificar _start_num_opt_, somente essa ocorrência de _texto_antigo_ será substituída. Caso contrário, cada ocorrência de _texto_antigo_ em _texto não_ é alterada para _novo_texto._
  
Use a função SUBSTITUTE quando quiser substituir texto específico em uma cadeia de caracteres de texto. Se você quiser substituir o texto que ocorre em um local específico em uma cadeia de caracteres de texto, use a função REPLACE.
  
## <a name="example"></a>Exemplo

SUBSTITUTE ("1º de janeiro de 2003", "Janeiro", "JAN") 
  
Retornará "1 JAN 2003". 
  
SUBSTITUTE ("1º de janeiro de 2003","janeiro","JAN") 
  
Retornará "1 de janeiro de 2003". Nenhuma alteração é feita porque a pesquisa de texto diferencia maiusculas de minúsculas. 
  

