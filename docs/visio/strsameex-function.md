---
title: Função STRSAMEEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Determina se duas cadeias de caracteres são iguais.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413861"
---
# <a name="strsameex-function"></a>Função STRSAMEEX

Determina se duas cadeias de caracteres são iguais.
  
## <a name="syntax"></a>Sintaxe

STRSAMEEX ("* * *seqüência1* * *", "* * *seqüência2* * *", * * *LocaleID* * *, * * *sinalizador* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A primeira cadeia a ser comparada.  <br/> |
| _string2_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | A segunda cadeia a ser comparada.  <br/> |
| _localeID_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O código de identificação de local.  <br/> |
| _flag_ <br/> |Obrigatório  <br/> |**Numérica** <br/> | Um bit que especifica o tipo de comparação.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="remarks"></a>Comentários

STRSAMEEX retornará VERDADEIRO se as duas cadeias de caracteres de entrada forem iguais e FALSO se forem diferentes. Use esta função para comparar cadeias de caracteres multibyte ou para fazer comparações usando regras de maiúsculas e minúsculas para um local específico.
  
Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.
  
|**Flag**|**Descrição**|
|:-----|:-----|
|1  <br/> |Ignorar maiúsculas e minúsculas.  <br/> |
|duas  <br/> |Ignorar caracteres sem espaçamento.  <br/> |
|4   <br/> |Ignorar símbolos.  <br/> |
|4096  <br/> |Tratar a pontuação da mesma forma que os símbolos.  <br/> |
|65536  <br/> |Não diferenciar entre os caracteres Hiragana e Katakana.  <br/> |
|131072  <br/> |Não diferenciar entre um caractere de byte único e o mesmo caractere como um caractere de byte duplo.  <br/> |
   

